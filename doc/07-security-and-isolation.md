# Security and Isolation

## Security posture

Security should be designed around the assumption that contributors may
be:

- careless;
- compromised;
- malicious;
- inexperienced;
- using an unsafe AI agent.

Likewise, builders may accidentally expose secrets or create unsafe
tasks.

## Initial security rule

Do not give contributors production access.

Prefer:

- public repositories;
- disposable forks;
- isolated branches;
- test environments;
- synthetic data;
- no production credentials.

## Secret handling

The platform should scan for:

- API keys;
- private keys;
- tokens;
- cloud credentials;
- database URLs;
- environment secrets.

Never expose `.env` files to contributors unless explicitly designed and
safely redacted.

## Task capsule isolation

A task should define:

- allowed repository;
- allowed branch;
- allowed files/directories;
- allowed commands;
- forbidden paths;
- required tests.

## Agent execution

If the platform eventually provides remote execution, use disposable
containers or VMs with:

- network restrictions;
- filesystem isolation;
- resource limits;
- time limits;
- syscall restrictions;
- secret redaction;
- audit logs.

## Diff-based security

Before acceptance:

- inspect changed files;
- detect unexpected binary files;
- detect outbound network calls;
- scan dependencies;
- run tests;
- run static analysis;
- check for credential exfiltration patterns.

## AI-specific risks

Coding agents can:

- modify files outside intended scope;
- install dependencies;
- execute arbitrary commands;
- call network services;
- leak environment variables;
- generate insecure code.

The platform should therefore treat an AI-assisted contributor as a
potentially privileged automation process.

## Private repositories

Private repositories should be a later feature.

Potential architecture:

``` text
Private repo
    ↓
Task compiler
    ↓
minimal context capsule
    ↓
temporary contributor workspace
    ↓
patch only
    ↓
owner review
```

The contributor should not automatically receive the entire repository.

## Security maturity levels

### Level 0

Public repository, human review.

### Level 1

Public repository + automated scans.

### Level 2

Private repository + scoped task workspace.

### Level 3

Sandboxed execution.

### Level 4

Enterprise isolation and policy enforcement.

Do not attempt Level 4 before product-market validation.
