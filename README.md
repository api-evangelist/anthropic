# Anthropic (anthropic)
Anthropic is an AI safety company and creator of the Claude family of large language models (Opus, Sonnet, Haiku). The Claude API provides access to Claude models for text generation, vision, tool use, extended thinking, batch processing, and agentic workflows including managed agents, skills, memory, compaction, and computer use. Anthropic also publishes the open Model Context Protocol (MCP) for standardized AI tool integration and ships Claude Code, the terminal-based agentic coding tool.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, Claude, Foundation Models, Large Language Models, Machine Learning, MCP, Agents

## Timestamps

- **Created:** 2025-08-14
- **Modified:** 2026-05-22

## Models

| Model | API ID | Context | Max Output | Input $/MTok | Output $/MTok |
|---|---|---|---|---|---|
| Claude Opus 4.7 (latest) | `claude-opus-4-7` | 1M tokens | 128k | $5 | $25 |
| Claude Sonnet 4.6 | `claude-sonnet-4-6` | 1M tokens | 64k | $3 (<200k) / $6 (>200k) | $15 / $22.50 |
| Claude Haiku 4.5 | `claude-haiku-4-5` | 200k tokens | 64k | $1 | $5 |
| Claude Opus 4.6 (legacy) | `claude-opus-4-6` | 1M tokens | 128k | $5 | $25 |
| Claude Opus 4.5 (legacy) | `claude-opus-4-5` | 200k tokens | 64k | $5 | $25 |
| Claude Sonnet 4.5 (legacy) | `claude-sonnet-4-5` | 200k tokens | 64k | $3 | $15 |
| Claude Opus 4.1 (legacy) | `claude-opus-4-1` | 200k tokens | 32k | $15 | $75 |
| Claude Sonnet 4 (deprecated, retires 2026-06-15) | `claude-sonnet-4-0` | 200k tokens | 64k | $3 | $15 |
| Claude Opus 4 (deprecated, retires 2026-06-15) | `claude-opus-4-0` | 200k tokens | 32k | $15 | $75 |

## APIs

### Anthropic Messages API
Send a structured list of input messages with text and/or image content; the model returns the next message. Supports text, images, tool use, extended thinking, streaming, structured outputs, prompt caching, server-side compaction, and the advisor tool.

**Human URL:** [https://docs.anthropic.com/en/api/messages](https://docs.anthropic.com/en/api/messages)

- [Documentation](https://docs.anthropic.com/en/api/messages)
- [Documentation — Streaming](https://docs.anthropic.com/en/api/messages-streaming)
- [OpenAPI](openapi/anthropic-messages-api-openapi.yml)
- [JSON Schema — Message](json-schema/anthropic-message-schema.json)
- [JSON Schema — Tool Use](json-schema/anthropic-tool-use-schema.json)
- [JSON-LD](json-ld/anthropic-context.jsonld)
- [Naftiko Capability — Messages](capabilities/messages-messages.yaml)

### Anthropic Models API
List and inspect Claude models. Returns `max_input_tokens`, `max_tokens`, and a `capabilities` object per model so clients can discover model properties programmatically.

**Human URL:** [https://docs.anthropic.com/en/api/models-list](https://docs.anthropic.com/en/api/models-list)

- [OpenAPI](openapi/anthropic-models-api-openapi.yml)
- [Naftiko Capability — Models](capabilities/models-models.yaml)
- [Naftiko Capability — Messages binding](capabilities/models-messages.yaml)
- [Naftiko Capability — Tokens binding](capabilities/models-tokens.yaml)

### Anthropic Message Batches API
Batch Messages requests at 50% off both input and output tokens. Batches can take up to 24 hours; up to 300k output tokens per request on Opus 4.6/4.7 and Sonnet 4.6 with the `output-300k-2026-03-24` beta header.

**Human URL:** [https://docs.anthropic.com/en/api/creating-message-batches](https://docs.anthropic.com/en/api/creating-message-batches)

- [OpenAPI](openapi/anthropic-message-batches-api-openapi.yml)
- [Naftiko Capability — Message Batches](capabilities/message-batches-message-batches.yaml)

### Anthropic Files API
Upload-once / reuse-many file management for Messages, Batches, code execution, and Managed Agents. 500 MB request limit.

**Human URL:** [https://docs.anthropic.com/en/api/files-create](https://docs.anthropic.com/en/api/files-create)

- [OpenAPI](openapi/anthropic-files-api-openapi.yml)
- [Naftiko Capability — Files](capabilities/files-files.yaml)

### Anthropic Admin API
Manage organization info, members, invites, workspaces, workspace members, and API keys. Requires an Admin API key (`sk-ant-admin...`).

**Human URL:** [https://docs.anthropic.com/en/api/admin-api/users/get-user](https://docs.anthropic.com/en/api/admin-api/users/get-user)

- [OpenAPI](openapi/anthropic-admin-api-openapi.yml)
- [Naftiko Capability — API Keys](capabilities/admin-api-keys.yaml)
- [Naftiko Capability — Organization](capabilities/admin-organization.yaml)
- [Naftiko Capability — Organization Invites](capabilities/admin-organization-invites.yaml)
- [Naftiko Capability — Organization Members](capabilities/admin-organization-members.yaml)
- [Naftiko Capability — Workspaces](capabilities/admin-workspaces.yaml)
- [Naftiko Capability — Workspace Members](capabilities/admin-workspace-members.yaml)

### Anthropic Prompts API
Generate, improve, and templatize prompts. Backs the Console Prompt Generator and the Workbench prompt authoring workflow.

**Human URL:** [https://docs.anthropic.com/en/api/prompt-tools-generate](https://docs.anthropic.com/en/api/prompt-tools-generate)

- [OpenAPI](openapi/anthropic-prompts-api-openapi.yml)
- [Naftiko Capability — Prompt Generation](capabilities/prompts-prompt-generation.yaml)
- [Naftiko Capability — Prompt Improvement](capabilities/prompts-prompt-improvement.yaml)
- [Naftiko Capability — Prompt Templatization](capabilities/prompts-prompt-templatization.yaml)

### Anthropic Token Counting API
Count input tokens for any Messages request shape (including tools, images, and documents) without creating it. Free; subject to RPM rate limits.

**Human URL:** [https://docs.anthropic.com/en/api/messages-count-tokens](https://docs.anthropic.com/en/api/messages-count-tokens)

- [OpenAPI](openapi/anthropic-token-counting-api-openapi.yml)
- [Naftiko Capability — Token Counting](capabilities/token-counting-tokens.yaml)

### Anthropic Skills API (beta)
Create and manage custom Agent Skills — filesystem-based directories of instructions, scripts, and resources that Claude loads on demand via progressive disclosure. Workspace-wide sharing. Requires the `skills-2025-10-02` beta header.

**Human URL:** [https://docs.anthropic.com/en/api/skills/create-skill](https://docs.anthropic.com/en/api/skills/create-skill)

- [OpenAPI](openapi/anthropic-skills-api-openapi.yml)
- [Naftiko Capability — Skills](capabilities/skills-skills.yaml)

### Anthropic Usage and Cost API
Programmatic access to token consumption (`/v1/organizations/usage_report/messages`) and USD service-level cost breakdowns (`/v1/organizations/cost_report`) for FinOps reporting. Admin API key required.

**Human URL:** [https://docs.anthropic.com/en/api/usage-cost-api](https://docs.anthropic.com/en/api/usage-cost-api)

- [OpenAPI](openapi/anthropic-usage-cost-api-openapi.yml)
- [Naftiko Capability — Usage and Cost Reporting](capabilities/usage-cost-reporting.yaml)

### Anthropic Claude Code Analytics API
Daily aggregated user-level Claude Code productivity metrics — sessions, lines of code, commits, pull requests, tool actions, and estimated costs by model — via `/v1/organizations/usage_report/claude_code`. Admin API key required.

**Human URL:** [https://docs.anthropic.com/en/api/claude-code-analytics-api](https://docs.anthropic.com/en/api/claude-code-analytics-api)

- [OpenAPI](openapi/anthropic-claude-code-analytics-api-openapi.yml)
- [Naftiko Capability — Claude Code Analytics](capabilities/claude-code-analytics.yaml)

### Anthropic Managed Agents API (beta)
Fully managed agent harness — define versioned `Agents`, configure `Environments` (cloud container or self-hosted sandbox), and run stateful `Sessions` driven by user events with SSE streaming, vault-managed OAuth credentials, multiagent sessions, MCP tunnels (research preview), and Memory. Requires the `managed-agents-2026-04-01` beta header.

**Human URL:** [https://platform.claude.com/docs/en/managed-agents/overview](https://platform.claude.com/docs/en/managed-agents/overview)

- [OpenAPI](openapi/anthropic-managed-agents-api-openapi.yml)
- [Naftiko Capability — Agents](capabilities/managed-agents-agents.yaml)
- [Naftiko Capability — Sessions](capabilities/managed-agents-sessions.yaml)
- [Naftiko Capability — Environments](capabilities/managed-agents-environments.yaml)

## Common Properties

- [Portal — anthropic.com](https://www.anthropic.com)
- [Portal — Claude Console](https://platform.claude.com/)
- [Documentation — docs.anthropic.com](https://docs.anthropic.com/)
- [Documentation — platform.claude.com](https://platform.claude.com/docs/)
- [GettingStarted](https://docs.anthropic.com/en/api/getting-started)
- [Pricing](https://www.anthropic.com/pricing)
- [GitHubOrganization](https://github.com/anthropics)
- [StatusPage](https://status.anthropic.com)
- [Blog — News](https://www.anthropic.com/news)
- [Blog — Engineering](https://www.anthropic.com/engineering)
- [SignUp](https://console.anthropic.com/)
- [Sandbox — Workbench](https://platform.claude.com/workbench)
- [TrustCenter](https://trust.anthropic.com/)
- [TermsOfService](https://www.anthropic.com/legal/aup)
- [PrivacyPolicy](https://www.anthropic.com/legal/privacy)
- [SDK — Python](https://github.com/anthropics/anthropic-sdk-python)
- [SDK — TypeScript](https://github.com/anthropics/anthropic-sdk-typescript)
- [SDK — Java](https://github.com/anthropics/anthropic-sdk-java)
- [SDK — Go](https://github.com/anthropics/anthropic-sdk-go)
- [SDK — Ruby](https://github.com/anthropics/anthropic-sdk-ruby)
- [SDK — C#](https://github.com/anthropics/anthropic-sdk-csharp)
- [SDK — PHP](https://github.com/anthropics/anthropic-sdk-php)
- [SDK — Claude Agent SDK (Python)](https://github.com/anthropics/claude-agent-sdk-python)
- [SDK — Claude Code](https://github.com/anthropics/claude-code)
- [SDK — `ant` CLI](https://docs.anthropic.com/en/api/sdks/cli)
- [Tool — Claude Code GitHub Action](https://github.com/anthropics/claude-code-action)
- [Tool — Public Skills repository](https://github.com/anthropics/skills)
- [CodeExamples — Claude Cookbooks](https://github.com/anthropics/claude-cookbooks)
- [Courses — Anthropic Courses](https://github.com/anthropics/courses)
- [Courses — Prompt Engineering Interactive Tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial)
- [Plugins — Official Claude Plugins](https://github.com/anthropics/claude-plugins-official)
- [Plugins — Knowledge Work Plugins](https://github.com/anthropics/knowledge-work-plugins)
- [Documentation — Model Context Protocol](https://modelcontextprotocol.io)
- [Models](https://docs.anthropic.com/en/docs/about-claude/models/all-models)
- [RateLimits](https://docs.anthropic.com/en/api/rate-limits)
- [Forum — Discord](https://discord.com/invite/6PPFFzqPDZ)
- [Postman Workspace](https://www.postman.com/postman/anthropic-apis/overview)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Anthropic Messages API](openapi/anthropic-messages-api-openapi.yml)
- [Anthropic Models API](openapi/anthropic-models-api-openapi.yml)
- [Anthropic Message Batches API](openapi/anthropic-message-batches-api-openapi.yml)
- [Anthropic Files API](openapi/anthropic-files-api-openapi.yml)
- [Anthropic Admin API](openapi/anthropic-admin-api-openapi.yml)
- [Anthropic Prompts API](openapi/anthropic-prompts-api-openapi.yml)
- [Anthropic Token Counting API](openapi/anthropic-token-counting-api-openapi.yml)
- [Anthropic Skills API](openapi/anthropic-skills-api-openapi.yml)
- [Anthropic Usage and Cost API](openapi/anthropic-usage-cost-api-openapi.yml)
- [Anthropic Claude Code Analytics API](openapi/anthropic-claude-code-analytics-api-openapi.yml)
- [Anthropic Managed Agents API](openapi/anthropic-managed-agents-api-openapi.yml)

### JSON Schema

- [Anthropic Message Schema](json-schema/anthropic-message-schema.json)
- [Anthropic Tool Use Schema](json-schema/anthropic-tool-use-schema.json)

### JSON-LD

- [Anthropic Context](json-ld/anthropic-context.jsonld)

### Capabilities (Naftiko)

- [Messages](capabilities/messages-messages.yaml)
- [Models](capabilities/models-models.yaml)
- [Models — Messages binding](capabilities/models-messages.yaml)
- [Models — Tokens binding](capabilities/models-tokens.yaml)
- [Message Batches](capabilities/message-batches-message-batches.yaml)
- [Files](capabilities/files-files.yaml)
- [Token Counting](capabilities/token-counting-tokens.yaml)
- [Skills](capabilities/skills-skills.yaml)
- [Usage and Cost Reporting](capabilities/usage-cost-reporting.yaml)
- [Claude Code Analytics](capabilities/claude-code-analytics.yaml)
- [Managed Agents — Agents](capabilities/managed-agents-agents.yaml)
- [Managed Agents — Sessions](capabilities/managed-agents-sessions.yaml)
- [Managed Agents — Environments](capabilities/managed-agents-environments.yaml)
- [Admin — API Keys](capabilities/admin-api-keys.yaml)
- [Admin — Organization](capabilities/admin-organization.yaml)
- [Admin — Organization Invites](capabilities/admin-organization-invites.yaml)
- [Admin — Organization Members](capabilities/admin-organization-members.yaml)
- [Admin — Workspaces](capabilities/admin-workspaces.yaml)
- [Admin — Workspace Members](capabilities/admin-workspace-members.yaml)
- [Prompts — Generation](capabilities/prompts-prompt-generation.yaml)
- [Prompts — Improvement](capabilities/prompts-prompt-improvement.yaml)
- [Prompts — Templatization](capabilities/prompts-prompt-templatization.yaml)

### Commercial artifacts

- [Plans / Pricing](plans/anthropic-plans-pricing.yml)
- [Rate Limits](rate-limits/anthropic-rate-limits.yml)
- [FinOps Definition](finops/anthropic-finops.yml)

### Blogs

Recent Anthropic news and engineering posts mirrored under [blogs/](blogs/).

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
