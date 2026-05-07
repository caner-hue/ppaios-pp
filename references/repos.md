# PP Engineering Repos

PP-managed code repos, where they live locally, what they ship.

## Live consultancy site
- **Repo:** `caner-hue/purposeful-profits`
- **Local clone:** `~/Documents/Kind Co Marketing/purposefulprofits.co`
- **Live URL:** https://purposefulprofits.co
- **Stack:** Next.js, Vercel, Prisma
- **Vercel project:** `purposefulprofits` in team `caner-1192s-projects` (`team_HC4wtBbVDJZOe8LYfw8uL39J`)
- **Cloudflare zone:** `73dc2534543ead0b7f66f16078ea31bf`
- **Update workflow:**
  1. PP Content drafts → save MD/MDX to `outputs/site-updates/{date}-{slug}.md`
  2. PP Operations clones repo if not local, creates branch `pp-{date}-{slug}`
  3. Apply changes, commit, push, open PR via Composio GitHub
  4. Caner reviews PR, merges → Vercel auto-deploys
- **Hard rule:** PP Content NEVER commits directly to main. Branch + PR every time.

## PPAIOS infrastructure
- **`caner-hue/ppaios`** — canonical: skills, references, scripts, knowledge wiki
- **`caner-hue/ppaios-kind2`** — KIND2 brand workspace
- **`caner-hue/ppaios-pp`** — this PP workspace
- **`caner-hue/houston-pp`** — empty fork target for Houston runtime forks (deferred)

## PP CRM
- **Repo:** `caner-hue/pp-crm`
- **Live:** https://pp-crm-psi.vercel.app
- **Stack:** Next.js + Supabase + Resend
- **Lead form:** `https://pp-crm-psi.vercel.app/`
- **Contacts dashboard:** `https://pp-crm-psi.vercel.app/contacts`
- **POST endpoint** (embedded forms): `https://pp-crm-psi.vercel.app/api/contacts`
- **Cron secret:** `pp_cron_8f2a91bd3e7c` (in `.env`)

## Other PP repos
- `caner-hue/myst-metrics` — analytics tooling
- `caner-hue/KIND2` — KIND2 store theme assets
- `caner-hue/pp-imessage-webhook` — iMessage webhook receiver
- `caner-hue/ai-growth-agent-team` — public 108-agent reference team

## How agents make site updates

**Most direct path** (PP Operations agent):
```
cd ~/Documents/Kind\ Co\ Marketing/purposefulprofits.co
git checkout -b pp-2026-05-08-blog-update
# edit MDX/JSX
git add .
git commit -m "blog: <slug>"
git push -u origin pp-2026-05-08-blog-update
gh pr create --title "..." --body "..."
```

**Via Composio GitHub** (preferred for autonomous routines):
- Use `composio execute GITHUB_CREATE_BRANCH`, `GITHUB_PUT_CONTENT`, `GITHUB_CREATE_PULL_REQUEST`.
- Faster for single-file edits (blog post, copy tweak).
- Use shell path for multi-file or when the change needs `npm run build` verification.
