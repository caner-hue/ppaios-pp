# Google Workspace CLI (gws) — PPAIOS reference

**Used by:** Customer Service (Gmail), Director (Gmail send + Calendar), Content/SEO (Drive + Docs), Reseller Outreach (Gmail send), Analytics (Sheets dashboards), Creator Manager (Gmail).

## Why
One CLI covers Gmail, Calendar, Drive, Docs, Sheets, Slides. Token efficient vs an MCP per surface.

## Install
```sh
brew install gws-cli  # or follow https://github.com/<...>/gws-cli
gws auth login        # OAuth2 device flow against the PP Workspace
```

## Common commands

### Gmail
```sh
gws gmail list --query "is:unread newer_than:1d" --max 50
gws gmail get <message-id>
gws gmail send --to "x@y.com" --subject "..." --body-file ./body.md
gws gmail label add <message-id> --label "Triaged"
gws gmail archive <message-id>
```

### Calendar
```sh
gws calendar list --since today --until 7d
gws calendar create --summary "..." --start "2026-05-12T10:00" --duration 30m
```

### Drive
```sh
gws drive ls "Purposeful Profits Growth Agency"
gws drive cp ./report.md drive:"Reports/2026-05-Report.md"
```

### Docs / Sheets / Slides
```sh
gws docs create --title "Weekly Review" --from ./review.md
gws sheets append "<sheet-id>" --range "KPIs!A:E" --values-file ./row.csv
gws slides create --title "Pitch deck" --template-id "<id>"
```

## Per-agent accounts
- Each agent uses a dedicated Google account where possible (e.g. `agent-cs@kind.community`).
- For send: keep `hello@purposefulprofits.co` for warm/transactional; `out.purposefulprofits.co` for cold (separate workspace, 4-week warm-up).

## References
- gws-cli docs (TBC pin upstream URL Phase 0)
- Gmail API direct: https://developers.google.com/gmail/api
- Calendar API: https://developers.google.com/calendar
- Drive API: https://developers.google.com/drive/api
