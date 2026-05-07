# Fireflies + Gemini Meetings — PPAIOS reference

**Used by:** Director (action items), Creator Manager (creator calls), Reseller Outreach (sales calls).

## Fireflies GraphQL API
- Auth: Bearer API key from Fireflies.ai → Settings → Developer.
- Endpoint: `https://api.fireflies.ai/graphql`
- Header: `Authorization: Bearer ${FIREFLIES_API_KEY}`.

### Useful queries
```graphql
query Recent {
  transcripts(limit: 10) {
    id title date duration meeting_link
    summary { keywords action_items overview }
  }
}

query OneTranscript($id: String!) {
  transcript(id: $id) {
    title date duration
    sentences { text speaker_name start_time }
    summary { action_items overview short_summary }
  }
}
```

## Gemini-via-Google
- Gemini meeting notes drop into Drive automatically when set up in Google Meet → Settings.
- Path pattern: `Meet Recordings/<title> - <date>` and a paired Google Doc with notes.
- Read via gws CLI: `gws drive ls "Meet Recordings"` then `gws docs export <id>`.

## PPAIOS workflow
1. Daily 7am routine: pull last 24h Fireflies transcripts.
2. Pull yesterday's Gemini Meet notes from Drive.
3. Run `summary-extract` skill: action items → Notion Tasks DB; decisions → Notion Decisions DB.
4. iMessage Caner if any P1 action item ("client churning", "missed delivery", "deadline today").

## References
- Fireflies API: https://docs.fireflies.ai/getting-started/introduction
- Gemini in Workspace: https://workspace.google.com/products/gemini/
