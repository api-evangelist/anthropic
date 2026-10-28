# Anthropic

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Anthropic is an AI safety company and the creator of the Claude family of large language models (Opus, Sonnet, Haiku, and the Fable/Mythos frontier line). The Claude Developer Platform exposes them through a single REST API at api.anthropic.com: the Messages API for text, vision, tool use, thinking, streaming and structured outputs; Message Batches for asynchronous work at half price; Files, Token Counting, Models, and experimental Prompt Tools; Managed Agents with sessions, environments, memory stores, vaults and scheduled deployments; a Skills API; and an Admin API for organizations, workspaces, members, invites and API keys. Authentication is x-api-key with a required anthropic-version date header and dated anthropic-beta opt-ins. Anthropic also authors two of the open standards the agent ecosystem runs on — the Model Context Protocol and the Agent Skills specification — and ships Claude Code, the terminal agentic coding tool, which doubles as a first-party stdio MCP server.

**Areas:** LLM · Anthropic · Artificial Intelligence · Claude · Foundation Models · Machine Learning · MCP · Agents

## Anthropic on APIs.io

Everything profiled for Anthropic is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/anthropic/](https://apis.io/providers/anthropic/)** — or go straight to one of the APIs or properties below.

### APIs (29)

- [Anthropic Messages API](https://apis.io/apis/anthropic/anthropic-messages-api/) — Send a structured list of input messages with text and/or image content, and the model will generate the next message in the conversation. The Messages API…
- [Anthropic Models API](https://apis.io/apis/anthropic/anthropic-models-api/) — List and inspect Claude models including Opus 4.7, Sonnet 4.6, and Haiku 4.5. The response includes max_input_tokens, max_tokens, and a capabilities object…
- [Anthropic Files API](https://apis.io/apis/anthropic/anthropic-files-api/) — The Files API lets you upload and manage files for reuse across Messages, Batches, code execution, and Managed Agents without re-uploading content. 500 MB…
- [Anthropic Skills API](https://apis.io/apis/anthropic/anthropic-skills-api/) — Create and manage custom Agent Skills. Skills are filesystem-based directories of instructions, scripts, and resources that Claude loads on demand via…
- [Anthropic Agents API](https://apis.io/apis/anthropic/anthropic-agents-api/) — Reusable, versioned agent configurations
- [Anthropic Api Keys API](https://apis.io/apis/anthropic/anthropic-api-keys-api/) — Monitor and manage API keys
- [Anthropic Cost API](https://apis.io/apis/anthropic/anthropic-cost-api/) — Service-level cost reporting
- [Anthropic Environments API](https://apis.io/apis/anthropic/anthropic-environments-api/) — Container configuration for agent sessions
- [Anthropic Events API](https://apis.io/apis/anthropic/anthropic-events-api/) — User messages and tool results sent to a session
- [Anthropic Organization API](https://apis.io/apis/anthropic/anthropic-organization-api/) — Retrieve organization information and settings
- [Anthropic Organization Invites API](https://apis.io/apis/anthropic/anthropic-organization-invites-api/) — Create and manage organization invitations
- [Anthropic Organization Members API](https://apis.io/apis/anthropic/anthropic-organization-members-api/) — Manage organization members and their roles
- [Anthropic Prompt Generation API](https://apis.io/apis/anthropic/anthropic-prompt-generation-api/) — APIs for generating well-written prompts for specified tasks
- [Anthropic Prompt Improvement API](https://apis.io/apis/anthropic/anthropic-prompt-improvement-api/) — APIs for enhancing existing prompts with feedback
- [Anthropic Prompt Templatization API](https://apis.io/apis/anthropic/anthropic-prompt-templatization-api/) — APIs for converting prompts into reusable templates with variables
- [Anthropic Sessions API](https://apis.io/apis/anthropic/anthropic-sessions-api/) — Stateful agent execution instances
- [Anthropic Usage API](https://apis.io/apis/anthropic/anthropic-usage-api/) — Token usage and consumption reporting
- [Anthropic Workspace Members API](https://apis.io/apis/anthropic/anthropic-workspace-members-api/) — Manage workspace membership and roles
- [Anthropic Workspaces API](https://apis.io/apis/anthropic/anthropic-workspaces-api/) — Create and manage workspaces within an organization
- [Anthropic API](https://apis.io/apis/anthropic/anthropic-anthropic-api-api/) — The Anthropic API API from Anthropic — 0 operation(s) for anthropic api.
- [Anthropic Complete API](https://apis.io/apis/anthropic/anthropic-complete-api/) — The Complete API from Anthropic — 1 operation(s) for complete.
- [Anthropic Deployment Runs API](https://apis.io/apis/anthropic/anthropic-deployment-runs-api/) — The Deployment Runs API from Anthropic — 1 operation(s) for deployment runs.
- [Anthropic Deployments API](https://apis.io/apis/anthropic/anthropic-deployments-api/) — The Deployments API from Anthropic — 5 operation(s) for deployments.
- [Anthropic Dreams API](https://apis.io/apis/anthropic/anthropic-dreams-api/) — The Dreams API from Anthropic — 3 operation(s) for dreams.
- [Anthropic Memory Stores API](https://apis.io/apis/anthropic/anthropic-memory-stores-api/) — The Memory Stores API from Anthropic — 7 operation(s) for memory stores.
- [Anthropic Organizations API](https://apis.io/apis/anthropic/anthropic-organizations-api/) — The Organizations API from Anthropic — 43 operation(s) for organizations.
- [Anthropic Tunnels API](https://apis.io/apis/anthropic/anthropic-tunnels-api/) — The Tunnels API from Anthropic — 7 operation(s) for tunnels.
- [Anthropic User Profiles API](https://apis.io/apis/anthropic/anthropic-user-profiles-api/) — The User Profiles API from Anthropic — 2 operation(s) for user profiles.
- [Anthropic Vaults API](https://apis.io/apis/anthropic/anthropic-vaults-api/) — The Vaults API from Anthropic — 6 operation(s) for vaults.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (11)

Multi-step workflows that chain operations into a business task.

- [Anthropic Cancel a Message Batch and Confirm](https://apis.io/arazzos/anthropic/anthropic-batch-cancel-and-confirm-workflow/)
- [Anthropic Create Batch, Poll, and Retrieve Results](https://apis.io/arazzos/anthropic/anthropic-batch-create-poll-results-workflow/)
- [Anthropic Count Tokens Then Create Message](https://apis.io/arazzos/anthropic/anthropic-count-tokens-then-message-workflow/)
- [Anthropic Create Workspace and Add a Member](https://apis.io/arazzos/anthropic/anthropic-create-workspace-and-add-member-workflow/)
- [Anthropic Discover a Model and Send a Message](https://apis.io/arazzos/anthropic/anthropic-discover-model-and-message-workflow/)
- [Anthropic Invite an Org Member and Confirm](https://apis.io/arazzos/anthropic/anthropic-invite-org-member-and-confirm-workflow/)
- [Anthropic List Batches and Fetch Latest Results](https://apis.io/arazzos/anthropic/anthropic-list-batches-and-fetch-latest-results-workflow/)
- [Anthropic Onboard an Org Member into a Workspace](https://apis.io/arazzos/anthropic/anthropic-onboard-member-to-workspace-workflow/)
- [Anthropic Provision and Promote a Workspace Member](https://apis.io/arazzos/anthropic/anthropic-provision-and-promote-workspace-member-workflow/)
- [Anthropic Upload, List, and Clean Up a File](https://apis.io/arazzos/anthropic/anthropic-upload-list-and-cleanup-file-workflow/)
- [Anthropic Upload, Verify, and Download a File](https://apis.io/arazzos/anthropic/anthropic-upload-verify-download-file-workflow/)

#### AsyncAPI (2)

Event-driven and webhook contracts.

- [Anthropic Messages Streaming API](https://apis.io/asyncapis/anthropic/anthropic-asyncapi/)
- [Anthropic Webhooks](https://apis.io/asyncapis/anthropic/anthropic-webhooks/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/messages](https://apis.io/channels/anthropic/messages/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/anthropic/](https://apis.io/graphqls/anthropic/anthropic-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [anthropic-claude-api](https://apis.io/servers/anthropic/anthropic-claude-api/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Anthropic Agentic Access](https://apis.io/agentic-access/anthropic/anthropic-agentic-access/)

#### JSON Schema (120)

The data models the API reads and writes.

- [AddWorkspaceMemberRequest](https://apis.io/schemas/anthropic/anthropic-add-workspace-member-request/)
- [Agent](https://apis.io/schemas/anthropic/anthropic-agent/)
- [ApiKey](https://apis.io/schemas/anthropic/anthropic-api-key/)
- [ApiKeyList](https://apis.io/schemas/anthropic/anthropic-api-key-list/)
- [ApiKey](https://apis.io/schemas/anthropic/anthropic-beta-api-key/)
- [Body_create_skill_v1_skills_post](https://apis.io/schemas/anthropic/anthropic-beta-body-create-skill-v1-skills-post/)
- [BetaCreateDreamRequest](https://apis.io/schemas/anthropic/anthropic-beta-create-dream-request/)
- [CreateMessageParams](https://apis.io/schemas/anthropic/anthropic-beta-create-message-params/)
- [CreateSkillResponse](https://apis.io/schemas/anthropic/anthropic-beta-create-skill-response/)
- [CreateSkillVersionResponse](https://apis.io/schemas/anthropic/anthropic-beta-create-skill-version-response/)
- [BetaCreateTunnelCertificateRequestBody](https://apis.io/schemas/anthropic/anthropic-beta-create-tunnel-certificate-request-body/)
- [BetaCreateTunnelRequest](https://apis.io/schemas/anthropic/anthropic-beta-create-tunnel-request/)
- [BetaCreateUserProfileRequest](https://apis.io/schemas/anthropic/anthropic-beta-create-user-profile-request/)
- [BetaDream](https://apis.io/schemas/anthropic/anthropic-beta-dream/)
- [BetaEnrollmentUrl](https://apis.io/schemas/anthropic/anthropic-beta-enrollment-url/)
- [Environment](https://apis.io/schemas/anthropic/anthropic-beta-environment/)
- [EnvironmentListResponse](https://apis.io/schemas/anthropic/anthropic-beta-environment-list-response/)
- [ExternalKey](https://apis.io/schemas/anthropic/anthropic-beta-external-key/)
- [FederationIssuer](https://apis.io/schemas/anthropic/anthropic-beta-federation-issuer/)
- [FederationRule](https://apis.io/schemas/anthropic/anthropic-beta-federation-rule/)
- [FederationRuleUpdateParams](https://apis.io/schemas/anthropic/anthropic-beta-federation-rule-update-params/)
- [FileDeleteResponse](https://apis.io/schemas/anthropic/anthropic-beta-file-delete-response/)
- [FileListResponse](https://apis.io/schemas/anthropic/anthropic-beta-file-list-response/)
- [FileMetadataSchema](https://apis.io/schemas/anthropic/anthropic-beta-file-metadata-schema/)
- [GetSkillResponse](https://apis.io/schemas/anthropic/anthropic-beta-get-skill-response/)
- …and 95 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Anthropic Context](https://apis.io/jsonld/anthropic/anthropic-context/)

#### Collections (39)

Postman and Open Collection request collections.

- [Anthropic Admin API](https://apis.io/collections/anthropic/open-anthropic-admin-api/)
- [Anthropic Admin Agents API](https://apis.io/collections/anthropic/open-anthropic-agents-api/)
- [Anthropic Admin Agents Api Keys API](https://apis.io/collections/anthropic/open-anthropic-api-keys-api/)
- [Anthropic Admin Agents Claude Code Analytics API](https://apis.io/collections/anthropic/open-anthropic-claude-code-analytics-api/)
- [Anthropic Admin Agents Cost API](https://apis.io/collections/anthropic/open-anthropic-cost-api/)
- [Anthropic Admin Agents Environments API](https://apis.io/collections/anthropic/open-anthropic-environments-api/)
- [Anthropic Admin Agents Events API](https://apis.io/collections/anthropic/open-anthropic-events-api/)
- [Anthropic Admin Agents Files API](https://apis.io/collections/anthropic/open-anthropic-files-api/)
- [Anthropic Managed Agents API](https://apis.io/collections/anthropic/open-anthropic-managed-agents-api/)
- [Anthropic Admin Agents Message Batches API](https://apis.io/collections/anthropic/open-anthropic-message-batches-api/)
- [Anthropic Admin Agents Messages API](https://apis.io/collections/anthropic/open-anthropic-messages-api/)
- [Anthropic Admin Agents Models API](https://apis.io/collections/anthropic/open-anthropic-models-api/)
- [Anthropic Admin Agents Organization API](https://apis.io/collections/anthropic/open-anthropic-organization-api/)
- [Anthropic Admin Agents Organization Invites API](https://apis.io/collections/anthropic/open-anthropic-organization-invites-api/)
- [Anthropic Admin Agents Organization Members API](https://apis.io/collections/anthropic/open-anthropic-organization-members-api/)
- [Anthropic Admin Agents Prompt Generation API](https://apis.io/collections/anthropic/open-anthropic-prompt-generation-api/)
- [Anthropic Admin Agents Prompt Improvement API](https://apis.io/collections/anthropic/open-anthropic-prompt-improvement-api/)
- [Anthropic Admin Agents Prompt Templatization API](https://apis.io/collections/anthropic/open-anthropic-prompt-templatization-api/)
- [Anthropic Prompt Tools API](https://apis.io/collections/anthropic/open-anthropic-prompts-api/)
- [Anthropic Admin Agents Sessions API](https://apis.io/collections/anthropic/open-anthropic-sessions-api/)
- [Anthropic Admin Agents Skill Versions API](https://apis.io/collections/anthropic/open-anthropic-skill-versions-api/)
- [Anthropic Admin Agents Skills API](https://apis.io/collections/anthropic/open-anthropic-skills-api/)
- [Anthropic Admin Agents Token Counting API](https://apis.io/collections/anthropic/open-anthropic-token-counting-api/)
- [Anthropic Admin Agents Tokens API](https://apis.io/collections/anthropic/open-anthropic-tokens-api/)
- [Anthropic Admin Agents Usage API](https://apis.io/collections/anthropic/open-anthropic-usage-api/)
- …and 14 more published on APIs.io

#### Overlays (71)

OpenAPI overlays, including conversational phrasing for each operation.

- [Anthropic Agents Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-agents-api-phrasing-overlay/)
- [Anthropic Agents Beta True Overlay](https://apis.io/overlays/anthropic/anthropic-agents-beta-true-overlay/)
- [Anthropic Agents Overlay](https://apis.io/overlays/anthropic/anthropic-agents-overlay/)
- [Anthropic Api Keys Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-api-keys-api-phrasing-overlay/)
- [Anthropic Api Keys Overlay](https://apis.io/overlays/anthropic/anthropic-api-keys-overlay/)
- [Anthropic Api Overlay](https://apis.io/overlays/anthropic/anthropic-api-overlay/)
- [Anthropic Complete Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-complete-api-phrasing-overlay/)
- [Anthropic Complete Overlay](https://apis.io/overlays/anthropic/anthropic-complete-overlay/)
- [Anthropic Cost Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-cost-api-phrasing-overlay/)
- [Anthropic Cost Overlay](https://apis.io/overlays/anthropic/anthropic-cost-overlay/)
- [Anthropic Deployment Runs Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-deployment-runs-api-phrasing-overlay/)
- [Anthropic Deployment Runs Beta True Overlay](https://apis.io/overlays/anthropic/anthropic-deployment-runs-beta-true-overlay/)
- [Anthropic Deployment Runs Overlay](https://apis.io/overlays/anthropic/anthropic-deployment-runs-overlay/)
- [Anthropic Deployments Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-deployments-api-phrasing-overlay/)
- [Anthropic Deployments Beta True Overlay](https://apis.io/overlays/anthropic/anthropic-deployments-beta-true-overlay/)
- [Anthropic Deployments Overlay](https://apis.io/overlays/anthropic/anthropic-deployments-overlay/)
- [Anthropic Dreams Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-dreams-api-phrasing-overlay/)
- [Anthropic Dreams Beta True Overlay](https://apis.io/overlays/anthropic/anthropic-dreams-beta-true-overlay/)
- [Anthropic Dreams Overlay](https://apis.io/overlays/anthropic/anthropic-dreams-overlay/)
- [Anthropic Environments Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-environments-api-phrasing-overlay/)
- [Anthropic Environments Beta True Overlay](https://apis.io/overlays/anthropic/anthropic-environments-beta-true-overlay/)
- [Anthropic Environments Overlay](https://apis.io/overlays/anthropic/anthropic-environments-overlay/)
- [Anthropic Events Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-events-api-phrasing-overlay/)
- [Anthropic Events Overlay](https://apis.io/overlays/anthropic/anthropic-events-overlay/)
- [Anthropic Files Api Phrasing Overlay](https://apis.io/overlays/anthropic/anthropic-files-api-phrasing-overlay/)
- …and 46 more published on APIs.io

#### Governance rules (4)

Spectral rulesets for the provider's contracts.

- [Anthropic — asyncapi rules](https://apis.io/rules/anthropic/anthropic-asyncapi-spectral-rules/)
- [Anthropic — jsonschema rules](https://apis.io/rules/anthropic/anthropic-jsonschema-spectral-rules/)
- [Anthropic API Rules](https://apis.io/rules/anthropic/anthropic-rules/)
- [Anthropic API Rules](https://apis.io/rules/anthropic/anthropic-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Anthropic Authentication](https://apis.io/security/anthropic/anthropic-authentication/)
- [Anthropic Domain Security](https://apis.io/security/anthropic/anthropic-domain-security/)
- [Anthropic Trust Center](https://apis.io/security/anthropic/anthropic-trust-center/)
- [Anthropic Vulnerability Disclosure](https://apis.io/security/anthropic/anthropic-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Anthropic Plans Pricing](https://apis.io/plans/anthropic/anthropic-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Anthropic Rate Limits](https://apis.io/rate-limits/anthropic/anthropic-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Anthropic Finops](https://apis.io/finops/anthropic/anthropic-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.anthropic.com/)
- [Documentation](https://github.com/anthropics/anthropic-quickstarts)
- [Getting started](https://docs.anthropic.com/en/docs/get-started)
- [API reference](https://platform.claude.com/docs/en/api/overview)
- [Pricing](https://claude.com/pricing)
- [Support](https://support.claude.com/en/collections/4078531-api)
- [Changelog](https://platform.claude.com/docs/en/release-notes/overview)
- [Blog](https://www.anthropic.com/news)
- [Trust centre](https://trust.anthropic.com/)
- [Terms of service](https://www.anthropic.com/legal/aup)
- [Privacy policy](https://www.anthropic.com/legal/privacy)
- [GitHub](https://github.com/anthropics)
- [Status](https://status.anthropic.com/)

## API Evangelist rating

**Kin Score 89.0** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 82.1 |
| Contract quality | 70.9 |
| Contract governance | 35.6 |
| Operational transparency | 100.0 |
| Developer ergonomics | 96.4 |
| Access clarity | 100.0 |

**Agent readiness 47.6** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | yes |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | — |

**Regulatory alignment 40.0** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/anthropic/](https://apis.io/providers/anthropic/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Anthropic: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/anthropic/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
