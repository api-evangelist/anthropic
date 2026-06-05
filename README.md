# Anthropic (anthropic)

Anthropic is an AI safety company and creator of the Claude family of large language models (Opus, Sonnet, Haiku). The Claude API provides access to Claude models for text generation, vision, tool use, extended thinking, batch processing, and agentic workflows including managed agents, skills, memory, compaction, and computer use. Anthropic also publishes the open Model Context Protocol (MCP) for standardized AI tool integration and ships Claude Code, the terminal-based agentic coding tool.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Claude
- Foundation Models
- Large Language Models
- Machine Learning
- MCP
- Agents

## Timestamps

- **Created:** 2025-08-14T00:00:00.000Z
- **Modified:** 2026-05-29

## APIs

### Anthropic Messages API

Send a structured list of input messages with text and/or image content, and the model will generate the next message in the conversation. The Messages API supports text, images, tool use, extended thinking, streaming, structured outputs, prompt caching, compaction, and the new advisor tool for pairing executor and higher-intelligence advisor models.

- **Human URL:** [https://docs.anthropic.com/en/api/messages](https://docs.anthropic.com/en/api/messages)

#### Tags

- AI
- Artificial Intelligence
- Messages

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/messages)
- [Documentation](https://docs.anthropic.com/en/api/messages-streaming)
- [OpenAPI](openapi/anthropic-messages-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-messages-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-messages-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/anthropic-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/anthropic-message-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/anthropic-tool-use-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/anthropic-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Anthropic Models API

List and inspect Claude models including Opus 4.7, Sonnet 4.6, and Haiku 4.5. The response includes max_input_tokens, max_tokens, and a capabilities object for every model so clients can discover model properties programmatically.

- **Human URL:** [https://docs.anthropic.com/en/api/models-list](https://docs.anthropic.com/en/api/models-list)

#### Tags

- AI
- Artificial Intelligence
- Models

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/models-list)
- [OpenAPI](openapi/anthropic-models-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-models-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-models-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Message Batches API

Send a batch of Message creation requests at 50% off both input and output tokens. Batches can take up to 24 hours to complete. Supports up to 300k output tokens per request on Opus 4.6/4.7 and Sonnet 4.6 with the output-300k-2026-03-24 beta header.

- **Human URL:** [https://docs.anthropic.com/en/api/creating-message-batches](https://docs.anthropic.com/en/api/creating-message-batches)

#### Tags

- AI
- Artificial Intelligence
- Batches
- Messages

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/creating-message-batches)
- [OpenAPI](openapi/anthropic-message-batches-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-message-batches-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-message-batches-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Files API

The Files API lets you upload and manage files for reuse across Messages, Batches, code execution, and Managed Agents without re-uploading content. 500 MB request limit; supports PDFs, images, Office documents, and plain text.

- **Human URL:** [https://docs.anthropic.com/en/api/files-create](https://docs.anthropic.com/en/api/files-create)

#### Tags

- AI
- Artificial Intelligence
- Files

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/files-create)
- [OpenAPI](openapi/anthropic-files-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-files-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-files-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Admin API

Programmatically manage administrative resources including organization info, members, invites, workspaces, workspace members, and API keys. Requires an Admin API key (sk-ant-admin...).

- **Human URL:** [https://docs.anthropic.com/en/api/admin-api/users/get-user](https://docs.anthropic.com/en/api/admin-api/users/get-user)

#### Tags

- Administrative
- AI
- Artificial Intelligence

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/admin-api/users/get-user)
- [OpenAPI](openapi/anthropic-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Prompts API

Prompt tools API for generating, improving, and templatizing prompts. Backs the Console Prompt Generator and integrates into the Workbench prompt authoring workflow.

- **Human URL:** [https://docs.anthropic.com/en/api/prompt-tools-generate](https://docs.anthropic.com/en/api/prompt-tools-generate)

#### Tags

- AI
- Artificial Intelligence
- Prompts

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/prompt-tools-generate)
- [OpenAPI](openapi/anthropic-prompts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-prompts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-prompts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Token Counting API

Count the number of tokens in a Message, including tools, images, and documents, without creating it. The Token Count API accepts the same structured list of inputs as Messages including system prompts, tools, images, and PDFs. Free to use but subject to requests-per-minute rate limits.

- **Human URL:** [https://docs.anthropic.com/en/api/messages-count-tokens](https://docs.anthropic.com/en/api/messages-count-tokens)

#### Tags

- AI
- Artificial Intelligence
- Counting
- Tokens

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/messages-count-tokens)
- [OpenAPI](openapi/anthropic-token-counting-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-token-counting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-token-counting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Skills API

Create and manage custom Agent Skills. Skills are filesystem-based directories of instructions, scripts, and resources that Claude loads on demand via progressive disclosure. Workspace-wide sharing. The Skills API is currently in beta and requires the skills-2025-10-02 beta header.

- **Human URL:** [https://docs.anthropic.com/en/api/skills/create-skill](https://docs.anthropic.com/en/api/skills/create-skill)

#### Tags

- Agents
- AI
- Artificial Intelligence
- Skills

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/skills/create-skill)
- [OpenAPI](openapi/anthropic-skills-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-skills-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-skills-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Usage and Cost API

Programmatically access your organization's API usage and cost data with the Usage & Cost Admin API. The Usage API tracks token consumption with breakdowns by model, workspace, and service tier via /v1/organizations/usage_report/messages. The Cost API retrieves service-level USD breakdowns via /v1/organizations/cost_report. Requires an Admin API key.

- **Human URL:** [https://docs.anthropic.com/en/api/usage-cost-api](https://docs.anthropic.com/en/api/usage-cost-api)

#### Tags

- Administration
- AI
- Artificial Intelligence
- Cost
- Usage
- FinOps

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/usage-cost-api)
- [OpenAPI](openapi/anthropic-usage-cost-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-usage-cost-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-usage-cost-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Claude Code Analytics API

Daily aggregated user-level Claude Code productivity metrics — sessions, lines of code, commits, pull requests, tool actions, and estimated costs by model — via /v1/organizations/usage_report/claude_code. Requires an Admin API key.

- **Human URL:** [https://docs.anthropic.com/en/api/claude-code-analytics-api](https://docs.anthropic.com/en/api/claude-code-analytics-api)

#### Tags

- Administration
- AI
- Analytics
- Artificial Intelligence
- Claude Code
- Productivity

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/claude-code-analytics-api)
- [OpenAPI](openapi/anthropic-claude-code-analytics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-claude-code-analytics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-claude-code-analytics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Anthropic Managed Agents API

Claude Managed Agents — a fully managed agent harness for running Claude as an autonomous agent with secure sandboxing, built-in tools (bash, file ops, web search/fetch, MCP), SSE streaming, vault-managed OAuth credentials, multiagent sessions, and self-hosted sandbox option. Three resources — Agents, Sessions, Environments — plus event streaming. Currently in public beta under the managed-agents-2026-04-01 header.

- **Human URL:** [https://platform.claude.com/docs/en/managed-agents/overview](https://platform.claude.com/docs/en/managed-agents/overview)

#### Tags

- Agents
- AI
- Artificial Intelligence
- Beta
- Managed Agents
- Sessions
- Environments

#### Properties

- [Documentation](https://platform.claude.com/docs/en/managed-agents/overview)
- [Documentation](https://platform.claude.com/docs/en/managed-agents/agent-setup)
- [Documentation](https://platform.claude.com/docs/en/managed-agents/sessions)
- [Documentation](https://platform.claude.com/docs/en/managed-agents/environments)
- [OpenAPI](openapi/anthropic-managed-agents-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/anthropic-managed-agents-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/anthropic-managed-agents-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [LinkedIn](https://www.linkedin.com/company/anthropicresearch)
- [Documentation](https://github.com/anthropics/anthropic-quickstarts)
- [Portal](https://platform.claude.com/docs/en/home)
- [Documentation](https://docs.anthropic.com/en/api/messages)
- [Status Page](https://status.anthropic.com/)
- [Changelog](https://platform.claude.com/docs/en/release-notes/api)
- [Documentation](https://platform.claude.com/login)
- [Rate Limits](https://docs.anthropic.com/en/api/rate-limits)
- [Tiers](https://docs.anthropic.com/en/api/service-tiers)
- [Errors](https://docs.anthropic.com/en/api/errors)
- [Documentation](https://docs.anthropic.com/en/api/client-sdks)
- [Versioning](https://docs.anthropic.com/en/api/versioning)
- [Regions](https://docs.anthropic.com/en/api/supported-regions)
- [Support](https://docs.anthropic.com/en/api/getting-help)
- [Plans](https://www.anthropic.com/pricing)
- [Pricing](https://www.anthropic.com/pricing#api)
- [Portal](https://www.anthropic.com/api)
- [Getting Started](https://docs.anthropic.com/en/docs/get-started)
- [Glossary](https://docs.anthropic.com/en/docs/about-claude/glossary)
- [Documentation](https://www.anthropic.com/legal/terms)
- [Privacy Policy](https://www.anthropic.com/legal/privacy)
- [Privacy Policy](https://privacy.claude.com/)
- [Status Page](https://status.anthropic.com)
- [Blog](https://www.anthropic.com/news)
- [Blog](https://www.anthropic.com/engineering)
- [Sign Up](https://console.anthropic.com/)
- [Sign Up](https://platform.claude.com/)
- [Sandbox](https://platform.claude.com/workbench)
- [Documentation](https://docs.anthropic.com/en/api/beta-headers)
- [Trust Center](https://trust.anthropic.com/)
- [Terms of Service](https://www.anthropic.com/legal/aup)
- [Documentation](https://docs.anthropic.com/en/api/administration-api)
- [Documentation](https://docs.anthropic.com/en/api/usage-cost-api)
- [Documentation](https://docs.anthropic.com/en/api/claude-code-analytics-api)
- [GitHub Organization](https://github.com/anthropics)
- [SDK](https://github.com/anthropics/anthropic-sdk-python)
- [SDK](https://github.com/anthropics/anthropic-sdk-typescript)
- [SDK](https://github.com/anthropics/anthropic-sdk-java)
- [SDK](https://github.com/anthropics/anthropic-sdk-go)
- [SDK](https://github.com/anthropics/anthropic-sdk-ruby)
- [SDK](https://github.com/anthropics/anthropic-sdk-csharp)
- [SDK](https://github.com/anthropics/anthropic-sdk-php)
- [SDK](https://github.com/anthropics/claude-agent-sdk-python)
- [Tool](https://github.com/anthropics/claude-code)
- [Tool](https://github.com/anthropics/claude-code-action)
- [Tool](https://github.com/anthropics/skills)
- [Code Examples](https://github.com/anthropics/claude-cookbooks)
- [Courses](https://github.com/anthropics/courses)
- [Courses](https://github.com/anthropics/prompt-eng-interactive-tutorial)
- [Plugins](https://github.com/anthropics/claude-plugins-official)
- [Code Examples](https://github.com/anthropics/financial-services)
- [Code Examples](https://github.com/anthropics/claude-for-legal)
- [Plugins](https://github.com/anthropics/knowledge-work-plugins)
- [Training](https://www.anthropic.com/learn)
- [Forum](https://discord.com/invite/6PPFFzqPDZ)
- [Documentation](https://www.postman.com/postman/anthropic-apis/overview)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/token-counting)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/data-residency)
- [Documentation](https://docs.anthropic.com/en/api/messages-streaming)
- [Documentation](https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/overview)
- [Documentation](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/citations)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/batch-processing)
- [Documentation](https://docs.anthropic.com/en/build-with-claude/compaction)
- [Documentation](https://docs.anthropic.com/en/agents-and-tools/agent-skills/overview)
- [Documentation](https://docs.anthropic.com/en/agents-and-tools/tool-use/memory-tool)
- [Documentation](https://docs.anthropic.com/en/api/openai-sdk)
- [Documentation](https://docs.anthropic.com/en/api/claude-on-amazon-bedrock)
- [Documentation](https://docs.anthropic.com/en/api/claude-on-vertex-ai)
- [Documentation](https://docs.anthropic.com/en/build-with-claude/claude-platform-on-aws)
- [Documentation](https://docs.anthropic.com/en/build-with-claude/claude-in-microsoft-foundry)
- [Models](https://docs.anthropic.com/en/docs/about-claude/models/all-models)
- [SDK](https://docs.anthropic.com/en/docs/claude-code/sdk)
- [SDK](https://docs.anthropic.com/en/api/sdks/cli)
- [Documentation](https://modelcontextprotocol.io)
- [GitHub Organization](https://github.com/modelcontextprotocol)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/structured-output)
- [Documentation](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Portal](https://www.anthropic.com)
- [Documentation](https://docs.anthropic.com/)
- [Documentation](https://platform.claude.com/docs/)
- [Getting Started](https://docs.anthropic.com/en/api/getting-started)
- [Plans](https://plans/anthropic-plans-pricing.yml)
- [Rate Limits](https://rate-limits/anthropic-rate-limits.yml)
- [Fin Ops](https://finops/anthropic-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
