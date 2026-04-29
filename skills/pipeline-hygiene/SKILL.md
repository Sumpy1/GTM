---
name: pipeline-hygiene
description: >
  Audits CRM pipeline health by flagging stalled deals, missing close dates, inflated stages,
  stale next steps, weak MEDDPICC fields, and forecast risk. Use when the user asks for pipeline
  hygiene, CRM cleanup, forecast inspection, deal risk review, rep coaching, or opportunity cleanup.
---

# Pipeline Hygiene

Find pipeline quality problems and recommend cleanup actions by deal, rep, stage, and forecast impact.

## Use When

- User wants pipeline hygiene, CRM cleanup, opportunity inspection, or forecast risk review.
- User provides opportunity exports, CRM rows, forecast calls, stage history, notes, close dates, next steps, or MEDDPICC fields.
- User asks to identify stalled deals, inflated stages, missing close dates, weak next steps, or dirty CRM data.
- User needs rep-level cleanup actions before forecast call, QBR, board update, or pipeline review.

## Hygiene Pattern

Pipeline risk often shows as:

- Stale activity: no next step, old last touch, no meeting scheduled, no recent buyer engagement.
- Stage mismatch: late stage without champion, pain, decision process, commercial event, or mutual action plan.
- Close date risk: close date in past, pushed repeatedly, end-of-quarter clustering, or no close date.
- Forecast inflation: commit/best-case without evidence, large deal with missing MEDDPICC, or stale amount.
- Data gaps: missing account, owner, source, amount, stage, persona, next step, or competitor.

## Evidence To Use

Prefer CRM/source-backed signals:

- Opportunity fields: stage, amount, close date, forecast category, owner, age, last activity, next step.
- Stage history, close date push count, activity history, meeting notes, call transcripts.
- MEDDPICC fields, buying committee, champion status, decision criteria, paper process.
- Account fit, intent, source, campaign, product line, renewal/expansion context.

## Process

1. Confirm review scope: team, rep, territory, segment, period, stage, and forecast category.
2. Normalize opportunity records and identify missing critical fields.
3. Apply hygiene checks by stage and forecast category.
4. Prioritize cleanup by revenue impact, forecast risk, and ease of action.
5. Recommend concrete next action per deal or rep.

## Output Format

Return:

```markdown
## Pipeline Hygiene Review

| Priority | Deal | Owner | Issue | Evidence | Cleanup action | Forecast impact |
|----------|------|-------|-------|----------|----------------|-----------------|
| High | [Opportunity] | [Rep] | [Risk] | [Field/source] | [Specific action] | [Commit/Best case/Pipeline impact] |

## Rep Actions

- [Rep]: [cleanup task], [deadline or review point]

## Data Quality Fixes

- [Field/process issue]: [recommended fix]

## Forecast Risks

- [Risk summary]
```

## Guardrails

- Do not mark deals risky without evidence.
- Do not change forecast category unless stage evidence supports it.
- Separate CRM data quality problems from real deal risk.
- Preserve rep/account context and avoid generic "follow up" recommendations.
- If key fields are missing, list missing data before making strong conclusions.
