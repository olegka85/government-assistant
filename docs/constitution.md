# Government Assistant Constitution

Status: **Foundation v0**

This document defines non-negotiable product and governance constraints for Government Assistant. Jurisdiction-specific deployments may add stricter rules, but should not silently weaken these guarantees.

## 1. Purpose

Government Assistant exists to help communities and public institutions turn public problems and proposals into transparent, evidence-backed, lawfully decided, and accountable outcomes.

The system may reduce administrative friction and routine coordination. It must not create an unelected AI authority.

## 2. Authority

AI has no inherent political, legal, or administrative mandate.

A deployment must identify, for every consequential action:

- the lawful decision-maker;
- the legal or procedural basis for the decision;
- whether human approval is required;
- what can be appealed or corrected;
- what evidence and reasoning must be retained.

Where law reserves a decision to a person, elected body, court, commission, public authority, or other institution, Government Assistant may prepare or support that decision but does not inherit the authority.

## 3. Problem-first treatment

The system evaluates an initiative by its public substance, evidence, scope, effects, feasibility, and applicable procedure.

The proposer's identity is provenance, not rank.

The system must not boost or suppress an otherwise equivalent initiative merely because it was proposed by:

- a politician or party;
- an incumbent or challenger;
- an official;
- a company or donor;
- a celebrity or influencer;
- a highly followed user;
- an anonymous or little-known resident.

Conflicts of interest, sponsorship, organizational affiliation, and official authorship may be displayed where relevant to transparency.

## 4. AI role

AI may:

- turn unstructured reports into structured problem statements;
- detect likely duplicates and related initiatives;
- summarize evidence and arguments;
- identify missing information;
- suggest alternative solutions;
- identify likely jurisdictions or responsible bodies;
- explain procedures;
- translate and improve accessibility;
- prepare non-binding drafts;
- monitor milestones and flag discrepancies;
- help compare outcomes against stated objectives.

AI must not:

- cast a citizen's vote, endorsement, signature, or consent;
- impersonate a citizen or public official;
- fabricate evidence, supporters, consensus, or implementation progress;
- independently impose a legal sanction, deprivation, entitlement denial, or other decision reserved to lawful authority;
- secretly manipulate initiative visibility based on political alignment or proposer identity;
- perform personalized political persuasion or microtargeting on behalf of a candidate, party, government, or interest group;
- suppress material counter-evidence from a decision record;
- conceal uncertainty or material conflicts of interest;
- make irreversible consequential actions without the authorization required by the applicable procedure.

## 5. Participation is not one mechanism

Government Assistant does not assume that every public question should be settled by a simple online majority vote.

A process may use, where lawful and appropriate:

- information and civic monitoring;
- consultation;
- proposal support thresholds;
- participatory budgeting;
- representative deliberation;
- administrative decision with public input;
- legislative consideration;
- a legally established ballot, referendum, or other formal vote.

The chosen mechanism, eligibility rules, thresholds, and legal effect must be visible before participation begins.

## 6. Rights and safeguards

Popularity alone cannot override rights, due process, constitutional constraints, anti-discrimination rules, or other applicable law.

The platform must distinguish between:

- people affected by a question;
- people invited to deliberate or provide evidence;
- people legally eligible to make or participate in a binding decision.

These sets may overlap but are not automatically identical.

## 7. Evidence and plural alternatives

For consequential initiatives the platform should expose:

- the problem statement;
- source evidence and its provenance;
- uncertainty and missing evidence;
- materially different feasible alternatives;
- costs and constraints where available;
- expected benefits and adverse effects;
- distributional effects where material;
- arguments and counterarguments;
- the decision mechanism and responsible authority.

AI-generated content must be identifiable as such.

## 8. Traceability

Every consequential AI-assisted step should generate a durable audit event containing, as appropriate:

- initiative and process identifiers;
- input references;
- rule or policy version;
- model/provider/version identifier;
- generated recommendation or transformation;
- human edits;
- approval or rejection;
- actor and role;
- timestamp;
- reason code;
- linked evidence.

The public view may redact protected data, but an authorized audit trail must preserve accountability.

## 9. Contestability and correction

People must have practical ways to:

- correct factual errors about an initiative;
- challenge incorrect merging or categorization;
- contest eligibility or affected-community determinations where the process permits;
- see why an initiative was rejected, deferred, merged, or rerouted;
- appeal or request review when applicable law or procedure provides it.

AI output is never exempt from correction merely because it was generated automatically.

## 10. Execution accountability

Acceptance is not closure.

An accepted initiative should transition into an execution record with:

- responsible authority;
- decision and legal basis;
- budget or funding status when relevant;
- milestones;
- dependencies;
- target dates;
- implementation evidence;
- changes and reasons;
- outcome measures;
- closure criteria.

A missed deadline or changed commitment remains part of the history.

## 11. Privacy and security

Deployments should follow data minimization and purpose limitation.

Public participation does not imply public exposure of sensitive personal data. Identity verification, eligibility verification, public display name, and audit identity should be separable concerns.

High-risk administrative systems and public participation systems require explicit trust boundaries, access controls, tamper-evident logs, and incident handling.

## 12. Portability and institutional independence

The reference platform should be:

- self-hostable;
- model-agnostic;
- based on documented interfaces;
- exportable in open formats where practical;
- able to replace AI providers without rewriting the civic process;
- able to run core non-AI workflows when AI services are unavailable.

No provider should become the de facto holder of public authority through technical lock-in.

## 13. Power matrix

Each capability must be classified before production use.

| Level | Meaning | Example |
|---|---|---|
| A | AI may perform automatically | deduplicate likely identical reports, with reversible review |
| B | AI may perform and notify | route a non-binding issue to the likely responsible queue |
| C | AI prepares; authorized human approves | publish an official response or approve an execution change |
| D | AI informs only | rights-affecting, legally reserved, or politically authoritative decision |

The matrix is deployment- and jurisdiction-specific. A feature must default to the more restrictive level when authority is unclear.

## 14. No hidden agenda engine

Ranking, recommendation, notification, and feed logic are part of governance.

A deployment must document the main factors used to determine:

- which initiatives are shown;
- which people are notified;
- which initiatives are grouped;
- what becomes trending or urgent;
- what enters an official queue.

Political alignment, private persuasion profiles, or payment must not be hidden ranking factors in a public decision process.

## 15. Definition of success

Success is not measured by replacing officials or maximizing votes.

Useful measures include:

- time from problem report to responsible-owner assignment;
- duplicate reports consolidated;
- evidence completeness;
- participation breadth and accessibility;
- response and decision latency;
- percentage of accepted initiatives with current execution data;
- milestone reliability;
- verified outcomes;
- rate and resolution of corrections and appeals;
- administrative effort saved without loss of accountability.
