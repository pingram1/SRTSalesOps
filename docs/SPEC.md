# SRTSalesOps — Product Spec

**Start Right Tutoring · internal only · 2026-08-16**

This is the idea-level spec. Code is generated from this plan, not the other way around. `docs/BUILD-PLAN.md` is the implementation companion.

---

## Who it is for

Me. Pierre. Solo operator of Start Right Tutoring. I take discovery calls for **Platforms** and **AI Consulting**, research local businesses in Gemini, and need one place that turns that work into outreach, a pipeline, and a PDF I can email within 24 hours of a call.

Not for clients. Not the public website. Not the Learning / OpSRT student waitlist.

## What it does

After I paste a Gemini research chat (businesses in a specific area, each with a pitch tied to the new website services), the app creates one card per company. I edit the pitch, copy an email, send it from `pingram@startrighttutoring.com`, and track follow-up. When someone books a call, I score five questions, it recommends Starter / Essential / Professional / Elite, I lock a quote, and I download a branded one-tier PDF.

Existing clients stay on the same record: tier, monthly, launch date, included hours.

## What excites me

I do not want a second brain. I want to open one app, see who I researched, who I owe a follow-up, who I quoted, and who is paying a monthly — and generate the proposal from that same record.

The PDF is the client-facing product. The calculator and pipeline are how I get there.

## What it is not

- Salesforce
- An email client (Gmail stays Gmail)
- A public pricing page
- Outlook / Microsoft 365 (work mail is Google Workspace)
- A Gemini API integration in v1 (paste only)
- A student / tutoring CRM

---

## The pipeline

| Stage | Who they are | What I do |
|---|---|---|
| **Research** | Gemini found them. Not contacted. | Review pitch, set a next action |
| **Lead** | I reached out or they inbound | Log emails, book discovery |
| **Quoted** | Call happened | Triage, one tier, send PDF |
| **Client** | They signed | Track monthly, hours, term |
| **Lost** | Not a fit / no | Reason, stop follow-up |

```
Gemini paste → Campaign → Research cards
    → Copy email as pingram@ → Lead
    → Discovery triage → Quote builder
    → One-tier PDF
    → Won → Client
```

**Lead generation** is my Gemini research-and-outreach, not ads. A second Gemini chat for a different city is a new campaign so lists do not mix.

---

## Research import

v1: a “New campaign from Gemini” screen. Campaign name, area, paste the chat or a table. Parse companies + pitch notes. Preview. Confirm. Dedupe by name / website / email. Store the raw paste on the campaign.

Ask Gemini to re-output as:

```
Business name | Website | City | Contact name | Email | Likely need | One-sentence pitch | Suggested first email
```

Skip tutoring/parent rows (Learning arm).

---

## Outreach

From: `pingram@startrighttutoring.com`  
v1: Copy email, copy subject, mark sent, set outcome (no reply / replied / booked / not a fit). `mailto:` is fine. Gmail API is later.

Voice: confident, specific, no hype, no exclamation marks. A concrete idea for *their* business.

---

## Rate card (do not renegotiate)

| | Starter | Essential | Professional | Elite |
|---|---|---|---|---|
| Build | $1,500 | $4,500 | $12,000 | From $30,000 |
| Monthly | — | $199 | $895 | $2,950 |
| Year one | $1,500 | $6,888 | $22,740 | $65,400 |
| Annual prepay (2 months free) | $1,500 | $6,490 | $20,950 | $59,500 |
| Timeline | 1–2 weeks | 3–5 weeks | 6–10 weeks | 10–16 weeks |
| Deposit | 100% kickoff | 50/50 | 40/30/30 | 30/30/40 |
| Initial term | none | 6 months | 12 months | 12 months, 60-day notice |

Starter $1,500 credits toward Essential within 12 months. **Monthly begins at launch.**

Full inclusions: `docs/sales/service-tiers.md`.

If they quantify a leak over **$250,000/year**, flag “value-price this” and do not force Elite. See `docs/sales/value-based-pricing-model.md`.

---

## Discovery triage

Five questions, score 1–4, total 5–20. Exact wording in `docs/sales/discovery-triage.md`.

| Total | Recommend |
|---|---|
| 5–8 | Starter |
| 9–12 | Essential |
| 13–16 | Professional |
| 17–20 | Elite |

Overrides: (1) Q5 = 4 and leak > $250k → value-price flag. (2) High repetitive-work score, everything else low → $2,500 AI readiness assessment, not a website. (3) Warn if I override downward.

Client sees **one tier**. Never the menu.

---

## Quote builder

On the company record: recommended tier, override, add-ons, Elite build fee (default 30000), kickoff month, pace (Fast / Typical / Slow), annual prepay.

Two ledgers:

- **Contract year one** — 12 service months from launch (what I quote)
- **This calendar year** — cash by 31 December; monthly only after launch

Launch month = first fully billed month. Weeks → months at 4.345.

---

## Two outputs

**Internal:** scores, override warnings, both cash ledgers, month table, margin/hours notes.

**Client PDF:** Start Right Tutoring branding. Cover with prospect name and date. One tier — included / not included. Quote table. Short “why this tier.” **Never** scores, margins, other tiers, or `$150/hr`.

---

## Existing clients

Tier, build, monthly, kickoff, launch, term end, included hours, hours used this month (typed). Warn if they exceed the cap two months running.

---

## Brand

Start Right Tutoring. Dark navy `hsl(230 35% 7%)` + cyan `hsl(195 85% 48%)`. Space Grotesk / Inter / JetBrains Mono. Internal UI = quiet dashboard. Client PDF = marketing-site feel, not a SaaS invoice.

---

## Build order

1. Pipeline, Gemini paste, company records, Today follow-ups  
2. Outreach (copy / mark sent)  
3. Triage + quote + schedule  
4. Client PDF  
5. Existing clients  
6. Later: Gmail, website inbound, auth, deploy  

Login v1 is localhost only. Storage v1 is `localStorage` key `srt-ops:v1`.
