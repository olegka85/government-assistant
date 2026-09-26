# Execution & Accountability

Status: **Foundation v0**

Government Assistant treats an approved public initiative as unfinished until implementation and outcome are visible.

The transition from decision to execution creates an **Execution Contract**: a public, versioned record of what is expected to happen, who owns it, and how progress will be evidenced.

This is a product concept, not necessarily a legal contract. A jurisdiction may map it to legally binding instruments where applicable.

## Execution Contract

Minimum fields:

- initiative ID;
- decision ID and date;
- responsible authority;
- accountable owner role;
- implementing organization(s);
- legal/procedural basis;
- approved scope;
- budget estimate and funding status, where relevant;
- milestones;
- target dates;
- dependencies;
- procurement/project references, where public;
- outcome measures;
- evidence requirements;
- change-control rules;
- closure criteria.

## Status model

Recommended public statuses:

```text
PLANNED
FUNDED
DESIGN
PROCUREMENT
IN_PROGRESS
BLOCKED
DELAYED
PARTIALLY_DELIVERED
DELIVERED
OUTCOME_VERIFICATION
COMPLETED
CANCELLED
```

A status change does not delete the prior state.

## Milestones

Each milestone should include:

- description;
- owner;
- planned date;
- actual date;
- current status;
- evidence;
- dependency links;
- explanation when late or changed.

Example:

```text
Milestone: engineering design approved
Planned: 2027-03-01
Actual: 2027-03-19
Status: completed late
Reason: utility survey revealed undocumented line
Evidence: design approval record #...
```

## Changes

Public commitments sometimes need to change. Government Assistant should make the change explicit rather than treat the latest text as if it had always been the promise.

A material change event should record:

- previous commitment;
- new commitment;
- changed by;
- date;
- reason;
- evidence;
- budget/schedule impact;
- whether renewed approval is required.

## Rejection, deferral, and cancellation

These are accountable outcomes, not disappearing states.

A decision should distinguish:

- legally impossible;
- outside jurisdiction;
- insufficient evidence;
- infeasible;
- not funded;
- superseded/merged;
- deferred to a planning cycle;
- rejected after consultation or deliberation;
- cancelled during execution.

The reason code should be accompanied by a human-readable explanation and review path where applicable.

## Budget visibility

Where lawful and available, an execution record may show:

- approved envelope;
- current forecast;
- committed amount;
- paid amount;
- funding source;
- material variance;
- links to public procurement or financial records.

Government Assistant should not invent financial certainty when only an estimate is available.

## Evidence of implementation

Evidence can include:

- official records;
- procurement notices;
- signed acceptance records;
- inspection reports;
- geotagged or otherwise provenance-aware media;
- sensor or operational measurements;
- public datasets;
- community verification reports.

Evidence should have provenance and timestamp metadata where possible.

## Output vs. outcome

The platform distinguishes:

- **Output** — what was built, purchased, changed, or published.
- **Outcome** — whether the original public problem improved.

Example:

```text
Problem: dangerous vehicle speeds near a school
Output: raised crossing installed
Outcome measure: 85th-percentile speed during school arrival period
Verification window: 90 days before vs. 90 days after
```

An initiative can be delivered but fail its intended outcome. That should remain visible.

## Public timeline

The public history should be append-oriented:

```text
12 Jan — initiative approved
02 Feb — funding confirmed
16 Feb — design started
28 Mar — target date changed (+21 days), reason published
11 May — procurement awarded
07 Aug — construction completed
10 Nov — outcome verification published
```

## Alerts

Government Assistant may flag:

- upcoming or missed milestones;
- budget variance;
- missing evidence;
- unexplained status changes;
- contradiction between official status and linked evidence;
- an initiative marked complete without outcome verification.

AI flags are prompts for review, not automatic findings of wrongdoing.

## Accountability views

### Citizen view

Simple answers:

- What was promised?
- Who owns it?
- What happens next?
- Is it late?
- Why did it change?
- What evidence shows completion?
- Did it solve the problem?

### Official view

Operational detail:

- assigned responsibilities;
- dependencies;
- evidence requests;
- pending approvals;
- milestone updates;
- change-control workflow.

### Oversight/audit view

Traceability:

- immutable event history;
- actor/role;
- decision authority;
- AI contributions;
- data sources;
- changes and approvals;
- redactions and access logs where appropriate.

## Closure

Completion requires explicit closure criteria.

Recommended closure record:

- delivered output;
- final cost/schedule where publishable;
- outcome measurement;
- unresolved deviations;
- lessons learned;
- sign-off authority;
- links to evidence.

If the public problem remains materially unresolved, the system should allow a linked follow-up initiative rather than force a false "success" state.

## Prior art

Decidim's Accountability component demonstrates the value of linking proposals/results to implementation statuses, milestones, and progress reporting. Government Assistant extends this concept into the canonical lifecycle so execution accountability is not an optional afterthought.

See [References and Prior Art](references.md).
