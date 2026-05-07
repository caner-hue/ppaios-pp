# PP Client Roster — Scope, Invoicing, Status

**Living doc.** PP Director / Account Manager / Knowledge Curator read this on every session. Caner edits it directly. Updates here propagate to every client workspace's `brand-brain.md` via `sync-client-roster.mjs`.

**Last updated:** 2026-05-07 (auto-mined from Notion + PP CRM + Gmail + Calendar + Drive)
**Total active engagements:** 9 (1 owned + 8 active clients across sprint, retainer, commission)

> Confidence per field: ✅ confirmed in PP system of record · 🟡 partial · ❓ TBC
> Sources cited inline: `notion://`, `crm://` (Supabase `client_events`), `gmail://`, `cal://`, `drive://`

---

## Cross-cutting facts (PP-side defaults)

- **Default sprint price:** £500/month per client (per `notion://MRR-Baseline`) ✅
- **Aggregate MRR baseline:** ~£8.5k from ~17 clients (per `notion://MRR-Baseline`) ✅
- **Phase 1 MRR target:** £11k by end of Offer sprint ✅
- **Sprint phases (in order):** Offer → CRO → Affiliates/UGC → Ads
- **Bank for invoicing:** Revolut, sort 23-01-20, account name PURPOSEFUL PROFITS LTD (per gmail invoice INV-2650, £3,250 due 28 Apr 2026)
- **Invoicing tool:** drafted manually + emailed PDF; PP CRM Supabase tracks `client_events` not `invoices` yet
- **Public client portal pattern:** `purposefulprofits.co/{client-slug}-contract` and `/{client-slug}-invoice`
- **Account manager:** Caner across all clients today

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
- **Started:** existing engagement (Notion page created 2026-04-13) — onboarded earlier
- **Scope:** Paid media management (Meta primary). Status calls regular ("Youth & Earth x Growthcurve | Status Call" cadence)
- **Invoicing:** Recurring; specific fee TBC ❓
- **Stakeholders:**
  - Client: Leyla, Matthew S
  - Office: Huckletree West, Mediaworks, 191 Wood Lane, London W12 7FP
  - Last invoice on file: **INV-2650, £3,250, due 28 Apr 2026** (gmail) ✅
- **Tools:**
  - Meta Ad Account: `10153865868170051` ✅ (per `crm://youth-and-earth` 2026-05-06)
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

## 4. Vertical Brands (FaceGym engagement)

- **Status:** active 🟡 (data thin in PP system today)
- **Tier:** commission
- **Scope:** FaceGym email marketing strategy delivery (per Drive: `FINAL_FACEGYM - Email Marketing Strategy - Vertical Brands.key`)
- **Invoicing:** Commission only ❓ %
- **Stakeholders:** TBC ❓
- **Tools:** TBC ❓
- **Open questions:**
  - Commission % and trigger (revenue lift? campaign performance fee?)
  - Reporting cadence to Vertical Brands?
  - PP-side lead?

---

## 5. Long Paws ✅

- **Status:** active ✅ — TTS sprint kicked off 2026-05-06
- **Tier:** sprint (TTS = TikTok Shop launch)
- **Scope:** TikTok Shop setup + samples + commission structure for TTS launch
- **Stakeholders:**
  - Client: **Elan Mansur** (`elan@longpaws.co.uk`) ✅
  - Intro/finder: **Raphael Patterson** (`raphaelpatterson6@gmail.com`) — intro invoice received 5 May 2026 due this week ✅
- **Tools:** TikTok Shop (linkup ready per gmail 2026-05-06)
- **Recent activity** (per `crm://long-paws` 2026-05-06):
  - TTS kickoff call held 2026-05-06 with Elan
  - Covered: TTS access, commission structure, samples
  - Intro invoice from Raphael received 5 May
- **Next steps:** pay Raphael intro invoice, confirm TTS shop access, send sample brief
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
- **Tier:** sprint retainer
- **Sprint timeline:** Sprint 1 Offer → Sprint 4 Ads (handover brief on file)
- **Scope:** Offer sprint completing; Sprint 4 Ads setup brief authored — audience segments, site performance context from Sprints 1-2, Sprint 4 access requirements
- **Stakeholders:**
  - Founder: **Jillian Mariani** (`jillian@niyama-wellness.ca`) — also runs Niyama (same founder, two brands) ✅
  - Mobile: 416 918 5696
  - Production: April (creative — brand video vertical/horizontal in flight; Niyama site mint-colour tweak request 2026-05)
- **Tools:** New Younited site in build (per gmail 2026-05-06: "horizontal video will be fantastic for when the new Younited website is ready")
- **Links:** [`notion://Younited Sprint Retrospective`](https://www.notion.so/34123a47bdd981fd8c70e0a81a872fdd), [`notion://Sprint 4 Ads Handover`](https://www.notion.so/34a23a47bdd9816c9ebcf8875f90f580)

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
