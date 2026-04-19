# Anthropic (anthropic)
Anthropic is an AI safety company and creator of the Claude family of large language models. The Anthropic API provides access to Claude models for text generation, vision, tool use, extended thinking, batch processing, and agentic workflows. Anthropic also publishes the Model Context Protocol (MCP) for standardized AI tool integration.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - AI, Artificial Intelligence, Claude, Foundation Models, Large Language Models, Machine Learning

## Timestamps

- **Created:** 2025-08-14
- **Modified:** 2026-04-19

## APIs

### Anthropic Messages API
Send a structured list of input messages with text and/or image content, and the model will generate the next message in the conversation. Supports text, images, tool use, extended thinking, streaming, and structured output.

**Human URL:** [https://docs.anthropic.com/en/api/messages](https://docs.anthropic.com/en/api/messages)

#### Tags:

 - AI, Artificial Intelligence, Messages

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/messages)
- [Documentation](https://docs.anthropic.com/en/api/messages-streaming)
- [OpenAPI](openapi/anthropic-messages-api-openapi.yml)
- [JSONSchema](json-schema/anthropic-message-schema.json)
- [JSONSchema](json-schema/anthropic-tool-use-schema.json)
- [JSONLD](json-ld/anthropic-context.jsonld)

### Anthropic Models API
List and retrieve available Claude models via the Models API.

**Human URL:** [https://docs.anthropic.com/en/api/models-list](https://docs.anthropic.com/en/api/models-list)

#### Tags:

 - AI, Artificial Intelligence, Models

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/models-list)
- [OpenAPI](openapi/anthropic-models-api-openapi.yml)

### Anthropic Message Batches API
Process multiple Messages API requests at once with the Message Batches API. Batches can take up to 24 hours to complete and offer significant cost savings.

**Human URL:** [https://docs.anthropic.com/en/api/creating-message-batches](https://docs.anthropic.com/en/api/creating-message-batches)

#### Tags:

 - AI, Artificial Intelligence, Batches, Messages

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/creating-message-batches)
- [OpenAPI](openapi/anthropic-message-batches-api-openapi.yml)

### Anthropic Files API
Upload and manage files to use with the Anthropic API without re-uploading content with each request.

**Human URL:** [https://docs.anthropic.com/en/api/files-create](https://docs.anthropic.com/en/api/files-create)

#### Tags:

 - AI, Artificial Intelligence, Files

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/files-create)
- [OpenAPI](openapi/anthropic-files-api-openapi.yml)

### Anthropic Admin API
Manage administrative functions for Anthropic API organizations including users, API keys, and workspaces.

**Human URL:** [https://docs.anthropic.com/en/api/admin-api/users/get-user](https://docs.anthropic.com/en/api/admin-api/users/get-user)

#### Tags:

 - Administrative, AI, Artificial Intelligence

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/admin-api/users/get-user)
- [OpenAPI](openapi/anthropic-admin-api-openapi.yml)

### Anthropic Prompts API
Create and manage prompts in the Anthropic prompt library.

**Human URL:** [https://docs.anthropic.com/en/api/prompt-tools-generate](https://docs.anthropic.com/en/api/prompt-tools-generate)

#### Tags:

 - AI, Artificial Intelligence, Prompts

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/prompt-tools-generate)
- [OpenAPI](openapi/anthropic-prompts-api-openapi.yml)

### Anthropic Token Counting API
Count the number of tokens in a Message, including tools, images, and documents, without creating it. Free to use.

**Human URL:** [https://docs.anthropic.com/en/api/messages-count-tokens](https://docs.anthropic.com/en/api/messages-count-tokens)

#### Tags:

 - AI, Artificial Intelligence, Counting, Tokens

#### Properties

- [Documentation](https://docs.anthropic.com/en/api/messages-count-tokens)

## Common Properties

- [Portal](https://www.anthropic.com)
- [Documentation](https://docs.anthropic.com/)
- [GettingStarted](https://docs.anthropic.com/en/api/getting-started)
- [Pricing](https://www.anthropic.com/pricing)
- [GitHubOrganization](https://github.com/anthropics)
- [StatusPage](https://status.anthropic.com)
- [Blog](https://www.anthropic.com/news)
- [SignUp](https://console.anthropic.com/)
- [Sandbox](https://console.anthropic.com/workbench)
- [TrustCenter](https://trust.anthropic.com/)
- [TermsOfService](https://www.anthropic.com/legal/aup)
- [PrivacyPolicy](https://www.anthropic.com/legal/privacy)
- [SDK — Python SDK](https://github.com/anthropics/anthropic-sdk-python)
- [SDK — TypeScript SDK](https://github.com/anthropics/anthropic-sdk-typescript)
- [SDK — Java SDK](https://github.com/anthropics/anthropic-sdk-java)
- [SDK — Go SDK](https://github.com/anthropics/anthropic-sdk-go)
- [Models](https://docs.anthropic.com/en/docs/about-claude/models/all-models)
- [Forum](https://discord.com/invite/6PPFFzqPDZ)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Anthropic Messages API](openapi/anthropic-messages-api-openapi.yml)
- [Anthropic Models API](openapi/anthropic-models-api-openapi.yml)
- [Anthropic Message Batches API](openapi/anthropic-message-batches-api-openapi.yml)
- [Anthropic Files API](openapi/anthropic-files-api-openapi.yml)
- [Anthropic Admin API](openapi/anthropic-admin-api-openapi.yml)
- [Anthropic Prompts API](openapi/anthropic-prompts-api-openapi.yml)

### JSON Schema

- [Anthropic Message Schema](json-schema/anthropic-message-schema.json)
- [Anthropic Tool Use Schema](json-schema/anthropic-tool-use-schema.json)

### JSON-LD

- [Anthropic Context](json-ld/anthropic-context.jsonld)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
