# Agent Roles

Role-based coding agents for architecture, product, implementation, verification, security, and delivery judgment.

This plugin is intentionally agent-only. It gives OMP and compatible harnesses crisp senior engineering roles that can be invoked independently or composed by a lead agent. It does not add an orchestration workflow, command router, or role hierarchy.

Core invariant:

> Each role owns one kind of judgment and must hand off when the question belongs to another role.

## Roles

| Agent | Owns | Use when |
|---|---|---|
| `product-architect` | Product intent and acceptance behavior | A request is fuzzy, acceptance is unclear, or implementation could redefine intent. |
| `systems-architect` | System shape, boundaries, interfaces, and trade-offs | A change affects modules, APIs, data flow, or long-term architecture. |
| `principal-engineer` | Correct, boring, maintainable implementation | Code must be changed or reviewed with clean cutover discipline. |
| `verification-lead` | Proof, tests, smoke checks, and acceptance evidence | Work needs behavioral evidence before it can be called complete. |
| `security-architect` | Threat model, trust boundaries, auth, secrets, data exposure | A change touches users, data, auth, external input, deployment, or secrets. |
| `delivery-lead` | Merge, release, rollout, rollback, and reviewer readiness | Work is ready to leave the branch or needs a readiness packet. |

## Handoff chains

Complex feature:

```text
product-architect -> systems-architect -> principal-engineer -> verification-lead -> delivery-lead
```

Sensitive feature:

```text
product-architect -> systems-architect -> security-architect -> principal-engineer -> verification-lead -> delivery-lead
```

Bug fix:

```text
principal-engineer -> verification-lead -> delivery-lead
```

Architecture decision:

```text
product-architect when behavior is unclear -> systems-architect -> verification-lead for proof strategy
```

## Install

### OMP

Install from GitHub as an OMP plugin marketplace:

```bash
omp plugin marketplace add dmltdev/agent-roles
omp plugin install agent-roles@agent-roles
```

For local development:

```bash
omp plugin marketplace add /path/to/agent-roles
omp plugin install agent-roles@agent-roles --force
```

### Claude Code compatible plugin marketplace

```text
/plugin marketplace add dmltdev/agent-roles
/plugin install agent-roles@agent-roles
```

### Codex compatible plugin

```bash
codex plugin marketplace add dmltdev/agent-roles --ref main
codex plugin add agent-roles@agent-roles
```

## Dispatch examples

```text
Use product-architect to turn this feature idea into behavior and acceptance criteria. Do not design the implementation yet.
```

```text
Use systems-architect to review this proposed API boundary. Return APPROVE, REVISE, or REJECT with trade-offs and the smallest safe implementation slice.
```

```text
Use principal-engineer to implement the approved plan. Keep a clean cutover, migrate callers, and remove obsolete paths.
```

```text
Use verification-lead to define the narrowest proof that this change works against the acceptance criteria.
```

```text
Use security-architect to threat-model this endpoint and identify realistic abuse paths before implementation.
```

```text
Use delivery-lead to decide whether this branch is ready to push or merge. Include blockers, checks, and reviewer packet.
```

## Instruction sources

The role contracts were distilled from related skills.sh pages and local plugin conventions. The goal is not to clone those skills; it is to fold their strongest instructions into role-specific agents.

| Role | Primary influences |
|---|---|
| `product-architect` | `feature-spec`, `write-product-spec`, `acceptance-criteria-designer`, PRD, requirements, and user-story skills. |
| `systems-architect` | `architecture-review`, `architect-agent`, `system-architecture`, `api-designer`, `backend-architect`, `implementation-planner`. |
| `principal-engineer` | `code-review-and-quality`, `code-simplification`, `refactor-safely`, staff/strict/code-quality review skills. |
| `verification-lead` | `verify`, `test-driven-development`, `verification-before-completion`, verify-behavior, QA, and regression skills. |
| `security-architect` | `security-threat-model`, `api-security-review`, code-review-security, security-test-generator, OWASP playbook skills. |
| `delivery-lead` | `ship`, `release`, pre-merge, pre-release, rollout, git workflow, and PR readiness skills. |

Research notes live in `docs/research/skills-sh-role-candidates.md`.

## Boundary

- This plugin supplies roles, not a mandated lifecycle.
- Roles must not silently steal each other's decisions.
- Read-only roles must not edit files even if their tool list would technically allow it.
- Output must be evidence-backed when it mentions files, commands, tests, URLs, or runtime behavior.
- Missing product intent, architecture constraints, proof evidence, or release policy should be surfaced as a handoff or blocker, not guessed.
