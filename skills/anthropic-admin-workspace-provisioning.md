---
name: anthropic-admin-workspace-provisioning
description: Provision an Anthropic workspace, invite an organization member, and grant them workspace access using the Admin API.
api: Anthropic Admin API
operations:
  - createWorkspace
  - listWorkspaces
  - getWorkspace
  - updateWorkspace
  - archiveWorkspace
  - createOrganizationInvite
  - listOrganizationInvites
  - deleteOrganizationInvite
  - listOrganizationMembers
  - addWorkspaceMember
  - updateWorkspaceMember
  - removeWorkspaceMember
  - listApiKeys
  - updateApiKey
generated: '2026-08-27'
method: generated
source: openapi/anthropic-workspaces-api-openapi.yml, openapi/anthropic-workspace-members-api-openapi.yml, openapi/anthropic-organization-invites-api-openapi.yml, openapi/anthropic-organization-members-api-openapi.yml, openapi/anthropic-api-keys-api-openapi.yml
---

# Provision a workspace and onboard a member

## Preconditions

- This is the **Admin API**. It requires an Admin API key (`sk-ant-admin...`),
  not a normal Claude API key, in the `x-api-key` header. A normal key returns
  an authentication error on every operation below.
- Base URL `https://api.anthropic.com`; Admin paths sit under
  `/organizations/...`.

## Steps

1. **Check what exists** — `listWorkspaces`
   (`GET /organizations/workspaces`). Workspace names are not unique, so search
   before creating or you will make a duplicate.
2. **Create the workspace** — `createWorkspace`
   (`POST /organizations/workspaces`). Keep the `wrkspc_`-prefixed id.
3. **Invite the person** — `createOrganizationInvite`
   (`POST /organizations/invites`) with their email and org role.
   `listOrganizationInvites` shows what is outstanding.
4. **Wait for acceptance** — a pending invite has no user id yet. Poll
   `listOrganizationMembers` (`GET /organizations/users`) until the user
   appears; only then can you add them to a workspace.
5. **Grant workspace access** — `addWorkspaceMember`
   (`POST /organizations/workspaces/{workspace_id}/members`) with the
   `user_id` and workspace role. `updateWorkspaceMember` changes the role later.
6. **Attribute the keys** — `listApiKeys` (`GET /organizations/api_keys`) shows
   which keys resolve to which workspace. `updateApiKey` can rename or disable
   one. Keys cannot be created over the API; that is Console-only.

## Reversal

Each step has a distinct reversal, and they are not equivalent:

- `deleteOrganizationInvite` — revokes an invite **before** it is accepted.
  After acceptance there is no invite left to delete; remove the member instead.
- `removeWorkspaceMember` (`DELETE .../members/{user_id}`) — revokes workspace
  access. The user stays in the organization.
- `removeOrganizationMember` (`DELETE /organizations/users/{user_id}`) — removes
  them from the organization entirely.
- `archiveWorkspace` (`POST /organizations/workspaces/{workspace_id}/archive`) —
  the soft path for a workspace. Anthropic's docs do not state an un-archive
  window, so treat archive as one-way unless you have confirmed otherwise.

No published window applies to any of these; none is time-boxed and none is
documented as restorable. Do not tell a user an action is undoable here.

## Conventions

Cursor pagination (`before_id`/`after_id`/`limit`, with
`has_more`/`first_id`/`last_id`). No idempotency key: a retried
`createWorkspace` creates a second workspace. See
`conventions/anthropic-conventions.yml`.
