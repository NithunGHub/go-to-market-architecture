# 01 - The Modern GTM Stack

A SaaS go-to-market stack has five layers. Most companies buy tools layer by layer as pain appears, which is why the average stack looks accidental. This doc describes the layers as they should fit together.

## The five layers

```
Engagement      Marketing automation, sales engagement, ads, chat, events
      |
System of Record   CRM (Salesforce / HubSpot): accounts, contacts, opportunities
      |
Transaction     CPQ, contract lifecycle, billing, provisioning
      |
Data Foundation CDP / warehouse, enrichment, identity resolution, ETL / iPaaS
      |
Intelligence    BI, forecasting, conversation intelligence, AI agents
```

### 1. Engagement layer

Tools that create and work pipeline: marketing automation (nurture, scoring inputs), sales engagement (sequences, dialer), advertising platforms, chat/event tools.

- Owns: touches, sequences, campaign execution.
- Feeds the CRM: activities, campaign membership, engagement scores.
- Common failure: engagement data that never lands on the lead/contact record, so attribution and routing run blind.

### 2. System of record (CRM)

One place where the truth about customers and pipeline lives. In B2B SaaS this is almost always Salesforce or HubSpot.

- Owns: account/contact/lead records, opportunity stages, forecast, customer lifecycle state.
- Everything else integrates to it. See [02 - CRM as System of Record](02-crm-as-system-of-record.md).

### 3. Transaction layer

CPQ (configure-price-quote), contract redlining / e-signature, billing, and provisioning. This is where pipeline becomes revenue.

- Owns: price integrity, approval chains, order accuracy, invoice correctness.
- Feeds the CRM: closed-won details, ARR/MRR, contract terms for expansion and renewal motions.

### 4. Data foundation

Customer data platform or warehouse, enrichment providers, and the integration fabric (iPaaS, event bus, or native connectors).

- Owns: identity resolution (is this the same person/company?), enrichment freshness, sync reliability.
- This layer is invisible when it works and the root cause of nearly everything when it does not.

### 5. Intelligence layer

BI dashboards, forecasting models, conversation intelligence, and increasingly AI agents that draft, summarize, and route.

- Owns: insight, not action. Agents should propose and log; humans approve until the error rate is measured and acceptable.

## Build vs. buy guidance

| Situation | Guidance |
|-----------|----------|
| Under ~$5M ARR | CRM + marketing automation + a billing tool. Resist the CDP and the data warehouse until funnel volume forces it. |
| $5M - $50M ARR | Add enrichment, sales engagement, CPQ-lite or approval flows, and a real integration layer. This is where RevOps becomes a function, not a person. |
| $50M+ ARR | Warehouse-centric architecture, formal data contracts between teams, deal desk, and dedicated systems for renewals and expansion. |

## Anti-patterns

- **Tool-first architecture.** Buying the engagement tool before defining the lead lifecycle it must support.
- **Two systems of record.** Marketing automation and CRM both claiming to own lead status. Pick one per object and enforce it.
- **Integration spaghetti.** Point-to-point syncs with no documented owner. After three tools, use an iPaaS or event bus.
- **Vanity instrumentation.** Dashboards nobody opens during forecast or funnel review. If a metric has no decision attached, delete it.
