# 02 - CRM as System of Record

"System of record" gets thrown around loosely. Here is the working definition: for any business object, the system of record is the one system whose value wins in a conflict, and every downstream consumer reads from it.

## Why the CRM wins

In B2B SaaS, revenue truth is relational: people belong to accounts, accounts have opportunities, opportunities have products and close dates. Only the CRM models all of those relationships natively. Marketing automation knows touches. Billing knows invoices. The CRM knows the customer.

## Object-model thinking

Design the data model around the questions leadership asks:

| Question | Object that answers it |
|----------|----------------------|
| How many qualified leads did we create? | Lead (with a strict lifecycle) |
| What is our pipeline coverage? | Opportunity (with enforced stage exit criteria) |
| Which accounts are we penetrating? | Account + Contact roles |
| Where did this deal come from? | Campaign influence on Opportunity |
| What did we actually sell? | Quote / Order / Contract linked to the Opportunity |

Rules that keep the model honest:

1. **One lifecycle per object, with entry/exit criteria.** A lead stage nobody can define is a stage that should not exist.
2. **Required fields only where they gate a decision.** Every required field is a tax on the rep; spend that tax on fields used in routing, scoring, or forecasting.
3. **Contacts belong to accounts. Always.** Contact-only selling creates attribution debt you will pay at renewal time.
4. **Dedupe is a process, not a tool.** Matching rules catch the obvious; survivorship rules decide which value wins; a human reviews the rest on a cadence.

## Data ownership

| Domain | Owner | Notes |
|--------|-------|-------|
| Account hierarchy, territory fields | RevOps | Changes need change control; they reroute pipeline |
| Contact data quality | Marketing Ops + enrichment | Automated first, human review on exceptions |
| Opportunity stages and amounts | Sales, enforced by validation | Reps own accuracy; RevOps owns the definitions |
| Product catalog and pricing | Deal desk / Finance | Sales never edits price books directly |

## Governance cadence

- **Weekly:** duplicate review queue, sync error triage, routing fallout.
- **Monthly:** field utilization audit (fields nobody uses get deprecated), lifecycle conversion review.
- **Quarterly:** object-model review against new business motions (new segment, new product, new channel).

## The test

Pick any closed-won deal. Can you trace it from first touch to invoice using only CRM data, with no Slack archaeology? If yes, your system of record works. If not, you have a filing cabinet, not a system of record.
