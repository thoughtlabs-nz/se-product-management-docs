# Aha.io Integration Skill

## Overview

The Aha.io Integration Skill provides full REST API integration for Paperclip agents to interact with Aha.io — the product management platform. This skill enables agents to read and write products, releases, features, epics, initiatives, goals, ideas, requirements, comments, to-dos, and more.

**Repository**: [thoughtlabs-nz/skill-aha](https://github.com/thoughtlabs-nz/skill-aha)

**Trigger Terms**: Aha, Aha.io, product roadmap, feature tracking, idea management, release planning, initiative tracking, roadmap updates, product-management workflow, Aha.io sync

---

## Environment Setup

Two environment variables are required:

| Variable | Purpose | Example |
|----------|---------|---------|
| `AHA_API_URL` | Base URL of your Aha.io account | `https://yourcompany.aha.io` |
| `AHA_API_KEY` | API key or OAuth2 bearer token | `xxxxxxxxxxxxxxxxxxxxxxxx` |

Generate an API key at `https://secure.aha.io/settings/api_keys`.

### Verify Connectivity

```bash
curl -sS "$AHA_API_URL/api/v1/me" \
  -H "Authorization: Bearer $AHA_API_KEY"
```

A 200 response with your user profile confirms the connection is live.

---

## Core Concepts

Aha.io organizes work hierarchically:

- **Products** — top-level workspaces (product lines)
- **Releases** — time-boxed delivery milestones
- **Epics** — large bodies of work spanning features
- **Features** — primary work items
- **Requirements** — sub-tasks within features
- **Initiatives** — strategic themes across products
- **Goals** — measurable business objectives
- **Ideas** — customer feedback from idea portals

Each resource has a **reference number** (e.g., `APP-1`, `APP-R-1`, `APP-E-1`).

---

## Common API Patterns

All requests use the base URL `$AHA_API_URL/api/v1` with the authorization header:

```
-H "Authorization: Bearer $AHA_API_KEY"
-H "Content-Type: application/json"
```

### Pagination

List endpoints return paginated results. Use `page` (1-indexed) and `per_page` (max 200):

```bash
curl -sS "$AHA_API_URL/api/v1/products/APP/features?page=2&per_page=100" \
  -H "Authorization: Bearer $AHA_API_KEY"
```

### Rate Limits

- 300 requests/minute
- 20 requests/second per account

If you hit 429, back off and retry.

---

## Quick Reference

### 1. List Products

```bash
curl -sS "$AHA_API_URL/api/v1/products" \
  -H "Authorization: Bearer $AHA_API_KEY"
```

### 2. Get Feature by Reference

```bash
curl -sS "$AHA_API_URL/api/v1/features/APP-123" \
  -H "Authorization: Bearer $AHA_API_KEY"
```

### 3. Create Feature

```bash
curl -sS -X POST "$AHA_API_URL/api/v1/releases/APP-R-1/features" \
  -H "Authorization: Bearer $AHA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "feature": {
      "name": "Agent-created feature",
      "workflow_status": "New",
      "description": "Created by Paperclip agent via API",
      "assigned_to_user": "user@example.com",
      "tags": "paperclip,automated"
    }
  }'
```

### 4. Update Feature

```bash
curl -sS -X PUT "$AHA_API_URL/api/v1/features/APP-123" \
  -H "Authorization: Bearer $AHA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "feature": {
      "workflow_status": "In progress",
      "description": "Updated by agent"
    }
  }'
```

### 5. Create Idea

```bash
curl -sS -X POST "$AHA_API_URL/api/v1/products/APP/ideas" \
  -H "Authorization: Bearer $AHA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "idea": {
      "name": "Customer request for dark mode",
      "description": "Multiple customers have requested this"
    }
  }'
```

### 6. Add Comment to Feature

```bash
curl -sS -X POST "$AHA_API_URL/api/v1/features/APP-123/comments" \
  -H "Authorization: Bearer $AHA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "comment": {
      "body": "Status update from Paperclip: work is on track."
    }
  }'
```

### 7. List Initiatives

```bash
curl -sS "$AHA_API_URL/api/v1/products/APP/initiatives" \
  -H "Authorization: Bearer $AHA_API_KEY"
```

### 8. Create To-Do

```bash
curl -sS -X POST "$AHA_API_URL/api/v1/features/APP-123/tasks" \
  -H "Authorization: Bearer $AHA_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "to_do": {
      "name": "Review API integration code",
      "due_date": "2026-05-01",
      "user": "user@example.com"
    }
  }'
```

---

## Paperclip ↔ Aha.io Sync Pattern

Workflow for syncing Paperclip issues with Aha.io features:

1. **Read the Paperclip issue** — extract title, description, status, assignee
2. **Search Aha.io** — check if a linked feature exists
3. **Create or update** — create new feature or update existing
4. **Comment** — post comment on Aha.io linking back to Paperclip issue
5. **Report back** — comment on Paperclip issue with Aha.io reference

For two-way sync, use Aha.io webhooks to trigger Paperclip heartbeats.

---

## Helper Script

A shell helper is available at `scripts/aha-api.sh`:

```bash
source "$(dirname "$0")/scripts/aha-api.sh"
aha_get "products"
aha_post "releases/APP-R-1/features" '{"feature":{"name":"New feature"}}'
```

Use `aha_json` for parsing responses (handles HTML control characters in descriptions):

```bash
aha_get "features/APP-123" | aha_json '.feature.name'
```

---

## Error Codes

| Code | Meaning |
|------|---------|
| 400 | Bad request — check payload |
| 403 | Auth failure — check API key |
| 404 | Not found |
| 429 | Rate limited — back off |
| 500 | Server error — contact support |
| 504 | Timeout — reduce page size |

---

## Quality Checklist

- [ ] `AHA_API_URL` and `AHA_API_KEY` set and connectivity confirmed
- [ ] Correct product prefix used (e.g., `APP`)
- [ ] Write operations include `Content-Type: application/json`
- [ ] Bulk operations use `?disable_mailers=true`
- [ ] Pagination handled for list endpoints
- [ ] Rate limit backoff implemented
- [ ] Custom field keys match Aha.io account configuration

---

## Full API Reference

For complete documentation covering all 40+ resource types, see:
[api-reference.md](https://github.com/thoughtlabs-nz/skill-aha/blob/main/api-reference.md)

---

## Skill Metadata

| Property | Value |
|----------|-------|
| **Name** | aha-io-integration |
| **Version** | 1.0.0 |
| **Author** | Thoughtlabs NZ |
| **Repository** | https://github.com/thoughtlabs-nz/skill-aha |
| **Language** | Shell (curl wrappers) |
| **License** | MIT |