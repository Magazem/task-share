# Trust, Reputation and Disputes

## Why trust matters

A stranger may be modifying code that matters to a project. A simple
five-star rating is insufficient.

The platform should maintain a structured contribution record.

## Contributor profile

Possible signals:

- tasks completed;
- acceptance rate;
- first-pass acceptance;
- median completion time;
- revision count;
- dispute rate;
- security incidents;
- languages/frameworks;
- verified GitHub history;
- open-source contributions.

## Builder profile

Builders also need reputation:

- task clarity;
- response time;
- acceptance fairness;
- dispute frequency;
- cancellation rate;
- average review delay.

This creates symmetry.

## Reputation should be task-specific

A contributor with:

> 200 React tasks

should not automatically be trusted with:

> Kubernetes infrastructure.

Use skill-specific reputation.

## Dispute model

### Stage 1 — direct resolution

Builder and contributor communicate through the task.

### Stage 2 — evidence

Both submit:

- task requirements;
- diff;
- tests;
- messages;
- screenshots/logs;
- acceptance criteria.

### Stage 3 — neutral review

A qualified reviewer evaluates the dispute.

Reviewer earns credits.

### Stage 4 — arbitration

For high-value tasks, multiple reviewers may be required.

## Automatic acceptance

A task can automatically release credits after a timeout if:

- required checks pass;
- contributor submitted required evidence;
- builder has not responded;
- no dispute exists.

This prevents builders from simply disappearing.

## Contributor protection

Do not allow builders to:

- continuously expand scope;
- demand unrelated work;
- reject without evidence;
- change acceptance criteria after work begins.

## Builder protection

Do not allow contributors to:

- substitute unrelated implementations;
- intentionally degrade security;
- hide changes outside task scope;
- repeatedly submit non-functional work.

## Reputation decay

Old reputation should matter less over time.

A contributor who was excellent two years ago but inactive should not be
ranked exactly like an active contributor.

## Key principle

The system should reward **predictability**, not just raw volume.
