---
name: anthropic-batch-processing
description: Submit, poll, retrieve and cancel a Claude Message Batch on the Anthropic API — the 50%-discount asynchronous path for large Messages workloads.
api: Anthropic Message Batches API
operations:
  - createMessageBatch
  - retrieveMessageBatch
  - retrieveMessageBatchResults
  - listMessageBatches
  - cancelMessageBatch
  - deleteMessageBatch
generated: '2026-08-27'
method: generated
source: openapi/anthropic-message-batches-api-openapi.yml, https://platform.claude.com/docs/en/build-with-claude/batch-processing
---

# Process a Claude Message Batch

Use this when you have many Messages requests that do not need an immediate
response. Batching costs 50% of standard token pricing.

## Preconditions

- `x-api-key` header with a Claude API key (see `authentication/anthropic-authentication.yml`).
- `anthropic-version: 2023-06-01` header on every request.
- Base URL `https://api.anthropic.com`.

## Steps

1. **Submit the batch** — `createMessageBatch` (`POST /v1/messages/batches`).
   Each entry in `requests[]` carries a `custom_id` you choose and a `params`
   object shaped exactly like a Messages request. Every batched request must set
   `max_tokens` of at least `1`; `max_tokens: 0` (cache pre-warming) is rejected
   inside a batch. Request body limit is 256MB.
   The `custom_id` is the only correlation key you get back — make it stable and
   unique, because the API applies no idempotency key of its own.

2. **Poll for completion** — `retrieveMessageBatch`
   (`GET /v1/messages/batches/{message_batch_id}`). Watch
   `processing_status` and `request_counts` (`processing`, `succeeded`,
   `errored`, `canceled`, `expired`). Most batches finish in under an hour.
   Results become available when every request completes **or after 24 hours,
   whichever comes first**; a batch that has not finished within 24 hours
   expires and its unstarted requests are marked `expired` and are not billed.

3. **Read the results** — `retrieveMessageBatchResults`
   (`GET /v1/messages/batches/{message_batch_id}/results`). The response is
   JSONL, one line per request, keyed by your `custom_id`. Results are
   **available for 29 days after creation**; after that the batch object is
   still readable but the results are not downloadable, and the batch object
   reports `archived_at`.

4. **Handle the four per-request outcomes** — `succeeded`, `errored`,
   `canceled`, `expired`. Only `succeeded` and `errored` consume tokens.
   Order is not guaranteed; always match on `custom_id`, never on position.

## Reversal

- `cancelMessageBatch` (`POST /v1/messages/batches/{message_batch_id}/cancel`)
  may be called **any time before processing ends**. The batch moves to
  `canceling`; in-progress non-interruptible requests may still complete, so a
  cancel is not guaranteed to cancel anything. Check `request_counts.canceled`.
- `deleteMessageBatch` (`DELETE /v1/messages/batches/{message_batch_id}`)
  removes the batch. This is not reversible.

## Errors

Errors use Anthropic's own envelope, not RFC 9457:
`{"type":"error","error":{"type":"...","message":"..."},"request_id":"..."}`.
See `errors/anthropic-problem-types.yml`. Always log the `request-id` response
header — it is what Anthropic support asks for.

## Rate limits

Batch submission is subject to the usage-tier limits in
`rate-limits/anthropic-rate-limits.yml`. On 429, honour `retry-after`.
