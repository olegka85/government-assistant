# Initiative Lifecycle

Status: **Foundation v0**

The core object in Government Assistant is a public problem or initiative with a durable lifecycle.

## Canonical lifecycle

```text
INTAKE
  -> STRUCTURED
  -> DEDUPLICATED / LINKED
  -> SCOPED
  -> EVIDENCE_OPEN
  -> OPTIONS_OPEN
  -> PROCEDURE_SELECTED
  -> DELIBERATION
  -> DECISION
  -> EXECUTION
  -> OUTCOME_VERIFICATION
  -> CLOSED
```

Additional terminal or side states include:

```text
REJECTED
WITHDRAWN
MERGED
DEFERRED
OUT_OF_SCOPE
APPEALED
REOPENED
```

A deployment may add jurisdiction-specific states, but it should preserve the event history rather than overwrite prior states.

## 1. Intake

A person, organization, public body, sensor-backed system, meeting, or imported dataset may surface a problem or proposal.

The intake can be informal:

> "Cars drive too fast here and children cross the road."

The user should not need to know the responsible agency, legal category, program name, or form number.

The system records provenance and separates:

- observed problem;
- proposed solution;
- location or scope;
- supporting material;
- urgency claim;
- author/source.

## 2. Structuring

AI may transform the submission into a draft structured record:

- title;
- problem statement;
- proposed solution, if any;
- geography or affected system;
- category;
- evidence references;
- safety/urgency indicators;
- possible responsible authorities.

The submitter should be able to correct the structured interpretation.

## 3. Duplicate and relationship detection

The platform searches for:

- exact duplicates;
- same underlying problem with different wording;
- competing solutions to the same problem;
- a parent/child relationship;
- dependency or conflict with another initiative.

Merging must preserve provenance. Support, evidence, comments, and authorship should not silently disappear.

## 4. Scope and affected community

The system determines a draft scope:

- geographic area;
- service area;
- user group;
- budgetary or administrative scope;
- potentially affected communities;
- responsible jurisdiction.

This determination must be explainable and reviewable. Geographic distance alone is not sufficient for every issue.

See [Affected Community](affected-community.md).

## 5. Evidence opening

The process gathers and distinguishes:

- verified official data;
- submitted documents;
- measurements and observations;
- expert assessments;
- photos/video with provenance where available;
- prior decisions and plans;
- estimates;
- claims not yet verified.

The interface should show uncertainty instead of flattening all material into one confidence level.

## 6. Alternatives

The platform separates the **problem** from any single **solution**.

Example:

Problem: unsafe pedestrian crossing.

Possible alternatives:

- traffic calming;
- signalized crossing;
- raised crossing;
- route redesign;
- enforcement changes;
- no-build option plus monitoring.

AI may help surface options, but materially different feasible alternatives should not be hidden merely because the original proposer named one preferred solution.

## 7. Procedure selection

A Decision Router determines the appropriate lawful process.

Inputs may include:

- legal authority;
- rights impact;
- budget size;
- reversibility;
- technical complexity;
- distributional effects;
- geographic scale;
- urgency;
- existing statutory or administrative procedure.

Output includes:

- responsible authority;
- participation method;
- who may participate;
- what participation changes;
- thresholds;
- decision-maker;
- appeal/review route;
- expected timeline.

See [Decision Models](decision-models.md).

## 8. Deliberation

The platform supports structured consideration rather than a single popularity counter.

A process may include:

- questions and answers;
- evidence requests;
- pro/con arguments;
- expert input;
- public meetings;
- representative panels;
- alternative comparison;
- amendments;
- costed variants.

Notifications should target materially affected or eligible participants based on published rules, not political persuasion profiles.

## 9. Decision

The decision record must state:

- what was decided;
- by whom or by which mechanism;
- applicable authority/procedure;
- participation result, where relevant;
- accepted/rejected alternatives;
- material reasons;
- conflicts or recusals where applicable;
- date and version.

A vote total is not a substitute for a legally required reasoned decision.

## 10. Execution contract

An accepted initiative transitions to an execution record.

This is the point at which public discussion becomes an accountable commitment with owners, milestones, resources, changes, and evidence.

See [Execution & Accountability](execution-accountability.md).

## 11. Outcome verification

Completion of procurement or construction is not automatically completion of the public goal.

The process should compare the result with the original problem statement.

Example:

- Output: crossing installed.
- Outcome: crossing speed reduced; pedestrian safety indicators improved.
- Verification: measurement window and evidence.

## 12. Close, appeal, or reopen

An initiative may close when closure criteria are met.

It may be appealed or reopened if:

- required procedure was not followed;
- material evidence changed;
- implementation materially diverged;
- the stated outcome was not achieved;
- a new linked problem emerged.

## Event model

Every state change should be append-only at the audit level:

```text
initiative.created
initiative.structured
initiative.linked
initiative.scope_changed
evidence.added
alternative.added
procedure.selected
participation.opened
participation.closed
decision.recorded
execution.started
milestone.updated
commitment.changed
outcome.measured
initiative.closed
initiative.reopened
```

The current state is a projection of the event history, not a replacement for it.
