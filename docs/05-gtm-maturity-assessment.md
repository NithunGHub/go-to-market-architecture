# 05 - GTM Maturity Assessment

A scored framework for honestly grading a go-to-market operation across six dimensions. Use it before buying tools, before reorgs, and at every planning cycle.

## How to run it

1. Gather RevOps, sales leadership, marketing leadership, and finance in one room.
2. Score each dimension 1-4 using the rubrics below. Require evidence for every score; opinions without artifacts do not count.
3. Plot the scores. The lowest dimension is your constraint; fix it before investing in the others.
4. Re-run quarterly. Progress is the delta, not the absolute score.

## The six dimensions

### 1. Data quality and governance

| Level | Looks like |
|-------|-----------|
| 1 | Duplicates everywhere, no matching rules, enrichment ad hoc, nobody trusts reports |
| 2 | Basic dedupe rules, one enrichment provider, monthly cleanup, trust is partial |
| 3 | Documented survivorship rules, enrichment waterfall, weekly hygiene cadence, field audits |
| 4 | Data contracts per object, automated quality monitoring with alerts, deprecation process for dead fields |

### 2. Systems and integrations

| Level | Looks like |
|-------|-----------|
| 1 | Point-to-point syncs, no documentation, failures discovered by reps |
| 2 | iPaaS or native connectors for core flows, partial documentation |
| 3 | Documented data contracts, error queues with owners, sandbox-tested changes |
| 4 | Event-driven architecture, versioned contracts, integration health dashboards |

### 3. Process definition

| Level | Looks like |
|-------|-----------|
| 1 | Stages exist as labels; entry/exit criteria live in people's heads |
| 2 | Lifecycle documented, some enforcement, routing and scoring rules written down |
| 3 | Exit criteria enforced by validation, SLAs measured, recycle paths defined |
| 4 | Processes versioned, change-managed, and reviewed quarterly against business motions |

### 4. Team and ownership

| Level | Looks like |
|-------|-----------|
| 1 | One overloaded admin; ownership by whoever shouts loudest |
| 2 | Named owners per system, RACI informal |
| 3 | RevOps function with charter, deal desk for non-standard deals, documented RACI |
| 4 | Specialized pods (marketing ops, sales ops, deal desk, data), career paths, on-call for critical flows |

### 5. Measurement and forecasting

| Level | Looks like |
|-------|-----------|
| 1 | Spreadsheet exports, forecast by gut feel |
| 2 | CRM dashboards, stage-based forecast, weekly inspection |
| 3 | Funnel conversion tracked stage by stage, forecast accuracy measured, cohort analysis |
| 4 | Predictive models with measured accuracy, self-serve analytics, metrics tied to decisions |

### 6. Change management

| Level | Looks like |
|-------|-----------|
| 1 | Changes made directly in production, announced never |
| 2 | Sandbox used sometimes, changes announced after the fact |
| 3 | Sandbox-first, announced with what/why/action, 30-day before/after measurement |
| 4 | Release calendar, stakeholder sign-off, rollback plans, post-change reviews |

## Scoring sheet

| Dimension | Score (1-4) | Evidence |
|-----------|-------------|----------|
| Data quality and governance | | |
| Systems and integrations | | |
| Process definition | | |
| Team and ownership | | |
| Measurement and forecasting | | |
| Change management | | |
| **Total / 24** | | |

## Reading the result

- **6-10:** Foundation work. Do not buy new tools; fix data, definitions, and ownership first.
- **11-16:** Operational. The machine works; invest in the lowest dimension and in measurement.
- **17-21:** Advanced. Focus on prediction, automation, and scale without adding headcount linearly.
- **22-24:** Verify with an outside audit. Almost nobody scores here honestly.

## 90-day improvement plan

Pick the single lowest dimension. Write three moves: one fix (this month), one system (next month), one habit (ongoing). Assign one owner. Review in 90 days with the same rubric. Repeat.
