# Notion API — PPAIOS reference

**Used by:** Director (decisions), Creator Manager (creator CRM), Reseller Outreach (pipeline), Content/SEO (briefs), Customer Service (KB).

## Auth
- Internal Integration in Notion → Settings → Integrations → New integration → "PPAIOS".
- Share each database/page with the integration.
- Header: `Authorization: Bearer ${NOTION_TOKEN}`, `Notion-Version: 2022-06-28`.

## Base URL
`https://api.notion.com/v1`

## Endpoints PPAIOS uses

| Verb | Path | Purpose |
|---|---|---|
| GET | `/databases/{id}` | Inspect schema |
| POST | `/databases/{id}/query` | Query rows |
| POST | `/pages` | Create page in a database |
| PATCH | `/pages/{id}` | Update properties |
| GET | `/blocks/{id}/children` | Read page content |
| PATCH | `/blocks/{id}/children` | Append blocks |
| POST | `/search` | Search workspace |

## Per-agent databases (to create in Notion)

| Database | Owner | Purpose |
|---|---|---|
| Tasks | Director | Single source of truth for PPAIOS tasks |
| Decisions | Director | Append-only decision log |
| Creator CRM | Creator Manager | Creators, deliverables, payments |
| Reseller Pipeline | Reseller Outreach | Prospects, stages, last touch |
| Content Calendar | Content/SEO | Posts, status, owner, publish date |
| KB | Customer Service | Resolved tickets → articles |

## Rate limits
- 3 req/sec average per integration. Backoff on 429.

## References
- API: https://developers.notion.com/reference/intro
- Auth: https://developers.notion.com/docs/authorization
