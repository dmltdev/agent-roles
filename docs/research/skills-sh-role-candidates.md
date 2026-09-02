# skills.sh role candidates for agent-roles

## Candidate inventory searched/read

| Category | Candidate | Source | Reusable patterns |
|---|---|---|---|
| Architecture | architecture-scaffold | https://www.skills.sh/petekp/claude-code-setup/architecture-scaffold | Turn architecture spec into typed skeleton; separate structure from logic; compiler as guardrail before implementation. |
| Architecture | architecture-review | https://www.skills.sh/marcus/marcus-skills/architecture-review | Make decisions explicit; prefer guardrails/golden paths over gates; document decisions as ADRs. |
| Architecture | system-architecture | https://skills.sh/hieutrtr/ai1-skills/system-architecture | Use for structural decisions, schema/refactor tradeoffs, ADRs; output architecture decisions and next-step handoff. |
| Architecture | api-designer | https://skills.sh/jeffallan/claude-skills/api-designer | Analyze domain, model resources, specify contract, validate, mock, plan evolution/deprecation. |
| Architecture | backend-architect | https://www.skills.sh/rmyndharis/antigravity-skills/backend-architect | Capture domain/non-functional requirements; define service boundaries/contracts; identify risks, observability, rollout. |
| Architecture | implementation-planner | https://www.skills.sh/jumppad-labs/jumppad/implementation-planner | Planning stays skeptical/iterative; separate working notes from deliverables; delegate research, verify findings. |
| Product/spec | requirements-specification | https://www.skills.sh/nicepkg/ai-workflow/requirements-specification | User stories should be INVEST; requirements should manage scope ruthlessly and be testable. |
| Product/spec | deliver-prd | https://www.skills.sh/product-on-purpose/pm-skills/deliver-prd | PRD communicates what/why, scope boundaries, success criteria; use after problem alignment and before engineering. |
| Product/spec | deliver-acceptance-criteria | https://www.skills.sh/product-on-purpose/pm-skills/deliver-acceptance-criteria | ACs are observable Given/When/Then pass/fail conditions; story-scoped, QA-ready, include edge/error/non-functional expectations. |
| Product/spec | specification | https://www.skills.sh/0xranx/agentbrief/specification | Spec structure: problem statement, why now/cost of not solving, primary/secondary/guardrail metrics, user stories. |
| Product/spec | write-product-spec | https://www.skills.sh/warpdotdev/common-skills/write-product-spec | Product spec from consumer perspective; specify surface, operations, invariants, edge cases; exclude implementation details. |
| Product/spec | deliver-user-stories | https://www.skills.sh/product-on-purpose/pm-skills/deliver-user-stories | Break approved PRD/features into user-value increments without prescribing implementation. |
| Product/spec | user-stories | https://www.skills.sh/phuryn/pm-skills/user-stories | Use 3 C's and INVEST; include description, design links, assumptions, acceptance criteria. |
| Code quality | code-reviewer | https://www.skills.sh/jeffallan/claude-skills/code-reviewer | Review context first; summarize PR intent; inspect structure, details, tests; immediate critical findings. |
| Code quality | code-quality | https://www.skills.sh/xbklairith/kisune/code-quality | Trigger on review/refactor/optimization/code smells/pre-commit/after feature; systematic checklist. |
| Code quality | forge-review | https://www.skills.sh/mgiovani/cc-arsenal/forge-review | Code-centric analysis only; architecture/design/readability/maintainability/refactoring; independent of story fit. |
| Code quality | code-review diagnostic | https://skills.sh/jwynia/agent-skills/code-review | Review before merge/PR/self-review; not for writing code, architecture, or requirements. |
| Code quality | comprehensive-review-full-review | https://skills.sh/rmyndharis/antigravity-skills/comprehensive-review-full-review | Multi-dimensional review: quality, security, performance, testing, docs; consolidate prioritized remediation. |
| Code quality | technical-advisory | https://skills.sh/404kidwiz/claude-supercode-skills/technical-advisory | Senior guidance for complex engineering tradeoffs across architecture, distributed systems, security, performance. |
| Verification | verification-before-completion | https://www.skills.sh/obra/superpowers/verification-before-completion | No completion claims without fresh evidence; identify proof command, run, read output/exit code, align claim to evidence. |
| Verification | verify-this | https://www.skills.sh/cursor/plugins/verify-this | Verification proves/disproves a specific measurable claim; not a recap; require before/after repro for bug fixes. |
| Verification | verify-behavior | https://www.skills.sh/mthines/agent-skills/verify-behavior | Find cheapest isolated executed proof; classify raw result vs claim as confirms/contradicts/ambiguous/null; do not score. |
| Verification | forge-qa | https://www.skills.sh/mgiovani/cc-arsenal/forge-qa | Story-centric QA against ACs, coverage, DoD; every verdict grounded in implementation/test evidence; partial is explicit. |
| Verification | principle-prove-it-works | https://www.skills.sh/cursor/plugins/principle-prove-it-works | Check real thing, not proxy; run full chain input-to-output; suspect observation method when verification fails. |
| Verification | verifykit | https://www.skills.sh/mimukit/skills/verifykit | For frontend: drive feature like a user, capture screenshots/GIF proof for PR. |
| Security | code-review-security | https://skills.sh/hieutrtr/ai1-skills/code-review-security | Trigger on PR security, auth/authz, user input/file upload/external data, OWASP, secrets, dependencies, sensitive APIs. |
| Security | api-security-tester | https://www.skills.sh/kalshamsi/claude-security-skills/api-security-tester | Static API analysis mapped to OWASP API Top 10:2023/CWE; BOLA, auth, excessive exposure, rate limits, SSRF. |
| Security | security-test-generator | https://www.skills.sh/kalshamsi/claude-security-skills/security-test-generator | Generate executable security tests only when requested; probe SQLi, XSS, CSRF, auth bypass, traversal, SSRF, mass assignment. |
| Security | security-requirement-extraction | https://skills.sh/rmyndharis/antigravity-skills/security-requirement-extraction | Convert threat models to security requirements, user stories, test cases, acceptance criteria, compliance mappings. |
| Security | security-pr-checklist-skill | https://skills.sh/patricio0312rev/skills/security-pr-checklist-skill | PR checklist: auth/authz, no hardcoded credentials, secure sessions, rate limiting, input validation. |
| Delivery | pre-merge-checklist | https://skills.sh/hieutrtr/ai1-skills/pre-merge-checklist | Final PR readiness: automated checks, blocking issues; not in-depth security, implementation, architecture, or E2E creation. |
| Delivery | git-pr-workflows-git-workflow | https://skills.sh/rmyndharis/antigravity-skills/git-pr-workflows-git-workflow | Orchestrate code review, test automation, deployment readiness, conventional commits, structured PR creation. |
| Delivery | pre-release | https://www.skills.sh/marcfargas/skills/pre-release | Before publish/version/release PR; run checks, generate changesets/changelog from git history, release readiness report. |
| Delivery | release | https://www.skills.sh/boshu2/agentops/release | Reversible local release prep; deterministic pre-flight; operator-owned push/publish; bind completion to tag SHA and exact-SHA CI. |
| Delivery | rollout | https://www.skills.sh/firetiger-oss/skills/rollout | Ship lifecycle: read change, monitoring plan, consentful merge, deploy, monitor, handoff or pivot on regression. |
| Delivery | ship | https://www.skills.sh/eigent-ai/agent-skills/ship | Make launch decisions explicit: scope, owner, risk, checklist, rollout, metrics, rollback, comms, post-launch decision. |
| Delivery | release workflow | https://skills.sh/parcadei/continuous-claude-v3/release | Trigger on prepare/cut/release/deploy; structured release preparation to ship confidently. |

## Role mappings

### product-architect

Sources:
- https://www.skills.sh/nicepkg/ai-workflow/requirements-specification
- https://www.skills.sh/product-on-purpose/pm-skills/deliver-prd
- https://www.skills.sh/product-on-purpose/pm-skills/deliver-acceptance-criteria
- https://www.skills.sh/0xranx/agentbrief/specification
- https://www.skills.sh/warpdotdev/common-skills/write-product-spec
- https://www.skills.sh/product-on-purpose/pm-skills/deliver-user-stories

Instruction patterns:
- Triggers: fuzzy product intent, PRD/spec/story/acceptance-criteria requests, scope alignment before engineering, multiple stakeholders needing shared deliverable.
- Boundaries: own what/why/scope/outcomes; do not prescribe internal types, algorithms, state layout, data flow, or module boundaries; if problem is contested, frame problem before PRD.
- Procedure: state user problem and why now; define primary, secondary, and guardrail metrics; describe consumer-visible surface/operations/invariants/edge cases; break work into INVEST stories; convert slices into observable Given/When/Then ACs.
- Output contract: concise spec/brief with problem, personas, user stories, acceptance criteria, success/guardrail metrics, non-goals, assumptions/open questions.
- Verification gates: every AC must be pass/fail observable; every story must be valuable/testable; success metric must identify intended behavior change.
- Red flags: implementation detail in product spec; ambiguous done-ness; story too broad/dependent; metrics absent; acceptance criteria describing tasks instead of behavior.

### systems-architect

Sources:
- https://www.skills.sh/petekp/claude-code-setup/architecture-scaffold
- https://www.skills.sh/marcus/marcus-skills/architecture-review
- https://skills.sh/hieutrtr/ai1-skills/system-architecture
- https://skills.sh/jeffallan/claude-skills/api-designer
- https://www.skills.sh/rmyndharis/antigravity-skills/backend-architect
- https://www.skills.sh/jumppad-labs/jumppad/implementation-planner

Instruction patterns:
- Triggers: new module/service/API/subsystem, structural decisions, schema/refactor design, service boundaries, integration patterns, ADR review.
- Boundaries: own architecture direction and contracts; avoid code-level bugfixes, small scripts, UX-only work; keep implementation planning separate from product specification.
- Procedure: capture domain context and non-functional requirements; compare feasible approaches; define service boundaries and API/data contracts; model resources before endpoint specs; plan versioning/deprecation; document significant decisions and tradeoffs.
- Output contract: architecture decision packet with chosen approach, alternatives rejected, contracts/interfaces, risks, observability needs, rollout/migration notes, ADR-worthy decisions.
- Verification gates: architecture should be enforceable where possible through typed skeleton/contracts/compilers; API contract should be lintable/mockable; decisions should be defensible and traceable to constraints.
- Red flags: local implementation choices contradict global design; unjustified abstractions; missing NFRs; no rollout/observability plan; undocumented architectural decisions.

### principal-engineer

Sources:
- https://www.skills.sh/jeffallan/claude-skills/code-reviewer
- https://www.skills.sh/xbklairith/kisune/code-quality
- https://www.skills.sh/mgiovani/cc-arsenal/forge-review
- https://skills.sh/jwynia/agent-skills/code-review
- https://skills.sh/rmyndharis/antigravity-skills/comprehensive-review-full-review
- https://skills.sh/404kidwiz/claude-supercode-skills/technical-advisory
- https://www.skills.sh/jumppad-labs/jumppad/implementation-planner

Instruction patterns:
- Triggers: implementation strategy, post-feature quality pass, PR/self-review, refactor/optimization/code smell, complex engineering tradeoff.
- Boundaries: own implementation/code quality and technical tradeoffs; do not replace product intent, architecture ownership, or security-specific audit when those are primary.
- Procedure: first summarize change intent; compare against existing patterns; inspect structure then details; check security/performance footguns; evaluate tests for behavior/edge coverage; prioritize remediation.
- Output contract: categorized findings with severity, evidence, why it matters, recommended fix; for implementation guidance include tradeoffs and chosen boring path.
- Verification gates: tests must assert behavior not implementation; critical findings surfaced immediately; recommendations grounded in code or explicit constraints.
- Red flags: cannot state PR intent; new abstraction without clear payoff; untested edge cases; N+1/injection/secrets; review comments not actionable; refactor changes behavior silently.

### verification-lead

Sources:
- https://www.skills.sh/obra/superpowers/verification-before-completion
- https://www.skills.sh/cursor/plugins/verify-this
- https://www.skills.sh/mthines/agent-skills/verify-behavior
- https://www.skills.sh/mgiovani/cc-arsenal/forge-qa
- https://www.skills.sh/cursor/plugins/principle-prove-it-works
- https://www.skills.sh/mimukit/skills/verifykit
- https://www.skills.sh/kalshamsi/claude-security-skills/security-test-generator

Instruction patterns:
- Triggers: completion/fix/passing claims, user asks prove/verify/evidence, bug fix before/after, story QA against ACs, UI proof needed.
- Boundaries: prove/disprove specific measurable claims; do not recap, score confidence, or grade intent beyond caller-owned criteria; require measurable claim if vague.
- Procedure: identify claim and cheapest direct proof; run isolated command or real user path; read full output/exit code; compare evidence to exact claim; classify confirms/contradicts/ambiguous/null; for story QA map ACs to files/tests and PASS/PARTIAL/FAIL.
- Output contract: receipt with claim, method, command/scenario, raw result, verdict, evidence refs, limits/ambiguities.
- Verification gates: no success claim without fresh evidence; check real thing not proxy; bug fixes require repro no longer triggers; UI requires user-like flow and visual evidence when applicable.
- Red flags: trusting agent self-report, linter as build proof, cached screenshots, assumed coverage, no file/test refs, broad “works” claim, PASS where only partial evidence exists.

### security-architect

Sources:
- https://skills.sh/hieutrtr/ai1-skills/code-review-security
- https://www.skills.sh/kalshamsi/claude-security-skills/api-security-tester
- https://www.skills.sh/kalshamsi/claude-security-skills/security-test-generator
- https://skills.sh/rmyndharis/antigravity-skills/security-requirement-extraction
- https://skills.sh/patricio0312rev/skills/security-pr-checklist-skill
- https://skills.sh/rmyndharis/antigravity-skills/backend-architect

Instruction patterns:
- Triggers: auth/authz changes, API endpoints/resolvers/middleware, user input/upload/external data, sensitive data exposure, rate limiting, OWASP/CWE/security tests/threat model/compliance.
- Boundaries: distinguish security audit, requirements extraction, and executable security-test generation; do not generate exploit tests unless asked for runnable security tests; escalate beyond generic PR checklist for deep API risks.
- Procedure: map attack surface; review authn/authz, object-level access, input validation/output encoding, secrets, session management, rate limiting, dependency exposure, SSRF/mass assignment/data exposure; convert threats into requirements/ACs/tests.
- Output contract: findings with severity, file:line/evidence, CWE/OWASP mapping when applicable, exploitability, remediation, regression-test idea.
- Verification gates: each finding should cite exact route/resolver/middleware or config; security requirements must be testable; executable tests should actively probe vulnerabilities.
- Red flags: hardcoded credentials; missing authorization on endpoints; insecure sessions; absent auth rate limits; overbroad data returned; mass assignment; SSRF/path traversal; security keyword used without actual security scope.

### delivery-lead

Sources:
- https://skills.sh/hieutrtr/ai1-skills/pre-merge-checklist
- https://skills.sh/rmyndharis/antigravity-skills/git-pr-workflows-git-workflow
- https://www.skills.sh/marcfargas/skills/pre-release
- https://www.skills.sh/boshu2/agentops/release
- https://www.skills.sh/firetiger-oss/skills/rollout
- https://www.skills.sh/eigent-ai/agent-skills/ship
- https://skills.sh/parcadei/continuous-claude-v3/release

Instruction patterns:
- Triggers: PR ready to merge, release/version/publish/deploy/ship/cut release, post-review final pass, rollout monitoring.
- Boundaries: own readiness/orchestration/evidence handoff; do not perform in-depth security audit, architecture decisions, implementation, or publish/push without explicit operator-controlled boundary.
- Procedure: confirm release scope/owner/risk/users/dependencies; run readiness checklist; ensure code review/test/deployment readiness; generate changelog/changesets from actual git range; plan rollout, monitoring, comms, rollback; monitor and decide continue/pause/expand/rollback.
- Output contract: readiness report with pass/fail/blockers, release notes/changelog source range, rollout plan, success/guardrail metrics, rollback/mitigation, exact evidence refs.
- Verification gates: deterministic pre-flight before tag/release; completion bound to exact tag SHA/CI, not green branch; merge/deploy/publish actions require consent; post-launch compare live metrics to expected ranges.
- Red flags: invented release notes; unverified tag; green branch treated as release proof; skip-checks without degraded-state note; deploy treated as release; no rollback owner/path.
