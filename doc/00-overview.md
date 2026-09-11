# Developer Exchange — Project Overview

## Thesis

Developer Exchange is a proposed marketplace for exchanging
small-to-medium software tasks through a non-cash credit economy. A
person with a large backlog can break work into bounded tasks; another
developer with spare time and AI-assisted development capacity can
complete those tasks and earn credits.

The key distinction is that this is not primarily a cheaper Upwork. The
proposed wedge is **fragmented developer work that is individually too
small to outsource, combined with unused developer + AI capacity**.

## Core loop

1.  A builder connects a project or repository.
2.  The builder creates a bounded task with acceptance criteria and a
    credit reward.
3.  A contributor claims the task.
4.  The contributor works manually and/or with tools such as Codex,
    Claude Code, Cursor, or other agents.
5.  The contributor submits a patch or pull request.
6.  Tests and policy checks run.
7.  The builder accepts or disputes the result.
8.  Credits are released.
9.  The contributor spends credits on other tasks, developer products,
    access, expertise, or eventually other ecosystem benefits.

## Critical product principle

Do **not** make subscription sharing or remote control of a
contributor’s AI account the core product. The platform should be
agent-agnostic. Contributors use tools they are already authorized to
use. An MCP integration can expose marketplace tasks to an explicitly
connected local coding agent without giving the marketplace arbitrary
control of the contributor’s computer.

## Initial wedge

Open-source projects are the safest initial environment because code,
issues, tests, and contribution history can be public. GitHub already
supports sponsorship of contributors and projects, including code,
documentation, triage, mentorship, design, and other contributions.[^1]

Existing bounty platforms prove that developers will engage with
financially rewarded software work. Opire, for example, explicitly
positions itself around bounties for open-source issues.[^2] The
opportunity is therefore not “invent developer bounties”; it is to test
whether **non-cash, reusable credits plus AI-assisted spare capacity**
produce a different and more liquid behavior.

## What must be proven

The project should not be built around assumptions. The first validation
questions are:

- Will builders publish enough tasks?
- Will contributors claim and complete them without cash?
- Do contributors return after earning credits?
- What do contributors actually spend credits on?
- Can task quality be verified cheaply?
- Can trust be established without exposing entire repositories?
- Does AI assistance increase throughput without increasing security
  risk?
- Can the marketplace avoid becoming a generic low-quality gig platform?

## Research index

- [01-product-thesis.md](01-product-thesis.md) — product definition and
  positioning.
- [02-market-research.md](02-market-research.md) — market evidence and
  demand hypotheses.
- [03-competitive-landscape.md](03-competitive-landscape.md) — adjacent
  and direct competitors.
- [04-economics-and-credit-system.md](04-economics-and-credit-system.md)
  — credit design and economic mechanics.
- [05-marketplace-dynamics.md](05-marketplace-dynamics.md) — two-sided
  marketplace and liquidity.
- [06-trust-reputation-and-disputes.md](06-trust-reputation-and-disputes.md)
  — reputation and dispute resolution.
- [07-security-and-isolation.md](07-security-and-isolation.md) —
  repository, secret, and execution security.
- [08-technical-architecture.md](08-technical-architecture.md) —
  platform architecture.
- [09-mcp-and-agent-integration.md](09-mcp-and-agent-integration.md) —
  MCP and local agent model.
- [10-github-and-repository-model.md](10-github-and-repository-model.md)
  — GitHub-first operating model.
- [11-legal-and-tos-risks.md](11-legal-and-tos-risks.md) — legal and
  provider-term risks.
- [12-mvp-and-validation.md](12-mvp-and-validation.md) — smallest
  credible experiment.
- [13-go-to-market.md](13-go-to-market.md) — initial acquisition
  strategy.
- [14-business-model.md](14-business-model.md) — possible monetization.
- [15-threat-model.md](15-threat-model.md) — abuse and adversarial
  scenarios.
- [16-metrics-and-experiments.md](16-metrics-and-experiments.md) —
  measurable hypotheses.
- [17-roadmap.md](17-roadmap.md) — staged product evolution.
- [18-open-questions.md](18-open-questions.md) — unresolved questions.

## Sources

[^1]: GitHub Docs, “About GitHub Sponsors” and “About GitHub Sponsors
    for open source contributors.”
    https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors

[^2]: Opire, GitHub organization and README. https://github.com/Opire
