# Threat Model

## Threat actors

### Malicious contributor

Goals:

- steal secrets;
- inject malware;
- manipulate tests;
- sabotage code;
- farm credits.

### Malicious builder

Goals:

- obtain free work;
- change requirements;
- refuse legitimate payment;
- harvest contributor IP.

### Colluding accounts

Two or more accounts may attempt to:

- inflate reputation;
- transfer credits;
- create fake work;
- manipulate prices.

### Compromised contributor machine

An otherwise honest contributor may have:

- malware;
- malicious browser extensions;
- compromised credentials.

### Compromised AI agent

The agent may:

- execute unintended commands;
- access secrets;
- call arbitrary endpoints;
- modify unrelated files.

## Assets

- source code;
- credentials;
- user identity;
- credits;
- reputation;
- private project information;
- marketplace integrity.

## High-risk scenarios

### Secret exfiltration

Mitigation:

- public-first model;
- secret scanning;
- isolated workspaces;
- minimal permissions.

### Credit farming

Mitigation:

- reputation;
- identity signals;
- anomaly detection;
- task diversity;
- delayed settlement.

### Scope abuse

Mitigation:

- immutable task requirements after claim;
- explicit change requests;
- dispute system.

### Malicious patch

Mitigation:

- automated tests;
- security scanning;
- diff review;
- sandboxing;
- reputation.

### Sybil attacks

Mitigation:

- GitHub verification;
- account age;
- contribution history;
- rate limits;
- progressive privileges.

## Security priority

The product should optimize for:

1.  preventing catastrophic access;
2.  making abuse expensive;
3.  detecting suspicious behavior;
4.  recovering from mistakes.

Perfect prevention is unrealistic.

## Security philosophy

> A contributor should be able to ruin a task, but not the entire
> project.
