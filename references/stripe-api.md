# Stripe API — PPAIOS reference (read-only)

**Used by:** Finance Reporter only. **Hard rule: never moves money.**

## Auth
- Restricted key created in Stripe Dashboard → Developers → API keys → Create restricted key.
- Permissions: read-only on Charges, Customers, Invoices, Payouts, Balance, Subscriptions, Refunds.
- Header: `Authorization: Bearer ${STRIPE_API_KEY_RO}`.

## Base URL
`https://api.stripe.com/v1`

## Endpoints PPAIOS uses (all GET)

| Path | Purpose |
|---|---|
| `/charges` | Recent charges + refund status |
| `/balance` | Current available + pending |
| `/balance_transactions` | Detailed P&L line items |
| `/payouts` | Payout history |
| `/customers` | Customer list (small reads only) |
| `/invoices` | Invoices issued |
| `/subscriptions` | Active subs + MRR calc |

## Rate limits
- 100 read req/sec, 100 write req/sec (we don't write).
- 429 → respect `Retry-After`.

## Storage
- `STRIPE_API_KEY_RO` in `.env`.

## References
- API: https://stripe.com/docs/api
- Restricted keys: https://stripe.com/docs/keys#limit-access
