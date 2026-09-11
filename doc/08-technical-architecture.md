# Technical Architecture

## Architectural principle

Build the marketplace first. Add agent infrastructure second.

## High-level architecture

``` text
                    Web App
                       |
                 API / Gateway
                       |
        +--------------+--------------+
        |              |              |
     Identity        Tasks          Credits
        |              |              |
     GitHub         Matching       Ledger
        |              |              |
        +--------------+--------------+
                       |
                 Task Engine
                       |
          +------------+------------+
          |                         |
       GitHub                     MCP
       Adapter                  Gateway
          |                         |
          ↓                         ↓
     Repositories            Local Agent
                                  |
                          Codex / Claude /
                          Cursor / other
```

## Core services

### Identity

- account;
- GitHub identity;
- contributor verification;
- reputation.

### Task service

- task creation;
- task state;
- task requirements;
- assignment;
- deadlines.

### Credit ledger

Use an append-only ledger rather than mutable balances alone.

Example:

``` text
transaction_id
from_account
to_account
amount
reason
task_id
timestamp
```

Balance is derived from ledger entries.

### Matching service

Ranks tasks against contributor capabilities.

### GitHub adapter

Handles:

- repository connection;
- branch/fork creation;
- PR creation;
- status checks;
- webhooks.

### Review service

Stores:

- acceptance;
- rejection;
- revisions;
- disputes;
- evidence.

### MCP gateway

Provides a narrow tool interface to explicitly connected local agents.

## Data model

Core entities:

``` text
User
Organization
Project
Repository
Task
TaskClaim
Workspace
Submission
Review
Dispute
CreditAccount
CreditTransaction
ReputationEvent
Skill
PartnerReward
```

## Event-driven architecture

Useful events:

``` text
task.created
task.claimed
workspace.created
submission.created
review.requested
submission.accepted
submission.rejected
credits.locked
credits.released
dispute.opened
reputation.updated
```

This enables later integrations without rewriting the core system.

## Suggested initial stack

The exact stack is less important than speed.

A practical MVP could use:

- TypeScript;
- Next.js or similar web framework;
- PostgreSQL;
- GitHub OAuth + GitHub App;
- background jobs;
- object storage for evidence;
- Redis or queue only when necessary.

Avoid microservices initially.

A modular monolith is likely better.

## Architecture evolution

### MVP

One application + database + GitHub integration.

### v2

Add MCP gateway and matching.

### v3

Add task compiler and isolated workspaces.

### v4

Add enterprise/private-repository security.
