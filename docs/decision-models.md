# Decision Models

Status: **Foundation v0**

Government Assistant must not assume that all public questions are best decided through the same mechanism.

The platform's job is to route an issue into a legitimate, transparent process and make the process understandable.

## Decision Router

Before opening a binding or quasi-binding process, determine:

1. **Authority** — who is legally empowered to decide?
2. **Legal effect** — advisory, administrative, budgetary, legislative, electoral, or other?
3. **Eligibility** — who may legally participate in a binding step?
4. **Affected community** — who should be informed or consulted?
5. **Rights impact** — can majority preference lawfully settle the question?
6. **Budget impact** — is money allocated, constrained, or merely estimated?
7. **Technical complexity** — what expert evidence is needed?
8. **Distributional impact** — who benefits, pays, or bears externalities?
9. **Reversibility** — how difficult is it to reverse the decision?
10. **Urgency** — is an emergency procedure lawfully available?
11. **Existing procedure** — does law already prescribe hearings, consultations, procurement, environmental review, council votes, referenda, or another process?

## Supported process families

### A. Information and civic monitoring

Use when the main public value is visibility and accountability.

Examples:

- track road repair progress;
- monitor an adopted program;
- publish milestones and evidence.

Public interaction may add observations or corrections without deciding the underlying authority.

### B. Consultation

Use when an authorized body seeks input before making a decision.

The platform must clearly label consultation as consultation. It should not imply that a popular comment is automatically binding.

Outputs may include:

- themes;
- support/opposition by argument;
- alternative suggestions;
- evidence submissions;
- official response to material issues raised.

### C. Proposal support threshold

Use to decide whether an initiative advances to deeper review, not necessarily whether it is finally adopted.

A threshold should define:

- eligible supporters;
- time window;
- verification method;
- geographic or jurisdictional scope;
- what happens after the threshold is reached.

Thresholds are agenda-setting rules, not an automatic grant of public authority.

### D. Participatory budgeting

Use where a public body has explicitly allocated a budget for participatory selection.

The process needs:

- a fixed budget envelope;
- eligibility rules for projects;
- cost estimation;
- feasibility screening;
- selection rule;
- conflict handling when chosen projects exceed budget;
- implementation tracking.

### E. Representative deliberative process

Use for complex or contested questions where informed discussion across a broadly representative group is valuable.

The process can include:

- transparent selection or sortition rules;
- balanced evidence;
- facilitated deliberation;
- expert questioning;
- documented recommendations;
- a clear statement of how the authorized institution will respond.

### F. Administrative decision with participation

Use when an executive or administrative authority lawfully owns the decision but public evidence or consultation is relevant.

Government Assistant can organize the public record and prepare decision material, but the official decision must identify its authorized signer/body and reasons.

### G. Legislative route

Use when the proposal requires a law, ordinance, regulation, or other legislative action.

The system may support drafting, consultation, committee/meeting records, amendments, and public tracking. It must preserve the formal legislative authority and procedure.

### H. Formal public vote

Use only where a legally valid ballot, referendum, poll, election, or other voting mechanism is authorized for the decision in question.

A production deployment must define:

- voter eligibility;
- identity and anti-duplication controls;
- ballot secrecy where required;
- observation/audit requirements;
- counting and certification;
- dispute process;
- legal effect.

Government Assistant should not invent binding voting authority merely because a digital poll is technically easy to create.

## Mechanisms can compose

A single initiative may pass through several mechanisms:

```text
report
 -> support threshold
 -> feasibility review
 -> deliberation
 -> participatory budget vote
 -> formal administrative approval
 -> execution monitoring
```

The UI should distinguish each phase so users know exactly what their action means.

## Decision record

Every consequential decision should expose, subject to lawful redactions:

- process type;
- authority;
- eligibility rules;
- participation window;
- threshold or aggregation rule;
- result;
- official decision;
- reasons;
- evidence considered;
- dissent/minority report where the process supports it;
- next step;
- review or appeal route.

## Reference basis

The OECD's citizen-participation guidance distinguishes multiple participation methods, including consultations, open innovation, civic monitoring, participatory budgeting, and representative deliberative processes. Government Assistant uses the same broad principle: choose a method appropriate to the question rather than treating participation as a universal up/down vote.

See [References and Prior Art](references.md).
