# Reference UX / MVP

Status: **Foundation v0**

The first Government Assistant product should demonstrate the public-initiative lifecycle, not imitate an existing government-services portal.

## Primary screen: public problem map

The default experience is a map plus a list.

Map objects may include:

- reported problems;
- initiatives;
- consultations;
- decisions;
- projects in execution;
- completed outcomes.

Recommended visual states:

```text
Reported
Evidence gathering
Options being developed
Public participation open
Decision pending
Approved
In execution
Delayed/blocked
Outcome verification
Completed
Rejected/cancelled
```

Color alone must not be the only status signal.

## Primary action

**Report a problem / propose an improvement**

The user can begin in natural language:

> "There is no safe place to cross this road near the school."

The intake assistant asks only for information needed to structure the issue, for example:

- exact place or area;
- what happens there;
- who is affected;
- evidence/photo if available;
- whether the user is describing a problem, a preferred solution, or both.

The user sees and confirms the structured version before publication.

## Duplicate-first creation

Before creating a new public object, show likely related items:

> "A similar road-safety issue already exists 80 m away. Add your evidence to it, follow it, or create a distinct issue."

Merging remains reviewable; the user can explain why an item is different.

## Initiative page

A canonical initiative page should answer, in this order:

### 1. What is the problem?

Plain-language statement plus location/scope.

### 2. What is happening now?

Current lifecycle state, deadline, and next step.

### 3. Who is responsible?

Responsible public authority and current accountable role/body.

### 4. Who is affected?

Published affected-community definition and participation eligibility.

### 5. What evidence exists?

Source list, key facts, uncertainty, missing information.

### 6. What options exist?

Comparable alternatives, including cost/constraints where known.

### 7. How can I participate?

The action must match the current process:

- submit evidence;
- comment;
- answer consultation;
- endorse;
- join a meeting/panel;
- allocate participatory budget;
- vote, only where the applicable process provides it.

Never label a non-binding "like" as a vote.

### 8. How will the decision be made?

Show:

- mechanism;
- authority;
- threshold/rule;
- deadline;
- legal effect;
- review/appeal path.

### 9. What happened after the decision?

Execution Contract, milestones, budget/funding state, delays, changes, evidence, and outcome.

## Views

### Citizen

Optimized for:

- nearby/followed problems;
- meaningful notifications;
- simple evidence contribution;
- clear participation action;
- visible result.

### Public official

Optimized for:

- assigned initiatives;
- jurisdiction routing;
- evidence gaps;
- duplicate/merge review;
- process configuration;
- draft official responses;
- approvals;
- execution updates.

AI drafts remain visibly drafts until authorized.

### Oversight

Optimized for:

- process integrity;
- change history;
- authority mapping;
- AI event history;
- unresolved appeals/corrections;
- missing or stale execution evidence.

## Notification examples

Good:

> "A consultation about the crossing on School Street is open until 18:00 on 14 May. You receive this because you follow this area."

Good:

> "The playground project you follow missed its design milestone. The authority published a new date and reason."

Avoid:

> "People like you support this proposal — vote now!"

The latter introduces social-pressure/persuasion dynamics that should not be the default for a neutral civic system.

## Search and discovery

Users should be able to filter by:

- location;
- category;
- lifecycle state;
- participation deadline;
- responsible authority;
- followed items;
- execution delay;
- completed outcomes.

"Trending" should not be the main discovery mechanism.

## MVP routes

A first web prototype can be small:

```text
/                         map + nearby/recent initiatives
/issues/new               natural-language intake
/initiatives/:id          canonical initiative page
/initiatives/:id/evidence evidence registry view
/initiatives/:id/options  alternatives comparison
/initiatives/:id/process  participation + decision rules
/initiatives/:id/execution execution timeline
/official                  mock official workspace
/oversight                 mock audit/accountability view
```

## Demo scenarios

Use synthetic scenarios, not live political campaigns.

### Scenario 1: unsafe road crossing

Demonstrates geo intake, duplicate detection, evidence, alternatives, consultation, administrative decision, execution, outcome measurement.

### Scenario 2: neighborhood playground

Demonstrates affected-community notification, feasibility, budget alternatives, participatory budgeting or consultation depending on demo configuration, and execution tracking.

### Scenario 3: bus stop relocation

Demonstrates conflicting affected groups, accessibility evidence, multiple alternatives, and a reasoned decision.

## MVP non-goals

Do not implement in the first prototype:

- real election infrastructure;
- political campaign tooling;
- legally binding referenda;
- real public identity databases;
- automated government payments;
- real procurement;
- autonomous rights-affecting decisions;
- predictive political profiling.

The prototype should prove that the lifecycle is understandable and useful before connecting consequential systems.
