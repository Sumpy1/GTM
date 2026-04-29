---
name: company-discovery
description: >
  Finds and prioritizes upmarket companies that are struggling to find repeatable GTM motion.
  Use when the user asks for company discovery, upmarket account selection, GTM motion diagnosis,
  ICP expansion, prospecting shortlists, or accounts likely to need clearer segmentation,
  messaging, channel mix, sales motion, or route-to-market strategy.
---

# Company Discovery

Find upmarket companies with visible GTM confusion. Output prospecting shortlist plus why each company likely needs GTM motion help.

## Use When

- User wants companies in upmarket, enterprise, or expansion-stage segments.
- User wants targets struggling with ICP, messaging, channel mix, sales motion, segment focus, or route-to-market.
- User asks for company discovery, prospecting accounts, ICP expansion, or "who should we go after?"
- User needs evidence-backed account prioritization, not generic company lists.

## Target Pattern

Best-fit companies show several signals:

- Upmarket motion exists or is emerging: enterprise customers, larger ACV, multi-stakeholder buying, complex procurement.
- GTM motion looks unsettled: broad positioning, many segments, unclear buyer, mixed PLG/sales-led language, or frequent packaging changes.
- Growth pressure visible: leadership changes, new funding, PE ownership, slowing growth, new regions, partner push, or sales hiring.
- Market has urgency: category noise, consolidation, security/compliance pressure, cost pressure, or AI/data modernization.
- Company likely benefits from sharper ICP, messaging, routing, segmentation, pipeline focus, or buyer mapping.

## Evidence To Use

Prefer source-backed signals:

- Website positioning, product pages, pricing, customer pages, case studies.
- Job posts for sales, RevOps, growth, partnerships, enterprise AE, SDR, demand gen, product marketing.
- Funding, ownership, acquisitions, leadership changes, earnings, investor updates.
- Tech stack, intent data, CRM fields, Snowflake rows, ZoomInfo/Apollo/Clay fields when available.
- News, press releases, LinkedIn posts, G2/category pages, partner directories.

## Process

1. Define upmarket lens: segment, ACV, buyer, geography, industry, and excluded company types.
2. Build candidate pool from provided data first. If no data, state needed sources before broad research.
3. Score each company on:
   - Upmarket readiness
   - GTM motion confusion
   - Timing/urgency
   - Fit to user's offer or ICP
   - Evidence quality
4. Prioritize companies with both pain and ability to buy. Do not over-rank tiny companies with noisy signals.
5. Produce shortlist with crisp rationale and recommended entry angle.

## Output Format

Return:

```markdown
## Company Discovery Shortlist

| Rank | Company | Why now | GTM motion gap | Entry angle | Evidence | Confidence |
|------|---------|---------|----------------|-------------|----------|------------|
| 1 | [Company] | [Timing signal] | [Likely GTM issue] | [Suggested wedge] | [Source-backed evidence] | High/Med/Low |

## Recommended Plays

- [Company]: [specific prospecting or discovery motion]

## Risks / Missing Data

- [Assumption or data gap]
```

## Guardrails

- Do not invent funding, headcount, customers, intent, or tech stack.
- Separate observed evidence from inferred GTM motion gaps.
- Avoid generic "high growth company" claims. Tie each recommendation to a concrete signal.
- If evidence is weak, mark confidence low and say what would validate it.
- Prefer fewer high-quality accounts over long undifferentiated lists.