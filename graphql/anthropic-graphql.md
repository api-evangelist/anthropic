# Anthropic GraphQL Schema

**Provider:** Anthropic  
**Source API:** Anthropic Claude API (REST)  
**Docs:** https://docs.anthropic.com/en/api/  
**GitHub:** https://github.com/anthropics  
**Schema file:** anthropic-schema.graphql  
**Schema source:** conceptual  

## Overview

This GraphQL schema is a conceptual representation of the Anthropic Claude API derived from the REST API surface. The Anthropic API provides access to Claude large language models for text generation, vision, tool use, extended thinking, batch processing, prompt caching, and agentic workflows including managed agents, skills, memory, compaction, and computer use.

The REST API is organized around several resource groups:

- **Messages API** — send structured input messages; receive text, tool use, or thinking blocks; supports streaming via SSE
- **Models API** — list and inspect available Claude models and their capabilities
- **Message Batches API** — submit and retrieve batches of message requests at reduced cost
- **Files API** — upload and reuse files across messages, batches, and managed agents
- **Admin API** — manage organization members, workspaces, API keys, invites, and roles
- **Prompts API** — generate, improve, and templatize prompts
- **Token Counting API** — count tokens for a prompt without creating a message
- **Skills API (beta)** — create and manage custom agent skills
- **Managed Agents API (beta)** — run Claude as an autonomous agent with sessions and environments
- **Usage and Cost API** — retrieve organization-level token usage and cost reports
- **Claude Code Analytics API** — daily aggregated Claude Code productivity metrics

## Types (62 named types)

| Type | Category | Description |
|------|----------|-------------|
| Message | Core | A complete message request/response object |
| MessageContent | Core | Union of content block types in a message |
| TextBlock | Content | A plain-text content block |
| ImageBlock | Content | An image content block with source reference |
| ToolUseBlock | Content | A block representing a tool call made by the model |
| ToolResultBlock | Content | A block carrying the result of a tool call |
| DocumentBlock | Content | A block referencing an uploaded document/file |
| ThinkingBlock | Content | An extended thinking reasoning block |
| Usage | Tokens | Token consumption counts for a request |
| InputTokens | Tokens | Breakdown of input token counts |
| OutputTokens | Tokens | Breakdown of output token counts |
| CacheReadTokens | Tokens | Tokens read from the prompt cache |
| CacheCreationTokens | Tokens | Tokens written into the prompt cache |
| Model | Models | A Claude model including ID, name, and capabilities |
| ModelInfo | Models | Detailed model metadata including context and output limits |
| ModelCapability | Models | A specific capability flag for a model |
| Capabilities | Models | Full capability set for a model |
| Feature | Models | A named feature supported by the API or a model |
| Completion | Core | A completed non-streaming response from the model |
| StreamEvent | Streaming | A server-sent event in a streaming response |
| MessageStart | Streaming | SSE event marking the start of a streamed message |
| ContentBlockStart | Streaming | SSE event marking the start of a content block |
| ContentBlockDelta | Streaming | SSE event carrying a delta within a content block |
| ContentBlockStop | Streaming | SSE event marking the end of a content block |
| MessageStop | Streaming | SSE event marking the end of a streamed message |
| Tool | Tools | A tool definition the model may invoke |
| ToolInput | Tools | The input schema for a tool |
| ToolChoice | Tools | How the model chooses which tool to call |
| ComputerTool | Tools | Built-in tool for browser and desktop automation |
| BashTool | Tools | Built-in tool for executing bash commands |
| TextEditorTool | Tools | Built-in tool for reading and editing files |
| SystemPrompt | Prompts | A system-level prompt prepended to a conversation |
| UserMessage | Messages | A message from the human turn |
| AssistantMessage | Messages | A message from the assistant turn |
| Conversation | Messages | An ordered list of messages forming a conversation |
| Batch | Batches | A message batch submission object |
| BatchResult | Batches | The result envelope for a completed batch |
| BatchError | Batches | An error returned at the batch level |
| BatchRequestError | Batches | An error returned for a single request within a batch |
| File | Files | A file uploaded to the Files API |
| FileSource | Files | The source reference for an image or document block |
| TokenCount | Counting | The token count result for a dry-run token count request |
| PromptCache | Caching | Prompt cache metadata and control settings |
| PromptCacheControl | Caching | Cache control breakpoint specifier |
| APIKey | Admin | An API key for a workspace or organization |
| Organization | Admin | An Anthropic organization account |
| Workspace | Admin | A workspace within an organization |
| Member | Admin | An organization or workspace member |
| Role | Admin | A named role (user, developer, workspace_admin, billing) |
| Permission | Admin | A fine-grained permission attached to a role |
| Invite | Admin | A pending organization invitation |
| InvoiceData | Billing | Invoice-level cost and usage summary |
| UsageReport | Billing | Token usage report broken down by model and workspace |
| CostReport | Billing | USD cost report broken down by service tier |
| Webhook | Webhooks | A registered webhook endpoint |
| WebhookEvent | Webhooks | A webhook payload delivered to a registered endpoint |
| BetaFeature | Beta | A named beta feature that can be activated via header |
| Skill | Skills | A custom agent skill definition |
| SkillResource | Skills | A resource file within a skill directory |
| Agent | ManagedAgents | A managed agent definition |
| Session | ManagedAgents | A managed agent session (run) |
| Environment | ManagedAgents | A sandboxed environment for managed agent execution |

## Queries

- `message(id: ID!)` — retrieve a message by ID
- `models` — list all available Claude models
- `model(id: ID!)` — retrieve a specific model
- `batches` — list message batches
- `batch(id: ID!)` — retrieve a batch by ID
- `batchResults(batchId: ID!)` — list results for a completed batch
- `files` — list uploaded files
- `file(id: ID!)` — retrieve a file by ID
- `countTokens(input: TokenCountInput!)` — count tokens for a prompt
- `organization` — retrieve organization metadata
- `members` — list organization members
- `workspaces` — list workspaces
- `workspace(id: ID!)` — retrieve a workspace
- `apiKeys` — list API keys
- `invites` — list pending invitations
- `usageReport(startDate: String!, endDate: String!)` — retrieve usage report
- `costReport(startDate: String!, endDate: String!)` — retrieve cost report
- `skills` — list agent skills
- `skill(id: ID!)` — retrieve a skill
- `agents` — list managed agents
- `agent(id: ID!)` — retrieve a managed agent
- `sessions(agentId: ID!)` — list sessions for an agent

## Mutations

- `createMessage(input: CreateMessageInput!)` — create a new message
- `createBatch(input: CreateBatchInput!)` — submit a message batch
- `cancelBatch(id: ID!)` — request cancellation of a batch
- `uploadFile(input: UploadFileInput!)` — upload a file
- `deleteFile(id: ID!)` — delete a file
- `generatePrompt(input: GeneratePromptInput!)` — generate a prompt
- `improvePrompt(input: ImprovePromptInput!)` — improve an existing prompt
- `createWorkspace(input: CreateWorkspaceInput!)` — create a workspace
- `addWorkspaceMember(input: WorkspaceMemberInput!)` — add a member to a workspace
- `inviteMember(input: InviteInput!)` — send an organization invite
- `createSkill(input: CreateSkillInput!)` — create an agent skill
- `createAgent(input: CreateAgentInput!)` — create a managed agent
- `createSession(agentId: ID!, input: CreateSessionInput!)` — start a managed agent session
