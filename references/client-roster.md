# PP Client Roster — Scope, Invoicing, Status

**Living doc.** PP Director / Account Manager / Knowledge Curator read this on every session. Caner edits it directly. Updates here propagate to every client workspace's `brand-brain.md` via `sync-client-roster.mjs`.

**Last updated:** 2026-05-07 (auto-mined from Notion + PP CRM + Gmail + Calendar + Drive)
**Total active engagements:** 9 (1 owned + 8 active clients across sprint, retainer, commission)

> Confidence per field: ✅ confirmed in PP system of record · 🟡 partial · ❓ TBC
> Sources cited inline: `notion://`, `crm://` (Supabase `client_events`), `gmail://`, `cal://`, `drive://`

---

## Cross-cutting facts (PP-side defaults)

### Invoicing infrastructure ✅ (canonical from `pp-weekly-invoicing` scheduled task)

- **Schedule:** every Monday 08:08 (cron `0 8 * * 1`)
- **Generator:** `Purposeful Profits Growth Agency/invoicing/generate_invoices.py` (Playwright PDF)
- **State file:** `invoicing/invoice_state.json` — tracks `last` invoice number, per-client `instalments` counter, `sent_invoices` keyed by `INV-XXXX`
- **Drive folder:** PDFs uploaded to `1FRRINGwzlGmHOfXYY_0OPFqelZgWLOW1`
- **Notion Invoices DB:** `30d3b48f-f9de-4ca4-9038-95b108c1ea44` (data source)
- **Notion Clients DB:** `fd7e9a0b-2e6e-47e6-9ac5-29d7324ec611`
- **Payment statuses:** Draft, Sent, Paid, Overdue, Disputed
- **Reminders:** auto-drafted for overdue invoices (until `payment_status="paid"` flipped in `invoice_state.json`)
- **No VAT** on any invoice (final amounts as quoted)

### Banking

| Currency | Bank | Sort/IBAN | Account |
|---|---|---|---|
| GBP | Revolut | 23-01-20 | 12300692 |
| CAD (Niyama, Younited) | Revolut | IBAN GB15 REVO 0099 6924 0983 73, BIC REVOGB21 | — |

**Account name:** PURPOSEFUL PROFITS LTD

### Client billing — registered names + addresses (canonical)

| Client | Registered Name | Address | Billing Email |
|---|---|---|---|
| 7th Heaven | Montagne Jeunesse (International) Ltd | Astral Court, Central Avenue, Baglan Energy Park, Port Talbot, SA12 7AX | accountspayable@montagnejeunesse.com |
| Vertical Brands | Vertical Brands Ltd | 22 Wenlock Road, London N1 7GU | Aran@verticalbrands.co |
| Long Paws | Long Paws | TBC | elan@longpaws.co.uk |
| Youth and Earth | Empower3d Ltd | Huckletree West, Mediaworks, 191 Wood Lane, London W12 7FP | leyla@youthandearth.com |
| Younited | Younited Nutrition with Purpose | 5858 Fourth Line, Hillsburgh, ON, N0B 1Z0, Canada | renzo@younitedwellness.ca |
| Niyama | (uses CAD bank — registered name TBC ❓) | TBC ❓ | TBC ❓ (likely jillian@niyama-wellness.ca) |

### Sprint pricing

- **Default sprint price:** £500/month per client baseline (per `notion://MRR-Baseline`)
- **Aggregate MRR baseline:** ~£8.5k from ~17 clients
- **Phase 1 MRR target:** £11k by end of Offer sprint
- **Sprint phases (in order):** Offer → CRO → Affiliates/UGC → Ads
- **Last known live invoice:** **INV-2650, £3,250** (Leyla / Empower3d / Youth & Earth, due 28 Apr 2026 — clearly above the £500 baseline, so Y&E is on a higher-tier retainer)
- **Instalment auto-tracking:** counters per client live in `invoice_state.json`. Recent state showed `Younited Wellness: 2`, `Youth and Earth (Empower3d Ltd): 1`. Counter resets to 1 after reaching `instalment_total`.

### Public portals

- Pattern: `purposefulprofits.co/{client-slug}-contract` and `/{client-slug}-invoice`
- Confirmed: 7th Heaven contract + invoice URLs

### Account manager

- Caner across all clients today

---

## 1. KIND2

- **Status:** active ✅
- **Tier:** owned (PP-owned brand)
- **Started:** 2026-05-06 (PPAIOS) · brand operates ongoing
- **Window:** 90-day Phase 1 → £15k MRR target
- **Scope:** Full DTC operation (Email/SMS revival, CRO, content, paid ads day 30+, Amazon day 60+, creator/reseller pipeline, customer service)
- **Invoicing:** N/A — owned brand. P&L tracked via Finance Reporter.
- **Stakeholders:** Caner (operator)
- **Tools:** Shopify (`kind2.myshopify.com`), Klaviyo (4,666 subs), GA4 `properties/290221861`, Meta Ads `act_274969793143990`, Sendcloud
- **Recent activity** (per `crm://kind2 status_update` 2026-05-06):
  - Unity Works fulfilment: REC08001 OOS across orders 8764/8768/8770 → swapped to FRC03001
  - Brigantia invoice 1344 received £356.22 due 14 Jun
  - Stripe payout £51.89 inbound; 3 Shopify Capital UK debits initiated
  - Boost Awards May/Jun deadline list received

---

## 2. Youth & Earth ✅

- **Status:** active ✅ (paid media currently running)
- **Tier:** retainer + paid media management
- **Registered billing entity:** **Empower3d Ltd** ✅
- **Billing address:** Huckletree West, Mediaworks, 191 Wood Lane, London W12 7FP ✅
- **Billing email:** **leyla@youthandearth.com** ✅
- **Started:** existing engagement (Notion page created 2026-04-13)
- **Scope:** Paid media management (Meta primary). Regular status calls ("Youth & Earth x Growthcurve | Status Call")
- **Invoicing:**
  - Last invoice: **INV-2650, £3,250, due 28 Apr 2026** ✅
  - Tracked under instalment counter "Youth and Earth (Empower3d Ltd)" in `invoice_state.json`
- **Stakeholders:** Leyla (primary), Matthew S
- **Tools:**
  - Meta Ad Account: `10153865868170051` ✅
  - Y&E private API key file in Drive (`Y&E_private-api-key.txt`)
- **Recent activity** (per `crm://`):
  - 2026-05-06: Meta billed £1,550 for 2-6 May window
  - Calendar event "Youth" 2026-05-06 12:45-15:00 ✅
  - "Youth & Earth x Growthcurve | Status Call" 2026-05-05
- **Links:** [`notion://Youth & Earth`](https://www.notion.so/34123a47bdd981ef850dca543a5a01e7)

---

## 3. 7th Heaven (Montagne Jeunesse) ✅

- **Status:** active ✅ — currently in **Sprint 2 (Paid Social & PPC)**, transitioning into Sprint 3 (Affiliates & UGC)
- **Tier:** sprint retainer (multi-sprint)
- **Registered billing entity:** **Montagne Jeunesse (International) Ltd** ✅
- **Billing address:** Astral Court, Central Avenue, Baglan Energy Park, Port Talbot, SA12 7AX ✅
- **Billing email:** **accountspayable@montagnejeunesse.com** ✅
- **SOW reference:** **SOW-7TH-2604** ✅
- **Onboarding:** 2026-02-10 (per `notion://Onboarding & Assets`)
- **Sprints completed/in-flight:**
  - Sprint 1: CRO ✅ closed
  - Sprint 2: Paid Social & PPC (in-flight)
  - Sprint 3: Affiliates & UGC (next)
- **Scope:** Amazon UK paid media (Sponsored Products + Sponsored Brands seller + vendor), creator gifting via Pingfluence (Glass Skin Collagen Facemask), CRO, affiliates pipeline
- **Invoicing:** Per-sprint fee structure ❓ specific amount
- **Stakeholders:** Kirstie (primary client contact); PP-side: Caner
- **Tools:**
  - Amazon UK Seller + Vendor accounts; `seventh_heaven_daily`, `seventh_heaven_weekly`, `seventh_heaven_asin_weekly`, `seventh_heaven_campaigns` tables in Supabase ✅ (active data tracking — 105 daily rows, 6 weekly rows, 59 ASIN-week rows)
  - Whitening Strips ASIN: `B0G1T6R24Q`
  - Pingfluence creator gifting active (per gmail Glass Skin Collagen Facemask gift-box invitations to creators)
- **Public:** `purposefulprofits.co/7th-heaven-contract`, `/7th-heaven-invoice`
- **Recent activity** (per `crm://7th-heaven` 2026-05-06):
  - April results review + May growth plan call held 2026-05-05
  - Today: ROAS baseline, audience mapping, creative library review, ad account audit running in parallel
  - Next: lock May ad spend plan, document ROAS baseline, ship creative refresh brief
- **Links:** [`notion://7th Heaven Dashboard`](https://www.notion.so/33523a47bdd9811fb914ccbe8c59ea2a), [`notion://7th Heaven (Montagne Jeunesse)`](https://www.notion.so/33523a47bdd981d6aac3c4d08ccf4dd4)

---

## 4. Vertical Brands (FaceGym engagement) ✅

- **Status:** active ✅
- **Tier:** commission / monthly retainer (FaceGym sub-engagement billed monthly per the invoicing skill)
- **Registered billing entity:** **Vertical Brands Ltd** ✅
- **Billing address:** 22 Wenlock Road, London N1 7GU ✅
- **Billing email:** **Aran@verticalbrands.co** ✅
- **Stakeholders:** Aran (primary contact at Vertical Brands)
- **Scope:** FaceGym email marketing strategy delivery (per Drive: `FINAL_FACEGYM - Email Marketing Strategy - Vertical Brands.key`). Invoice line uses `FaceGym | <Month YYYY>` per skill rendering rules.
- **Invoicing:** Monthly invoice via the same `pp-weekly-invoicing` task (period field = `FaceGym | <Month YYYY>`) ✅
- **Tools:** Klaviyo (assumed, per email strategy doc)
- **Open questions:**
  - Specific monthly fee amount ❓
  - End date of FaceGym engagement ❓

---

## 5. Long Paws ⚠️

- **Status:** active ⚠️ — TTS sprint kicked off 2026-05-06; **billing entity unresolved (P1)**
- **Tier:** 3-month advisory engagement (Mar–Jun 2026)
- **SOW reference:** **SOW LP-0426** (Statement of Work, Long Paws x Purposeful Profits Ltd, v3.0, 1 April 2026)
- **PP entity (filled in SOW):** Purposeful Profits Ltd, Company No. 14802091, 4th Floor, Silverstream House, 45 Fitzroy Street, London W1T 6EB
- **Client entity (NOT filled):** SOW v3 shows `Company Name: [TO BE COMPLETED]`, `Company No.: [TO BE COMPLETED]`, `Registered Address: [TO BE COMPLETED]` for Long Paws side — only Elan's name is on the signature line
- **Why blocked:** Drive screenshots `Longpaws-eSignature-Error-Companies-House.png` + `Long-Paws-Pet-Supplies-Companies-House-Dissolved.png` show **"Long Paws Pet Supplies Ltd" is DISSOLVED at Companies House**. eSignature errored on that entity. A different active entity needs to be confirmed before any invoice can be issued.
- **Billing email:** elan@longpaws.co.uk ✅
- **Stakeholders:**
  - Client: **Elan Mansur** (elan@longpaws.co.uk) ✅ — primary signatory on SOW
  - Intro/finder: **Raphael Patterson** (raphaelpatterson6@gmail.com) — intro invoice received 5 May 2026, due this week ✅
- **Scope (per SOW v3):**
  - **Engagement type:** 3-month strategic advisory (CRO, TikTok Shop, affiliates). No website implementation.
  - **Month 1:** CRO advisory (full-site audit, offer architecture, bundle strategy, PDP restructuring recommendations, landing page brief) + TikTok Shop setup + initial affiliate commission structure (15-25%) and brief + identify 200 micro-influencers
  - **Month 2:** Scale affiliate recruitment to 500+ active affiliates, creator content briefs, leaderboard structure, identify winning content for paid amplification
  - **Month 3:** Affiliate performance review + iteration + CRO recommendations review (pending Shopify migration completion) + end-of-engagement review
  - **Shopify migration dependency:** Long Paws has a Shopify template migration completing end Apr–mid May 2026. Site-level CRO recs are contingent on completion.
- **Governance:** English/Welsh law, exclusive English/Welsh courts. Force majeure mutual. Termination rights mutual. Both parties signed.
- **Recent activity** (per `crm://long-paws` 2026-05-06):
  - TTS kickoff call held 2026-05-06 with Elan (notes in Drive: `🐾 Long Paws TTS | Kickoff Call with Elan – 2026 05 06`)
  - Earlier scoping call: 2026-03-24
  - Intro invoice from Raphael received 5 May
- **Next steps:**
  1. **Resolve billing entity (P1)** — ask Elan which active company name + Companies House number + registered address PP should invoice. Until resolved, no PP invoice can be issued for this engagement.
  2. Pay Raphael intro invoice
  3. Confirm TTS shop access
  4. Send sample brief
- **Drive artefacts:**
  - `LongPaws-SOW-LP-0426-Signable.pdf` (canonical signed copy)
  - `Long_Paws_SOW_v3.docx` (working master)
  - `Long_Paws_Contract_Comparison.docx` (v1→v3 diff)
  - `KIND CO./Clients/Clients/Long Paws/` (full project folder)
  - `KIND CO./Clients/Clients/Youth & Earth/INVOICES/INV-2653-Long-Paws.pdf` (note: filed under Y&E folder by mistake — move to Long Paws/INVOICES on next housekeeping pass)
- **Links:** [`notion://Long Paws`](https://www.notion.so/33623a47bdd98139bd2ec165ea5efe07)

---

## 6. Pingfluence ✅

- **Status:** active ✅ — Sprint 1 (Offer) closing, **Sprint 2 (CRO) starting Week 5**
- **Tier:** sprint retainer
- **Onboarding:** 2026-03-17 ✅
- **Account Manager:** Caner ✅
- **Sprints:**
  - Sprint 1: Offer ✅ (closing) — pricing strategy + 7-touch Apollo outreach + competitive landscape audit
  - Sprint 2: CRO (begins Week 5) — fix JS rendering for SEO, optimise homepage + booking-flow conversions
  - Sprint 3 (planned): Affiliates/UGC
  - Sprint 4 (planned): Ads
- **Current MRR:** £8.3k ✅
- **Target MRR:** £25k by September 2026 ✅
- **Scope (delivered):** 5-email brand nurture sequence, demo no-show recovery sequence, hospitality creator playbook 2026, post-demo follow-up, re-engagement, ad creative, growth audit + ROI calculator, 3-tier pricing launched
- **Stakeholders:** **Ollie** (Oliver Andersen-Cox — confirmed in gmail thread `Ping Oliver Andersen-Cox has accepted this invitation`)
- **Tools:** Apollo (7-touch outbound live + sending), competitive set tracked (Joli, Kolsquare, Collabstr, Modash, Heepsy, Invyted, Secret Social)
- **Case studies confirmed by Ollie:** Lane7 (300+ creators, millions of views, booking spikes), Swiss Butter (queue + hour-long waits), Sixes (book 300+ creators, hit millions of views), Barry's (moved entirely to UGC)
- **Links:** [`notion://Pingfluence Dashboard`](https://www.notion.so/32623a47bdd981c9b028cca032de9edc), [`notion://Sprint Playbook Pingfluence`](https://www.notion.so/32623a47bdd981ed9f1afa7415ee7152)

---

## 7. Younited Wellness ✅

- **Status:** active ✅ — Sprint 1 (Offer) Week 4 (due 17 May 2026)
- **Tier:** sprint retainer (paid in CAD)
- **Registered billing entity:** **Younited Nutrition with Purpose** ✅
- **Billing address:** 5858 Fourth Line, Hillsburgh, ON, N0B 1Z0, Canada ✅
- **Billing email:** **renzo@younitedwellness.ca** ✅
- **Currency:** CAD (paid via Revolut IBAN GB15 REVO 0099 6924 0983 73)
- **Notion client page:** https://www.notion.so/34123a47bdd981629e5df3742e939b00 ✅ (linked in invoicing skill)
- **Instalment counter (per `invoice_state.json`):** Younited Wellness = 2 ✅
- **Sprint timeline:** Sprint 1 Offer → Sprint 4 Ads (handover brief on file)
- **Scope:** Offer sprint completing; Sprint 4 Ads setup brief authored
- **Stakeholders:**
  - Billing: **Renzo** (renzo@younitedwellness.ca) ✅
  - Brand strategy: **Jillian Mariani** (jillian@niyama-wellness.ca) — also runs Niyama (same founder, two brands)
  - Mobile: 416 918 5696
  - Production: April (creative — brand video vertical/horizontal in flight)
- **Tools:** New Younited site in build (per gmail 2026-05-06)
- **Links:** [`notion://Younited Sprint Retrospective`](https://www.notion.so/34123a47bdd981fd8c70e0a81a872fdd), [`notion://Sprint 4 Ads Handover`](https://www.notion.so/34a23a47bdd9816c9ebcf8875f90f580), [`notion://Younited client page`](https://www.notion.so/34123a47bdd981629e5df3742e939b00)

---

## 8. Niyama Wellness ✅

- **Status:** active ✅ — bundles strategy + flow mapping in flight
- **Tier:** sprint retainer
- **Brand:** Niyama Wellness — Yoga-focused health & wellness products
- **Site:** [niyama-wellness.ca](https://www.niyama-wellness.ca/)
- **Scope:** Bundles strategy + flow mapping (existing vs gaps), AI-driven SEO content engine, CRO, UGC + creator outreach (UK primary, US/CA/AU secondary)
- **Stakeholders:**
  - Founder: **Jillian Mariani** (`jillian@niyama-wellness.ca`) — same founder as Younited
  - **POV Media** team: Alanna Wilson (`alanna@povmedia.ca`), Daly Davis (`Daly@povmedia.ca`)
- **Recent activity** (per `crm://niyama` 2026-05-06):
  - Bundles strategy call held 5 May with Alanna + Daly
  - Flow mapping S4 scheduled today
  - Site mint-colour homepage tweak requested
- **Next steps:** complete flow mapping S4, define bundle SKUs + offer, hand off to creative
- **Links:** [`notion://Niyama Dashboard`](https://www.notion.so/32623a47bdd98156a12cfec389ea7b24), [`notion://Niyama Wellness`](https://www.notion.so/32423a47bdd980db8b0ac9e023b7492f), [`notion://Niyama - Offer`](https://www.notion.so/32423a47bdd980d7b1dfde619ef5a369)

---

## 9. Invasion ✅ (NEW — was not in your list)

- **Status:** access provisioned 2026-05-06 ✅
- **Tier:** TBC ❓
- **Scope:** TBC ❓ — Serra Saygili (`saygiliserra@gmail.com`) joined Invasion Business Manager
- **Stakeholders:** Serra Saygili
- **Next:** confirm Serra access tier matches scope; brief PP what Invasion is (gym brand? media brand? clarify)

---

## Cross-cutting open questions (still TBC)

1. Vertical Brands commission % + reporting cadence
2. Per-sprint fee for 7th Heaven, Pingfluence, Niyama, Younited (you said default is £500/mo — does that apply to all, or are some priced higher)
3. Net-X payment terms (INV-2650 was due ~3 weeks after issue → Net 21?)
4. Late-payment policy
5. Renewal cadence between sprints (auto-roll, or quoted per sprint)
6. Termination notice period
7. Invasion: full scope brief

---

## How to update this file

1. Caner edits this file directly (Obsidian, Cursor, any editor).
2. Run: `node ~/dev/ppaios/scripts/sync-client-roster.mjs` → propagates each client section into their workspace's `brand-brain.md` under an auto-synced block.
3. Run: `node ~/dev/ppaios/scripts/sync-to-houston.mjs` → pushes to Houston runtime.

PP Director's first-action list reads this file before anything else, so any session starts with current scope context.
