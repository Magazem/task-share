# GitHub and Repository Model

## Why GitHub first

GitHub already contains:

- repositories;
- issues;
- branches;
- pull requests;
- CI;
- reviews;
- contributor identities;
- contribution history.

That makes it the natural first substrate.

## GitHub App

Prefer a GitHub App rather than asking users for broad personal access
tokens where practical.

The app should request the minimum permissions needed.

## Project onboarding

Example:

``` text
Connect GitHub
      ↓
Select repository
      ↓
Import open issues
      ↓
Choose issues eligible for exchange
      ↓
Create task capsules
```

## Issue conversion

A GitHub issue can become a marketplace task.

Example:

``` text
GitHub issue #183
       ↓
Task capsule
       ├── reward
       ├── estimated time
       ├── acceptance criteria
       ├── allowed paths
       └── contributor requirements
```

## PR-based completion

Completion should normally produce a PR.

Benefits:

- familiar workflow;
- reviewable diff;
- existing CI;
- traceable history;
- easy rollback.

## Repository modes

### Public

Recommended for MVP.

### Private

Later, with scoped access.

### Disposable

Temporary challenge/task repositories.

### Partner

Projects specifically published by organizations.

## GitHub identity and reputation

Verified GitHub history can improve trust.

Potential signals:

- account age;
- contribution history;
- merged PRs;
- issue participation;
- repository ownership;
- language expertise.

Do not reduce reputation to GitHub stars.

## GitHub limitations

The platform should not become completely dependent on one provider.

Long term, abstract the repository adapter:

``` text
RepositoryProvider
  ├── GitHub
  ├── GitLab
  └── Bitbucket
```

But do not build all three initially.
