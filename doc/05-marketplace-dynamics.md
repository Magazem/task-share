# Marketplace Dynamics

## Two-sided marketplace

There are two primary sides:

### Builders

Need work completed.

### Contributors

Have time and skills.

The platform has a classic cold-start problem: contributors do not join
without tasks, and builders do not post without contributors.

## Recommended launch strategy

Do not launch as an unrestricted marketplace.

Start with:

> one contributor community + one project category + one task format.

Example:

**Open-source TypeScript/React projects.**

This concentrates liquidity.

## Matching

Match on:

- language;
- framework;
- task type;
- estimated duration;
- difficulty;
- reputation;
- previous project familiarity;
- availability;
- contributor preferences.

## Task quality

Bad tasks create marketplace death.

Every task should answer:

- What exactly changes?
- Which files are in scope?
- What must not change?
- How will success be tested?
- What evidence must be submitted?
- What is the expected time?
- What happens if requirements are ambiguous?

## Task lifecycle

``` text
Draft
  ↓
Published
  ↓
Claimed
  ↓
In progress
  ↓
Submitted
  ↓
Review
  ├── Accepted → Paid
  ├── Revision
  └── Disputed
```

## Liquidity metrics

Track:

- time to first claim;
- percentage of tasks claimed;
- percentage completed;
- percentage accepted;
- median number of revisions;
- contributor return rate;
- builder return rate;
- credits spent per active user.

## Marketplace failure modes

### Too many tasks, too few contributors

Builders lose confidence.

Response: - narrow categories; - recruit contributors; - increase
rewards selectively.

### Too many contributors, too few tasks

Contributors leave.

Response: - recruit builders; - create partner task pools; - allow
contributors to request tasks.

### Low-quality supply

Builders stop posting.

Response: - reputation; - qualification; - better task packaging; -
automated validation.

### Low-quality demand

Contributors stop caring.

Response: - minimum task quality; - meaningful rewards; - better
discovery; - useful credit sinks.
