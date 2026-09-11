# Economics and Credit System

## Core economic question

The credit system must create real utility without simply recreating
money.

If:

> 100 credits = €10

and credits can always be bought and sold for €10, then the system is
effectively a freelance marketplace with an unnecessary currency.

The stronger model is:

> credits represent access to scarce ecosystem value.

## Three possible models

### Model A — closed credits

Credits can only be earned by completing tasks and spent on tasks.

**Pros** - simple; - avoids immediate financial regulation complexity; -
reinforces reciprocity.

**Cons** - weak supply-side motivation; - difficult to bootstrap; -
credits may accumulate without useful sinks.

### Model B — credits + ecosystem rewards

Credits can buy:

- tasks;
- code reviews;
- private beta access;
- SaaS trials;
- developer tools;
- templates;
- datasets;
- community access;
- expert sessions.

This is the preferred early model.

### Model C — convertible credits

Credits eventually become redeemable for money.

This dramatically increases regulatory, tax, fraud, KYC, payment, and
marketplace complexity. It should not be the starting assumption.

## Credit creation

Credits should enter the system through:

- completed accepted work;
- high-value moderation/review;
- verified open-source contributions;
- onboarding grants;
- promotional grants;
- ecosystem partners.

Avoid unlimited arbitrary issuance.

## Credit destruction / sinks

Credits should leave circulation when users:

- claim tasks;
- request expert review;
- access premium tools;
- redeem partner benefits;
- purchase private beta access;
- request higher-priority matching.

## Escrow

A builder deposits the reward when a task is posted or claimed.

Example:

``` text
Builder wallet:       1,000
Task reward:            50
Available:              950

Contributor accepts
        ↓
50 locked in escrow
        ↓
PR accepted
        ↓
Contributor +50
Builder -50
```

## Pricing

A task’s initial reward can be set by the builder, but the platform
should recommend prices using:

- expected duration;
- complexity;
- language/framework;
- historical completion time;
- historical rejection rate;
- contributor demand;
- required reputation;
- urgency.

## Dynamic pricing

If a task receives no qualified claims:

> increase reward.

If many contributors compete immediately:

> reduce recommended reward for future similar tasks.

The goal is to learn the market price of small software work.

## Anti-farming controls

Potential controls:

- reputation thresholds;
- task acceptance limits;
- identity/account age signals;
- contribution history;
- stake requirements;
- anomaly detection;
- reward caps for low-value tasks;
- delayed release;
- anti-collusion analysis.

## Credit inflation

If credits are issued faster than useful rewards are consumed, their
perceived value collapses.

A useful system should track:

``` text
credits issued
credits earned
credits spent
credits locked
credits expired
active balances
average time-to-spend
```

The most important early metric is:

> **earned credits that are subsequently spent.**

## Economic hypothesis

Credits become valuable if they unlock something users genuinely want
but cannot obtain as easily elsewhere.

Therefore, partner rewards may be more important than task supply alone.
