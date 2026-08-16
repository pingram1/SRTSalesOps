# Value Proposition Document — Master Template

**How to use this file.** Copy it, replace every `{{placeholder}}`, delete this block and the internal appendix at the bottom, then export to PDF. Derive all pricing from [value-based-pricing-model.md](./value-based-pricing-model.md) before you start writing — never fill the pricing section from instinct. A completed reference is at [examples/smith-co-custom-home-builders.md](./examples/smith-co-custom-home-builders.md).

**Voice.** Confident, clear, technical-but-human. Specific over impressive. No hype, no "revolutionize", no "cutting-edge", no exclamation marks. Every claim carries a number or gets cut. If a sentence would read the same in any other agency's proposal, rewrite it.

**Length.** Six pages maximum. If the ROI section is right, nothing else needs to be long.

---

# Prepared for {{Client Business Name}}

**{{Client Industry}}**
Prepared by Start Right Tutoring · {{Date}}
{{Primary Contact Name}}, {{Title}}

---

## 1. Executive Summary

{{One paragraph, 3–4 sentences, in their language rather than ours. Name the bottleneck as they described it on the call — reuse their exact phrasing where you can, because it proves you listened. Do not mention any technology here.}}

Three things are costing you money right now:

1. **{{Pain point one}}** — {{one sentence on the business consequence, with a number}}
2. **{{Pain point two}}** — {{one sentence on the business consequence, with a number}}
3. **{{Pain point three}}** — {{one sentence on the business consequence, with a number}}

Together these represent an estimated **{{$cost_of_delay}} per month** in revenue you are not capturing and labor you are paying for twice. That figure is derived entirely from numbers you gave us on {{date of discovery call}} — the arithmetic is shown in section 3 so you can check it.

> **Writing note — delete before sending.** Lead with the cost of delay. It reframes everything downstream: by the time they reach pricing they are comparing your fee against a monthly loss they have already accepted as accurate, not against zero.

---

## 2. The Digital Transformation Plan

{{Two sentences on the approach before listing components. Non-technical throughout — the reader is an owner or operator, not an engineer. Describe what changes about their day, not what gets deployed.}}

### {{Component One — e.g. A website built to load in under two seconds}}

**What it is.** {{Plain-language description. No framework names, no stack, no jargon.}}

**What changes for you.** {{The observable difference in their business. "Someone searching for a custom builder in {{their city}} finds you before they find your competitor."}}

**How we'll know it worked.** {{The specific metric, with its current baseline. "Mobile load time under 2 seconds, down from 8. Measured monthly."}}

### {{Component Two — e.g. An AI receptionist that answers every call}}

**What it is.** {{Plain-language description.}}

**What changes for you.** {{Observable difference.}}

**How we'll know it worked.** {{Specific metric with baseline.}}

### {{Component Three}}

**What it is.** {{Plain-language description.}}

**What changes for you.** {{Observable difference.}}

**How we'll know it worked.** {{Specific metric with baseline.}}

### Timeline

| Phase | Duration | What you'll see |
|---|---|---|
| Discovery and architecture | {{X weeks}} | {{Concrete deliverable they can look at}} |
| Build | {{X weeks}} | {{Concrete deliverable}} |
| Launch | {{X weeks}} | {{Concrete deliverable}} |
| Operations | Ongoing | {{Monthly performance review against the projections in section 3}} |

> **Writing note — delete before sending.** Every component gets all three subheadings. "How we'll know it worked" is the one competitors omit, and it is the one that signals you intend to be measured. It also sets up the monthly review that keeps the retainer alive.

---

## 3. The ROI Projection

Every number below comes from the discovery call on {{date}}. Where we had to estimate, we chose the conservative figure and marked it.

### What's being lost today

**{{Revenue stream — e.g. Missed inbound leads}}**

```
{{X}} leads recovered per month
  × 12 months
  × {{Y}}% close rate          ← your number, not an industry average
  × {{$Z}} gross profit per job ← gross profit, not contract value
  = {{$V_revenue}} per year
```

{{One sentence naming the conservative choice you made. "We've used your 25% close rate rather than the industry's 30%, and gross profit rather than contract value — this is the defensible floor, not the ceiling."}}

**{{Labor stream — e.g. Manual data entry}}**

```
{{X}} hours per month
  × 12 months
  × {{$Y}} fully loaded hourly cost ← salary plus tax, benefits, overhead
  = {{$V_labor}} per year
```

{{If applicable:}}

**{{Avoided cost stream}}**

```
{{Description of the calculation}}
  = {{$V_risk}} per year
```

### Total annual opportunity

| Stream | Annual value |
|---|---|
| {{Revenue stream}} | {{$V_revenue}} |
| {{Labor stream}} | {{$V_labor}} |
| {{Risk stream}} | {{$V_risk}} |
| **Total** | **{{$V}}** |

**This works out to {{$cost_of_delay}} for every month the current setup stays in place.**

That is the number this proposal is measured against. Not our fee — the cost of the alternative.

> **Writing note — delete before sending.** Show the arithmetic as arithmetic. A formula they can check builds more trust than a polished summary figure, because it invites verification instead of deflecting it. If they correct one of your inputs, that is a good outcome: they are now co-authors of the number, and people do not argue with their own math.

---

## 4. Investment Options

Three ways to move forward. Each is priced as a fraction of the value it is projected to capture — the return multiple is shown for every option so you can compare them directly.

### Elite — {{$elite_build}} build + {{$elite_monthly}}/month

*{{One line on who this is for. "For {{Client}} if the goal is to make {{outcome}} the growth engine for the next three years, not just fix what's broken."}}*

Everything in Professional, plus:

- {{Elite-only deliverable}}
- {{Elite-only deliverable}}
- {{Elite-only deliverable}}
- Reserved engineering capacity — {{X}} hours monthly, yours to direct
- {{Response time / access commitment}}

| | |
|---|---|
| Year-one investment | **{{$elite_y1}}** |
| Projected value captured | **{{$elite_captured}}** |
| Return | **{{elite_multiple}}×** |
| Net gain, year one | **{{$elite_net}}** |

### Professional — {{$pro_build}} build + {{$pro_monthly}}/month

*Recommended for {{Client Business Name}}.*

Everything in Essential, plus:

- {{Professional-only deliverable}}
- {{Professional-only deliverable}}
- {{Professional-only deliverable}}
- Monthly performance review against the projections in section 3

| | |
|---|---|
| Year-one investment | **{{$pro_y1}}** |
| Projected value captured | **{{$pro_captured}}** |
| Return | **{{pro_multiple}}×** |
| Net gain, year one | **{{$pro_net}}** |

**Why we recommend this one.** It captures {{$pro_net}} of the {{$elite_net}} available under Elite — within {{X}}% — at roughly half the year-one commitment. {{One sentence on what specifically makes it the right fit for their situation.}}

### Essential — {{$ess_build}} build + {{$ess_monthly}}/month

*{{One line. "The highest-severity problem solved properly, with room to expand later."}}*

- {{Core deliverable}}
- {{Core deliverable}}
- Hosting, monitoring, and security
- {{Support terms}}

| | |
|---|---|
| Year-one investment | **{{$ess_y1}}** |
| Projected value captured | **{{$ess_captured}}** |
| Return | **{{ess_multiple}}×** |
| Net gain, year one | **{{$ess_net}}** |

### What the monthly covers

The recurring fee is operations, not maintenance. We are not being paid to keep things from breaking — we are being paid to make them measurably better each month:

- Hosting, monitoring, uptime, and security patching
- {{AI tuning against real usage — the system gets more accurate every month it runs}}
- Ongoing conversion and performance optimization against live traffic
- A monthly review of actual results against the projections in section 3

That last point is the one that matters. Every month we show you the real numbers next to the numbers in this document. If we are wrong, you will know before you have to ask.

### Terms

- {{Payment schedule — e.g. 50% to begin, 50% at launch. Retainer begins at launch.}}
- {{Retainer commitment and notice period}}
- {{Ownership: you own the code, the content, the data, and the accounts. No lock-in.}}
- {{What would change the price — the honest list of scope conditions}}

> **Writing note — delete before sending.** Present descending: Elite, Professional, Essential. Anchoring only works in that direction. Mark Professional as recommended and say why in one specific sentence about *their* business — a generic recommendation reads as an upsell, a specific one reads as advice.

---

## 5. Next Steps

1. {{Concrete action with a date — "Reply by {{date}} with the option you'd like to move forward with."}}
2. {{What happens then — "We'll send a scope document and contract within 48 hours."}}
3. {{First milestone — "Kickoff the week of {{date}}. {{First deliverable}} in your hands by {{date}}."}}

Questions before then: **hello@startrighttutoring.com**

---

## Appendix — Assumptions

{{List every assumption in the ROI model, with its source. This section exists to be checked. Being audited and surviving it is worth more than being believed on faith.}}

- {{Assumption}} — source: {{stated on discovery call / industry benchmark / conservative estimate}}
- {{Assumption}} — source: {{...}}

Where an input was uncertain, we used the conservative figure. If any of these are wrong, tell us — the model is only as good as its inputs, and we would rather correct it now than defend it later.

---
---

# INTERNAL APPENDIX — DELETE BEFORE SENDING

## Objection handling

Everything below is for you, not the client. Strip this entire section from the outgoing PDF.

### Before anything: let the silence sit

When you present price, stop talking. The first person to speak after a number loses ground. Most deals are discounted by the seller filling a four-second pause that was never an objection in the first place.

### "The price is too high."

This sentence is never information. It is one of three different objections wearing the same clothes, and answering the wrong one loses the deal. Diagnose before you respond.

**Step 1 — Reframe to the cost of delay.**

> "I understand. Let me put it next to the other number. Staying as you are costs about **{{$cost_of_delay}} a month** — that's your figure, from your close rate and your margins. Professional runs **{{$pro_monthly}} a month**. So the real question isn't whether {{$pro_monthly}} is a lot of money. It's whether you'd rather keep paying {{$cost_of_delay}} for nothing."

Then stop. Let them answer.

**Step 2 — Isolate the real objection.**

> "Can I ask which of these it actually is? Is it that the money isn't there this quarter, or that you're not convinced we'll hit those numbers? Those are completely different problems and I'd rather solve the right one."

The three real objections and what each requires:

- **Budget** — the money genuinely isn't there. Restructure payment or move down a tier. Never discount.
- **Belief** — they don't buy the projection. This is not a pricing problem. Go back to section 3 and rebuild the model with their inputs, live. Offer a reference from a comparable engagement.
- **Timing** — something else is consuming attention. Ask what would need to be true in ninety days, and price the cost of delay across that gap: `{{$cost_of_delay}} × 3`.

**Step 3 — Offer scope, never discount.**

> "I'm not going to drop the price, and here's why: I derived it from your numbers, so if I knocked six thousand off it now, you'd be right to wonder what the first number was based on. What I can do is change what we build."

In order of preference:

1. Move down a tier
2. Phase the scope — {{component one}} this quarter, {{component two}} next. Full price, sequenced.
3. Restructure payment — 40/30/30 across milestones, or lower build fee with higher retainer
4. Trade the discount for equal value — named case study, video testimonial, two warm referrals, or a 24-month term

### "We need to think about it."

> "Of course. What's the piece you want to think through? If it's the projections I'd rather work through them with you now, while I'm here to answer for them."

Then set a date before you leave the call. An unscheduled follow-up is a no with better manners.

### "We can get this cheaper elsewhere."

> "You can, and it'll probably work. The difference is what happens in month seven — whether anyone's still watching whether it's actually earning. That monthly review in section four is the whole product. The website is just what it runs on."

Do not disparage the competitor. Compete on the operating model, which is the part they cannot copy from a template.

### "Can you just do the website?"

> "Yes. That's Essential, and it's a real option. Worth knowing what it leaves behind: the site fixes {{$X}} of the {{$V}} we modeled. The other {{$Y}} is the {{other component}}, and that's the larger half. Happy to start with Essential and add the rest in Q{{N}} — I'd just want you to choose it knowing what's still on the table."

### "How do I know you'll deliver?"

> "Section three is the answer to that. Every month we put the real numbers next to the projected numbers, in front of you. If we're not hitting them, you'll know before you have to ask — and you can leave on {{notice period}} notice. I've made it deliberately easy to fire us."

### Never say

- "It's an investment, not a cost." — the ROI table already made this point. Saying it out loud makes it sound like you don't believe the table.
- "What's your budget?" — after presenting a value model, this hands the frame back.
- "Let me see what I can do." — this is a discount with extra steps, and they know it.
- Anything at all in the four seconds after you name a price.
