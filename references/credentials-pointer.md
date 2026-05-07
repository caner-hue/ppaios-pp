# Credentials — Pointer (DO NOT COMMIT SECRETS HERE)

PP agents need credentials to operate. **Secrets live outside this repo:**

## Where to read
1. **`~/.dev-houston/.env`** — chmod 600, machine-local. Loaded by Houston routines automatically.
2. **`Purposeful Profits Growth Agency/memory/context/credentials.md`** in Google Drive — full master list, edited by Caner.

## What's in `.env` already (PP-relevant)
- `RESEND_API_KEY` — transactional email from `hello@purposefulprofits.co`
- `RESEND_FROM=hello@purposefulprofits.co`
- `RESEND_DOMAIN_ID=9eb884eb-4a02-4a59-9cf0-40135ce8aa86`
- `SUPABASE_URL=https://walaabqjmhbvsltmkvmq.supabase.co`
- `SUPABASE_PROJECT_REF=walaabqjmhbvsltmkvmq`
- `SUPABASE_ANON_KEY` (anon, public-safe)
- `SUPABASE_SERVICE_KEY` (service role, server-only — NEVER expose to client)
- `PP_CRM_URL=https://pp-crm-psi.vercel.app`
- `PP_CRM_CRON_SECRET=pp_cron_8f2a91bd3e7c`
- `VERCEL_TEAM_SLUG=caner-1192s-projects`
- `VERCEL_TEAM_ID=team_HC4wtBbVDJZOe8LYfw8uL39J`
- `CLOUDFLARE_ACCOUNT_ID=4ad51e54135daa8fa41ec76833a56bf1`
- `CLOUDFLARE_ZONE_PP=73dc2534543ead0b7f66f16078ea31bf`
- `GITHUB_PAT=ghp_…` (gh CLI auth)
- `GH_OWNER=caner-hue`
- Meta Ads token + KIND2 ad account IDs (for cross-client work)

## What's in Composio (no `.env` needed)
- GitHub, Gmail, Google Ads, GA4, Calendar, Drive, Klaviyo, Notion, Shopify

## Agents that need credentials by role

| Agent | Needs |
|---|---|
| PP Director | iMessage MCP + Gmail (Composio) + Slack (when wired) |
| PP Sales | Gmail (Composio) + PP CRM URL/cron secret + GitHub (PRs to crm repo) |
| PP Content | GitHub (Composio) + Drive (Composio) + purposefulprofits.co repo (local clone) |
| PP Account Manager | Gmail (Composio) + Notion (Composio) + cross-workspace read |
| PP Finance | Stripe (Composio) + Resend + Supabase (PP CRM revenue tables) |
| PP Operations | GitHub (Composio + local) + Vercel (via gh + curl) + Cloudflare zone |
| PP Knowledge Curator | Drive + Notion + cross-workspace read |

## Hard rules
- Never echo a secret value in chat output.
- Never commit `.env` or any file containing keys.
- Never paste a secret into a Notion DB.
- For ops that need a secret, read it via `process.env.X` or `cat ~/.dev-houston/.env | grep X` and use it inline.
