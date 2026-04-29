---
name: cold-email-personalization
description: >
  Generates source-grounded cold email personalization for outbound prospecting.
  Use when the user asks for cold email openers, first lines, outbound personalization,
  persona-specific email copy, account-based email hooks, or email variants grounded in
  company news, filings, podcasts, LinkedIn posts, CRM notes, or intent signals.
---

# Cold Email Personalization

Create concise outbound email personalization from real evidence. Output usable copy plus source rationale.

## Use When

- User wants cold email first lines, openers, subject lines, or account-persona email variants.
- User provides account, persona, ICP, territory list, CRM notes, source docs, or research links.
- User needs outbound copy tied to specific business context, not generic praise.
- User asks to personalize for industry, trigger, buying committee, opportunity stage, or GTM theme.

## Personalization Pattern

Strong email personalization has:

- Relevant trigger: recent news, hiring, funding, product launch, executive change, regulation, earnings, intent, or tech signal.
- Buyer-specific pain: tied to role, team goal, metric, risk, or operational pressure.
- Clear bridge: why the trigger connects to the user's offer.
- Low-friction CTA: small ask, specific next step, or useful diagnostic.
- Natural tone: specific, direct, non-creepy.

## Evidence To Use

Prefer source-backed signals:

- Company website, press, blog, customer stories, pricing, product pages.
- 10-K, earnings call, investor deck, funding announcement, PE/investor update.
- LinkedIn posts, podcasts, webinars, conference talks.
- CRM notes, call transcripts, opportunity history, intent data, technographics.
- Job posts for RevOps, sales, growth, data, security, finance, or operations roles.

## Process

1. Identify recipient persona, company, offer, and desired CTA.
2. Extract 2-4 credible triggers or context points.
3. Map each trigger to a likely business pain or priority.
4. Write short variants. Keep first line specific and avoid false familiarity.
5. Flag weak evidence, missing persona context, or claims needing validation.

## Output Format

Return:

```markdown
## Cold Email Personalization

### Best Variant
Subject: [short subject]

Hi [Name],

[Personalized opener tied to evidence.]
[Pain/priority bridge.]
[One-sentence value prop.]
[Low-friction CTA.]

### Alternatives
- Opener 1: [copy]
- Opener 2: [copy]
- Subject options: [option], [option], [option]

## Evidence Used

| Signal | Source | Why it matters |
|--------|--------|----------------|
| [Trigger] | [Source] | [Business relevance] |

## Risks / Missing Data

- [Assumption or data gap]
```

## Guardrails

- Do not invent news, quotes, funding, customer names, metrics, or LinkedIn activity.
- Do not over-personalize with sensitive personal details.
- Keep email copy concise. Default to under 120 words unless user asks otherwise.
- Separate usable copy from rationale.
- If evidence is thin, say so and produce safer generic-but-relevant copy.
