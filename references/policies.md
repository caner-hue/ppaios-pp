# PPAIOS Policies

Workspace-level overrides live at `~/.dev-houston/workspaces/{brand}/.houston/policies.json`. This file describes the defaults.

## Spend caps (per brand)
- Daily total ad spend across Meta + TikTok + Google + Amazon: **£20/day** in Phase 4 entry.
- New campaign launch: ≤ £10/day auto; >£10/day requires Caner approval.
- Budget increase per day: ≤ 20% auto; >20% requires approval.
- Breach of daily total cap: pause all paid until Caner acks.

## Publishing gates
- Theme: branch publishes auto; live publishes gated.
- Blog: `/blog/draft/*` auto; `/blog/{slug}` gated.
- Product create / price change: always gated.
- Discount creation: ≤15% auto; >15% gated.
- New product publish: gated.
- Amazon listing edit: draft auto; submit gated.

## Send caps
- Email broadcast: ≤5k auto; >5k gated.
- SMS broadcast: always gated.
- Social live publish: scheduled queue auto; live publish gated.
- DM reply: drafted auto; sending always gated.
- Outreach email rate: ≤50/day from `out.purposefulprofits.co`. Warm-up window first 4 weeks.

## Customer Service
- First 30 days: drafts only.
- After 30 days, auto-send allow-list:
  - Refund ≤ £50 to existing customer (>1 prior order).
  - Returns ≤ £50 value to existing customer.
  - WISMO replies with verified tracking link.
- Anything else: drafts only.

## Finance Reporter
- **Read-only. Never moves money. Never executes a trade.**
- Hard-coded refusal in skill layer.
- **KIND2 scope:** Shopify orders + ad spend (no Stripe — KIND2 takes all payments via Shopify).

## Kill switch
- File: `~/.dev-houston/KILL_SWITCH`.
- Toggle via iMessage commands `KILL` (create) and `RESUME` (delete).
- Every spend/publish/send skill checks before acting.

## Approvals via iMessage
Caner reply tokens accepted on the Monday review or any blocking ask:
- `OK` — proceed as proposed
- `STOP {channel}` — pause that channel
- `KILL` — full kill switch on
- `RESUME` — kill switch off
- free text — Director interprets
