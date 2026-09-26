---
name: anthropic-files-workflow
description: Upload a file to the Anthropic Files API, reference it from a Messages request, download it back, and delete it when done.
api: Anthropic Files API
operations:
  - upload_file_v1_files_post
  - list_files_v1_files_get
  - get_file_metadata_v1_files__file_id__get
  - download_file_v1_files__file_id__content_get
  - delete_file_v1_files__file_id__delete
  - messages_post
generated: '2026-09-23'
method: generated
source: openapi/anthropic-files-api-openapi.yml, openapi/anthropic-messages-api-openapi.yml, https://platform.claude.com/docs/en/build-with-claude/files
---

# Upload, use, and clean up a file

## Preconditions

- `x-api-key` and `anthropic-version: 2023-06-01` headers.
- Base URL `https://api.anthropic.com`. Upload size limit 500MB.
- The Files API left beta on 2026-08-19: the `files-api-2025-04-14` beta header
  is no longer required, and requests sent **without** it use the current
  response format (file expiration + `page`/`next_page` pagination). Sending the
  old header still works but returns the previous shape — pick one and be
  consistent.

## Steps

1. **Upload** — `upload_file_v1_files_post` (`POST /v1/files`), `multipart/form-data`.
   Optionally set `expires_in_seconds`; the file object reports `expires_at`.
   Keep the returned `id` — it is the only handle.
2. **Confirm** — `get_file_metadata_v1_files__file_id__get` (`GET /v1/files/{file_id}`) to check
   `size_bytes`, `mime_type` and `expires_at` before you spend tokens on it.
3. **Use it** — `messages_post` (`POST /v1/messages`) with a content block that
   references the file id. This is where the file earns its cost; a file that is
   never referenced is just storage.
4. **Download** — `download_file_v1_files__file_id__content_get` (`GET /v1/files/{file_id}/content`)
   returns the bytes.
5. **List** — `list_files_v1_files_get` (`GET /v1/files`) with `page`/`next_page` cursors and
   an `ids[]` filter.

## Reversal

- `delete_file_v1_files__file_id__delete` (`DELETE /v1/files/{file_id}`) is **permanent — there is no
  restore and no stated grace window.** Confirm the id before calling it.
- The soft alternative is expiry: set `expires_in_seconds` at upload so the file
  removes itself, rather than deleting eagerly.

## Errors and conventions

See `conventions/anthropic-conventions.yml` and
`errors/anthropic-problem-types.yml`. There is no idempotency-key header on this
API, so a retried upload creates a second file — list before you re-upload.
