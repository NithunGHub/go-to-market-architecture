# Go-to-Market Architecture

How modern SaaS go-to-market stacks are designed, integrated, and operated.

This repo is a working reference for GTM systems architecture: the layers of the modern SaaS stack, how the CRM acts as the system of record, how data flows between systems, and how a RevOps function keeps it all honest. It is written from real-world experience building and running Salesforce-centered GTM operations.

## Who this is for

- RevOps / Sales Ops / Marketing Ops practitioners designing or auditing a GTM stack
- Salesforce architects mapping business process to platform design
- Founders and GTM leaders buying their first serious stack (or untangling the one they have)

## Contents

| Doc | What it covers |
|-----|---------------|
| [01 - The Modern GTM Stack](docs/01-the-modern-gtm-stack.md) | The five layers of a SaaS GTM stack, what each layer owns, and how they connect |
| [02 - CRM as System of Record](docs/02-crm-as-system-of-record.md) | Why the CRM wins as source of truth, object-model thinking, and data governance |
| [03 - Data Flow Reference Architecture](docs/03-data-flow-reference-architecture.md) | Reference diagrams: lead flow, opportunity flow, and integration patterns |
| [04 - RevOps Operating Model](docs/04-revops-operating-model.md) | The operating cadence, metrics tree, and ownership model that keep the stack working |

## Guiding principles

1. **The CRM is the system of record.** Every other tool feeds it or reads from it. If a number matters, it lives in the CRM.
2. **Data flows in one direction per object.** Bidirectional sync on the same fields is where GTM data goes to die.
3. **Automate the routine, gate the judgment calls.** Speed-to-lead is automation. Deal qualification is a human decision supported by data.
4. **Instrument before you optimize.** You cannot fix funnel conversion you cannot measure stage by stage.

## Contributing

This is a living reference. Open an issue or PR with corrections, war stories, or patterns you have seen work.
