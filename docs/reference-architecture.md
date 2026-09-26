# Reference Architecture

Status: **Foundation v0**

Government Assistant is designed as a replaceable, self-hostable reference architecture. The civic process must not depend on one AI provider or one deployment vendor.

## Logical architecture

```text
+-------------------------------------------------------------+
| Interfaces                                                  |
| Citizen Web/Mobile | Official Workspace | Public Dashboard  |
| Oversight/Audit    | Public API          | Notifications     |
+-----------------------------+-------------------------------+
                              |
+-----------------------------v-------------------------------+
| Civic Process Core                                           |
| Initiative Registry | Lifecycle Engine | Decision Router     |
| Community Resolver  | Evidence Registry | Alternative Model   |
| Execution Tracker   | Appeals/Corrections | Notification Rules |
+-----------------------------+-------------------------------+
                              |
+-----------------------------v-------------------------------+
| Trust & Governance                                           |
| Identity/Eligibility | Roles/Authority | Policy/Rules         |
| Audit Ledger         | Consent/Privacy  | Abuse Prevention     |
+-----------------------------+-------------------------------+
                              |
+-----------------------------v-------------------------------+
| AI Assistance Layer                                          |
| Intake Structuring | Semantic Dedup | Summaries              |
| Option Discovery   | Evidence Extraction | Translation        |
| Risk/Gap Flags     | Model Gateway | Evaluation/Guardrails   |
+-----------------------------+-------------------------------+
                              |
+-----------------------------v-------------------------------+
| Integrations                                                 |
| GIS | Public Registries | Budgets | Procurement | Open Data   |
| Document Systems | Identity Providers | Messaging | Sensors    |
+-------------------------------------------------------------+
```

## 1. Initiative Registry

Canonical record for:

- problem;
- proposals/alternatives;
- scope;
- provenance;
- relationships;
- current lifecycle state;
- linked process;
- linked decision;
- linked execution record.

The registry should use stable IDs. Human-readable titles may change without changing identity.

## 2. Lifecycle Engine

Controls allowed state transitions.

The lifecycle is deterministic policy logic where possible. AI may suggest a transition or missing requirement, but should not silently bypass required procedural states.

## 3. Decision Router

Maps an initiative to the applicable process.

Inputs:

- jurisdiction;
- category;
- authority rules;
- rights impact;
- budget;
- scale;
- urgency;
- technical/risk classification.

Outputs:

- responsible authority;
- participation mechanism;
- eligibility model;
- approval requirements;
- appeal/review route.

Rules should be versioned.

## 4. Community Resolver

Builds transparent participation sets for notification, consultation, deliberation, support, and decision eligibility.

Possible inputs:

- GIS boundaries;
- service catchments;
- transit routes;
- utility/network topology;
- verified relationship to a service;
- administrative districts;
- policy rules.

AI may propose semantic relationships but should not be the sole source of legal eligibility.

## 5. Evidence Registry

Evidence is stored or referenced with provenance.

Suggested fields:

```text
evidence_id
initiative_id
type
source
source_uri
submitted_by
observed_at
published_at
geography
integrity_hash
verification_state
visibility
supersedes
```

The platform should distinguish source material from AI summaries of that material.

## 6. Alternative Model

A problem may have zero, one, or many proposed solutions.

```text
Problem 1
  |- Alternative A
  |- Alternative B
  |- Alternative C
  \- No-action / monitor option
```

This avoids turning the first submitted solution into the definition of the problem.

## 7. Identity and eligibility

Separate concerns:

- account identity;
- real-person verification;
- residency/service eligibility;
- legal voting eligibility;
- public profile/pseudonym;
- official organizational role.

A system should avoid exposing private verification data merely to prove that a public action was valid.

## 8. Audit Ledger

Use append-only event semantics for consequential events.

Recommended properties:

- event ID;
- entity ID;
- event type;
- actor;
- actor role;
- timestamp;
- previous-state reference;
- payload hash;
- policy/rule version;
- AI/model metadata where applicable;
- approval reference.

Tamper evidence may be implemented using cryptographic hashes/signatures; the architecture does not require a blockchain.

## 9. AI Assistance Layer

AI is an adapter around civic workflows, not the source of authority.

All AI providers should sit behind a Model Gateway so deployments can:

- switch models;
- route by sensitivity;
- use local models;
- disable external providers;
- record model/version;
- evaluate task quality;
- enforce data boundaries.

Core workflows must have non-AI fallbacks.

## 10. Ranking and recommendation

Feeds and notifications can shape public attention, so ranking is a governance surface.

Prefer explainable filters such as:

- geography followed;
- initiative state;
- official deadline;
- verified urgency/safety category;
- explicit user subscriptions;
- process eligibility.

If algorithmic ranking is used, its significant factors should be documented and reviewable.

Do not build political ideology profiles for civic-feed ranking or persuasion.

## 11. Integration boundary

Adapters should isolate external systems.

Examples:

```text
GISAdapter
RegistryAdapter
BudgetAdapter
ProcurementAdapter
IdentityAdapter
DocumentAdapter
NotificationAdapter
OpenDataAdapter
```

Each adapter should expose source freshness, authorization scope, and failure state. Missing external data must not silently become "no issue".

## 12. Deployment profiles

### Reference/demo

Synthetic data, no binding decisions, no real eligibility.

### Municipal pilot

One jurisdiction, limited initiative categories, real officials, explicit non-binding or narrowly authorized processes.

### Production public authority

Formal identity/eligibility, records management, security controls, accessibility, legal retention, audit/appeal processes, disaster recovery, operational monitoring, and jurisdiction-specific approvals.

## 13. Data classes

At minimum distinguish:

- public;
- internal administrative;
- personal;
- sensitive personal;
- security-sensitive;
- legally restricted.

AI-provider routing and logging policy should depend on data class.

## 14. Availability philosophy

Loss of AI capability should degrade assistance, not erase civic records.

If the model gateway is unavailable:

- initiatives remain readable;
- evidence remains accessible subject to permissions;
- legal workflows remain enforceable;
- decisions and execution history remain available;
- officials can continue manual processing.

## 15. Initial implementation boundary

Foundation v0 intentionally excludes:

- production identity verification;
- binding online voting;
- direct writes to government registries;
- autonomous budget allocation;
- autonomous sanctions or benefit decisions;
- production procurement actions.

The first implementation should validate the public problem -> initiative -> process -> execution information model before adding consequential integrations.
