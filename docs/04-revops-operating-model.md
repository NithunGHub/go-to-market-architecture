# 04 - RevOps Operating Model

Tools do not run themselves. RevOps is the operating function that keeps the GTM stack aligned to how the business actually sells. This doc describes the model: charter, cadence, metrics, and ownership.

## Charter

RevOps owns the **design and reliability of the revenue process**: the lifecycle definitions, the routing and scoring logic, the forecast methodology, and the data the business runs on. RevOps does not own the number; it owns the machine that produces the number.

## Operating cadence

| Ritual | Cadence | Purpose |
|--------|---------|---------|
| Funnel review | Weekly | Stage-by-stage conversion, fallout, SLA adherence |
| Forecast call | Weekly | Commit / best-case / pipeline inspection by stage and age |
| Data hygiene triage | Weekly | Duplicates, sync errors, routing exceptions |
| Stack review | Monthly | Tool utilization, contract renewals, integration health |
| Lifecycle audit | Quarterly | Are stage definitions still true? Retire dead stages and fields |
| Planning | Annually | Territories, quotas, comp plans reflected in systems before Jan 1 |

## Metrics tree

Every metric rolls up to revenue. If it does not, it is trivia.

```
Revenue
├── Pipeline created (by source, by segment)
│   ├── MQLs → SQLs → Opportunities (conversion at each gate)
│   └── Speed-to-lead, follow-up attempts
├── Pipeline quality
│   ├── Win rate by stage, segment, source
│   ├── Sales cycle length
│   └── Average deal size
└── Customer revenue
    ├── Gross and net retention
    ├── Expansion pipeline
    └── Time-to-value / onboarding completion
```

## Ownership model

| Decision | Owner | Consulted |
|----------|-------|-----------|
| Lifecycle stage definitions | RevOps | Sales + Marketing leadership |
| Scoring model changes | Marketing Ops | SDR leadership |
| Routing rules | RevOps | Sales leadership |
| Required fields / validation | RevOps | Reps (they pay the tax) |
| New tool purchases | RevOps (technical fit) | Finance (commercial) |
| Forecast methodology | RevOps | CRO / CFO |

## Change management

GTM systems change constantly: new segments, new products, new motions. The discipline is boring and non-negotiable:

1. **Sandbox first.** No lifecycle, routing, or scoring change goes to production untested.
2. **Announce the change** with what changed, why, and what reps must do differently. One paragraph, not a wiki.
3. **Measure the before/after** for 30 days. Revert what does not improve.

## Maturity checkpoints

- Level 1: CRM exists; reporting is spreadsheet exports.
- Level 2: Defined lifecycle, basic routing and scoring, weekly funnel review.
- Level 3: Integrated stack with documented data contracts, deal desk, forecast rigor.
- Level 4: Warehouse-centric, predictive scoring, self-serve analytics, AI-assisted workflows with measured error rates.

Most companies overestimate by one level. Audit honestly before buying the next tool.
