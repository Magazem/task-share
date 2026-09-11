# MCP and Agent Integration

## Purpose

MCP should connect an already-authorized local coding agent to the
marketplace.

It should not become a mechanism for remotely controlling a stranger’s
computer.

## User flow

``` text
Contributor
    ↓
Connects marketplace MCP
    ↓
Agent asks for available tasks
    ↓
Contributor selects task
    ↓
MCP provides scoped context
    ↓
Agent works locally
    ↓
Contributor reviews
    ↓
MCP submits evidence / PR
```

## Candidate tools

### `list_tasks`

Filters:

- language;
- framework;
- difficulty;
- estimated time;
- reward;
- reputation requirement.

### `get_task`

Returns:

- objective;
- acceptance criteria;
- allowed files;
- test instructions;
- reward;
- deadline.

### `claim_task`

Claims the task for the authenticated contributor.

### `get_task_context`

Returns only task-authorized context.

### `submit_result`

Submits:

- branch;
- PR;
- summary;
- tests;
- evidence.

### `request_clarification`

Sends a question to the builder.

### `get_task_status`

Returns review state and feedback.

## Security model

The MCP should be capability-limited.

A task should explicitly grant:

``` text
read:
  src/auth/*
  tests/auth/*

write:
  src/auth/reset.ts
  tests/auth/reset.test.ts

commands:
  npm test -- auth
```

The MCP should not provide arbitrary shell execution.

## Why not make the platform execute Claude/Codex itself?

Because the platform would then become responsible for:

- model provider relationships;
- API costs;
- credentials;
- provider terms;
- arbitrary code execution;
- abuse;
- secrets;
- infrastructure.

Let contributors bring their own tools.

## Provider terms

Codex usage is governed by the applicable OpenAI terms for the account
and product being used.\[^1\]

The platform should therefore avoid designing around account sharing or
any assumption that a consumer subscription can be pooled among
strangers.

## Long-term possibility

A future platform could support:

- local MCP;
- hosted agents;
- enterprise-managed agents;
- third-party agent operators.

But these should be separate execution modes.

## Design principle

**Marketplace owns the task. Contributor owns the agent.**
