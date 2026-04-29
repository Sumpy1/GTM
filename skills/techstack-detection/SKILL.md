---
name: tech-stack-detection
description: >
  Detects and validates tools an account uses across CRM, marketing automation, data warehouse,
  analytics, sales engagement, security, finance, and other GTM systems. Use when the user asks
  for technographic research, installed tools, stack fit, disqualification, enrichment, or account
  qualification based on technology signals.
---

# Tech Stack Detection

Detect account technology stack from reliable signals. Return tools, confidence, evidence, and GTM implications.

## Use When

- User wants to know what tools a company uses.
- User asks for CRM, MAP, data warehouse, analytics, sales engagement, cloud, security, or finance stack.
- User needs stack-based account qualification, disqualification, routing, enrichment, or personalization.
- User provides company domain, website, job posts, Snowflake rows, CRM records, ZoomInfo/Apollo/Clay fields, or notes.

## Detection Pattern

Useful tech stack detection separates:

- Confirmed tools: explicit evidence from job posts, docs, integrations, script tags, source data, or public pages.
- Probable tools: repeated indirect signals or strong role/tool language.
- Weak signals: generic keywords, vendor partner pages, old mentions, or ambiguous acronyms.
- GTM implication: why the tool matters for qualification, messaging, migration, integration, or competitive angle.

## Evidence To Use

Prefer source-backed signals:

- Job posts mentioning tools, certifications, systems, integrations, or admin ownership.
- Website script tags, docs, status pages, help center, privacy/subprocessor pages.
- Case studies, partner directories, marketplace listings, customer stories.
- CRM, Snowflake, enrichment fields, intent data, technographics, and implementation notes.
- Public engineering blogs, security docs, procurement docs, and API pages.

## Process

1. Define stack categories relevant to the request.
2. Extract tool mentions and normalize vendor names.
3. Classify each tool as confirmed, probable, weak, or rejected.
4. Map stack to GTM implication: fit, risk, integration angle, competitor, migration, budget owner, or disqualifier.
5. Flag stale or ambiguous evidence.

## Output Format

Return:

```markdown
## Tech Stack Detection

| Category | Tool | Confidence | Evidence | GTM implication |
|----------|------|------------|----------|-----------------|
| CRM | [Tool] | High/Med/Low | [Source-backed signal] | [Why it matters] |

## Qualification Notes

- Fit signals: [tools or stack pattern]
- Risk/disqualifier signals: [tools or missing stack]
- Personalization angle: [how to reference stack in outreach]

## Unknowns

- [Tool/category needing validation]
```

## Guardrails

- Do not infer tool usage from category keywords alone.
- Do not treat vendor website logos as proof unless source clearly names the account as customer.
- Mark evidence stale if date is old or unknown.
- Keep rejected/ambiguous tools separate from confirmed tools.
- Do not invent integrations, budgets, migrations, or renewal dates.
