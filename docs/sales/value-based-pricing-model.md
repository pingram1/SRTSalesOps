# Value-Based Pricing Model — Internal

**Audience: Start Right Tutoring only. Never send this file to a client.**

This is the engine. It converts a discovery call into three defensible prices. The client-facing output is generated from it — see [value-proposition-template.md](./value-proposition-template.md) and the worked example at [examples/smith-co-custom-home-builders.md](./examples/smith-co-custom-home-builders.md).

---

## Which pricing system to use

Start Right Tutoring runs two pricing systems. Using the wrong one costs money in both directions.

| Situation | Use |
|---|---|
| Client wants a website, maintenance, or a defined package of automation work | [service-tiers.md](./service-tiers.md) — the fixed rate card |
| Modeled annual value under $250,000 | [service-tiers.md](./service-tiers.md) |
| Modeled annual value above $250,000 with a quantifiable revenue leak | This document |
| Client can't or won't quantify the value | [service-tiers.md](./service-tiers.md) — you cannot value-price without inputs |

**The short version.** Most prospects are rate-card clients. A small business that wants a good website and someone to maintain it does not need a value model — it needs a price, quickly, from a menu. Running the engine below on a $6,000 engagement wastes their time and yours, and the guardrails will simply tell you to decline work that is perfectly good business at rate-card prices.

The engine below is for the minority of engagements where the client has a large, measurable problem and the fixed card would leave serious money on the table. Elite tops out at $65,400 in year one. A client with a $400,000 annual leak should not be paying $65,400.

---

## The core principle

**Every price is derived, never quoted.**

We compute the client's year-one value first, then price each tier as a fixed fraction of it. The client never sees a number that isn't visibly anchored to their own arithmetic. This is what makes the fee an asset line rather than an expense line, and it is the entire reason we do not publish rate cards.

Practical consequence: if you cannot compute the value, you cannot quote the price. Leave the discovery call with the six inputs below or book a second call. Quoting from instinct destroys the model.

---

## Step 1 — The value equation

Year-one value `V` is the sum of three streams. Each must survive being questioned independently.

```
V = V_revenue + V_labor + V_risk

V_revenue = leads_recovered_per_month × 12 × close_rate × contribution_per_win
V_labor   = hours_saved_per_month × 12 × fully_loaded_hourly_cost
V_risk    = annualized avoided cost (churn, rework, penalties, redundant tool spend)
```

### The six inputs to collect on the discovery call

| Input | What to actually ask |
|---|---|
| `leads_recovered_per_month` | "How many inbound calls or forms go unanswered in a typical week?" |
| `close_rate` | "Of the qualified leads you *do* reach, how many become jobs?" |
| `contribution_per_win` | "What's your gross profit on a typical job?" — **not** contract value |
| `hours_saved_per_month` | "Walk me through what your admin does manually every week." |
| `fully_loaded_hourly_cost` | Salary ÷ 2080, then × 1.3 for tax, benefits, overhead |
| `avoided_cost` | Tool subscriptions replaced, penalties, rework, churn |

### The credibility move: discount by close rate

A "$50,000 lead" is not worth $50,000. It is worth `$50,000 × close_rate`. Say this out loud, unprompted, before the client can think it.

> "Three leads a month at fifty thousand each isn't a hundred and fifty thousand a month. You close about one in four, so it's closer to thirty-seven and a half. I'd rather build the case on a number you can defend to your CFO than one that falls apart the first time someone checks it."

This single sentence does more for close rate than any slide in the deck. It signals you are modeling their business rather than selling into it, and it pre-empts the "these numbers are inflated" objection permanently.

### Use gross profit, never contract value

A $1.2M custom home is not $1.2M of value. Ask for gross margin and use that. On a discovery call where the client will not disclose margin, use conservative industry defaults and say you are doing so:

- Custom residential construction: 15–20% of contract value
- Professional services: 40–60% of revenue
- E-commerce: 30–45% of revenue
- SaaS: 70–80% of revenue

### Three rules that keep the model honest

1. **Halve anything the client is enthusiastic about.** Clients inflate their own pain. Their "we lose like five leads a week" is three a month.
2. **Never count the same dollar twice.** If the AI receptionist recovers a lead *and* saves the admin an hour of callback chasing, the hour is already inside the lead value. Count it once.
3. **Exclude anything you cannot instrument.** If you can't measure it in month six, it doesn't go in the model. "Improved brand perception" is not a value stream.

### Cost of delay

```
cost_of_delay_per_month = V ÷ 12
```

Compute this every time and write it down before the pricing conversation. It is the single most useful number in the engagement — it carries the entire objection-handling section, and it is the number you repeat when the room goes quiet.

---

## Step 2 — Tier construction

Each tier captures a different fraction of `V`. Year-one investment is then derived by dividing captured value by a target return multiple.

```
captured_value  = V × capture_fraction
y1_investment   = captured_value ÷ target_multiple
build_fee       = round(build_split × y1_investment, nearest $1,000)
monthly_fee     = round((y1_investment − build_fee) ÷ 12, nearest $50)
```

### Design constants

| Tier | Capture fraction | Target multiple | Build split | Resulting % of captured value |
|---|---|---|---|---|
| Essential | 45% | 6.75× | 44% | ~15% |
| Professional | 80% | 5.65× | 42% | ~18% |
| Elite | 100% | 3.65× | 40% | ~27% |

**Why Elite prices above the 10–18% band the other two sit in.** Essential and Professional are priced purely against modeled value. A meaningful share of the Elite retainer buys capacity and optionality — reserved engineering hours, new value streams that were never in the model, a standing seat rather than a scheduled service. Clients buying Elite are buying access, and access is priced differently from output. Do not apologize for this on the call; state it plainly as what distinguishes the tier. If a client challenges the Elite rate specifically, that is a signal they should be on Professional.

### Build fee stays at 40–45% of year one

Recurring revenue is where retention and margin live, and a lower build fee reduces the size of the yes we're asking for. Never let the build fee exceed 50% of year one — it front-loads risk onto the client and turns the engagement into a project instead of a relationship.

### Tier separation is deliberate

Elite is the anchor. Professional wins the deal.

Professional's net gain should land within roughly 10% of Elite's while costing about half. That gap is what makes Professional the obvious choice rather than the cheap one — the client selects it feeling shrewd rather than budget-constrained, which is a materially better state to begin an engagement in.

Essential exists to be declined. It is not a trap; it is genuinely deliverable and genuinely worth buying. But its role in the conversation is to establish the floor and make Professional's incremental cost look small against its incremental value.

**Present in descending order: Elite, then Professional, then Essential.** Anchoring only works in that direction.

---

## Step 3 — Positioning the recurring fee

Call it **operations**, never **maintenance**.

Maintenance implies decay — you are being paid to stop something from getting worse, which is a cost centre. Operations implies compounding — you are being paid to make something continuously better, which is an investment. The work is identical. The framing determines renewal.

What actually goes in the recurring fee:

- Hosting, monitoring, uptime, security patching
- AI tuning against real call transcripts — the receptionist gets measurably better every month
- Conversion-rate and performance optimization against live traffic
- A monthly performance review against the ROI model in the proposal

That last one matters more than the rest combined. Reviewing your own ROI projection monthly, in front of the client, using real numbers, is the reason retainers survive budget season. It converts the proposal from a sales artifact into an operating scorecard.

---

## Step 4 — Guardrails

### Floors

No engagement below **$8,500 build** and **$750/month**, regardless of what the model returns. Below this the work cannot be delivered to a standard worth attaching the Start Right Tutoring name to.

When the derived price falls below a floor, the floor wins and the return multiple drops. Disclose the real multiple anyway.

### Engagement thresholds

Stress-tested against the model at both extremes:

- **`V` < $250,000/yr** — do not value-price this. Quote from [service-tiers.md](./service-tiers.md) instead. Below this level the delivery floors compress the tiers into roughly the same number and the value model adds friction without adding revenue. This is not bad business — it is most of your business — it just belongs on the fixed card.
- **`V` ≥ $250,000** — full three-tier value structure. Tiers separate cleanly and the bespoke model earns its overhead.

These thresholds describe *which pricing instrument to use*, not which clients to accept. A client with $60,000 of modeled value is a perfectly good Essential or Professional engagement; they are simply not a value-priced engagement.

### Taper above $1M

For `V` > $1,000,000, apply standard rates to the first $1M and **half** the standard rate above it.

Without the taper, a $2M-value engagement prices Elite at roughly $548,000 year one. The 3.65× is real, but absolute magnitude triggers procurement review regardless of the multiple, and the deal dies in a process you cannot influence. With the taper the same engagement prices near $411,000 and returns 4.86× — a smaller invoice *and* a stronger pitch.

### Stress-test results

The engine was run across the full range of deal sizes. These are the actual outputs, and they are why the thresholds above sit where they do:

| Modeled value | Essential return | Professional return | Elite return | Behavior |
|---|---|---|---|---|
| $60,000 | 1.54× | 2.74× | 3.31× | All three floored to nearly the same price. Use the rate card. |
| $120,000 | 3.09× | 5.13× | 3.66× | Essential and Professional land within $1,200 of each other. Use the rate card. |
| $250,000 | 6.22× | 5.65× | 3.65× | Clean separation. Three-tier structure works from here up. |
| $470,160 | 6.74× | 5.66× | 3.65× | Reference case. Professional nets within 9.3% of Elite. |
| $2,000,000 | 6.75× | 6.95× | 4.86× | Taper active on Professional and Elite. |

**One inversion to know about.** Above roughly $1.25M of modeled value, Professional's return multiple overtakes Essential's — at $2M it is 6.95× against 6.75×. This happens because the taper only applies to captured value above $1M, so Professional and Elite get relief that Essential does not.

This is not a bug and does not need fixing. It means that on large engagements Professional beats Essential on *both* net gain and return multiple, which makes the recommendation easier rather than harder. Just do not be caught off guard if a sharp CFO notices that the middle tier is the most efficient option on the page — the correct response is "yes, that's why we're recommending it."

### Capacity cap

Never price above what the team can deliver. A price you cannot honor is worse than no deal — it costs the client, the reference, and the referral chain behind it. Above roughly $250,000 in year-one delivery, restructure as a phased multi-year program rather than compressing everything into twelve months.

### Never discount — cut scope

Discounting retroactively invalidates the ROI math you just presented. If $28,000 becomes $22,000 because they pushed, then the $28,000 was never derived from anything, and every number in the proposal is now suspect.

When there is genuine budget pressure, in order of preference:

1. **Move down a tier.** The tiers exist for exactly this.
2. **Phase the scope.** Website in Q1, AI receptionist in Q2. Full price, sequenced delivery.
3. **Restructure payment.** 40/30/30 across milestones, or a higher retainer with a lower build fee. Same total, easier cash flow.
4. **Trade a discount for something of equal value.** A case study with named metrics, a video testimonial, two warm referrals, or a 24-month term instead of 12. Never give price away for free.

### Walk away when

- They want the AI receptionist but will not give access to the CRM. You will be blamed for an integration you were not permitted to build.
- They will not share close rate or margin. You cannot model value, so you cannot value-price — move them to the rate card rather than guessing.
- The value case rests entirely on `V_risk`. Avoided costs are the softest stream and the hardest to prove in month six.
- They have fired two agencies in eighteen months. You will be the third.
- They negotiate before the value model has been presented. The frame is already wrong and will not recover.

---

## Worked reference — Smith & Co. Custom Home Builders

Inputs: 3 leads/month recovered, 25% close rate, $50,000 contribution per win, 60 hours/month saved, $28/hr fully loaded.

```
V_revenue = 3 × 12 × 0.25 × $50,000 = $450,000
V_labor   = 60 × 12 × $28           =  $20,160
V         =                            $470,160

cost of delay = $470,160 ÷ 12 = $39,180 / month
```

| Tier | Captured value | Build | Monthly | Year one | Return | Net gain |
|---|---|---|---|---|---|---|
| Essential | $211,572 | $14,000 | $1,450 | $31,400 | 6.74× | $180,172 |
| Professional | $376,128 | $28,000 | $3,200 | $66,400 | 5.66× | $309,728 |
| Elite | $470,160 | $52,000 | $6,400 | $128,800 | 3.65× | $341,360 |

Professional nets $309,728 against Elite's $341,360 — within 10% — at roughly half the year-one commitment. That is the tier that should close.

---

## Payback modeling

Value does not begin on day one. Model the ramp honestly or the payback figure will not survive contact with reality:

- **Months 1–2:** build. No value accrual.
- **Month 3:** launch. 50% of monthly value.
- **Month 4 onward:** 100% of monthly value.

Payback is the month where cumulative value crosses cumulative investment. On the Smith & Co. Professional tier that lands in **month 4**. Quote payback in months, not weeks — weeks sound like a sales claim, months sound like a plan.

Use the interactive calculator to run this live on a call. Changing the client's own assumptions in front of them converts the pricing from your claim into their arithmetic, which is the shortest path from proposal to signature.
