# skills.sh role candidates for agent-roles

This note records the source audit behind the `agent-roles` plugin. The role agents are not copies of the source skills. They synthesize reusable execution principles into six role-specific agents and intentionally drop upstream tool names, command assumptions, output templates, and repository-specific paths.

## Audit standard

- Use skills.sh as discovery.
- Follow each shortlisted skills.sh candidate to the owning GitHub repository.
- Inspect raw `SKILL.md` files, referenced local instructions only when needed, and repository license files or the GitHub license API.
- Treat uninspected candidates as discovery leads only; do not base shipped role instructions on search summaries.
- Attribute sources here. No source text is copied into the role agents.

## Raw-source source matrix

| Role | Source skill | skills.sh discovery | Raw instruction inspected | License evidence | Adopted principles | Rejected upstream-specific assumptions |
|---|---|---|---|---|---|---|
| `product-architect` | `write-spec` | https://www.skills.sh/anthropics/product-management/write-spec | https://raw.githubusercontent.com/anthropics/knowledge-work-plugins/main/product-management/skills/write-spec/SKILL.md | Apache-2.0; https://raw.githubusercontent.com/anthropics/knowledge-work-plugins/main/product-management/LICENSE | Start from user problem, target users, constraints, prior art, measurable outcomes, goals/non-goals, user stories, P0/P1/P2 requirements, independently testable acceptance criteria, and explicit scope-creep prevention. | Do not import connector placeholders, project-tracker/knowledge-base/design tool assumptions, or PRD section bulk as mandatory agent output. |
| `product-architect` | `write-product-spec` | https://www.skills.sh/warpdotdev/common-skills/write-product-spec | https://raw.githubusercontent.com/warpdotdev/common-skills/main/.agents/skills/write-product-spec/SKILL.md | MIT; https://raw.githubusercontent.com/warpdotdev/common-skills/main/LICENSE | Specify behavior from the consumer perspective; enumerate surface, operations, states, transitions, invariants, edge/error/loading/cancellation cases; keep implementation details out of product intent. | Do not require Warp-specific `PRODUCT.md`, `TECH.md`, Figma questioning, directory conventions, or validation-section rules. |
| `product-architect` | `acceptance-criteria-designer` | https://www.skills.sh/jovd83/acceptance-criteria-designer | https://raw.githubusercontent.com/jovd83/acceptance-criteria-designer/main/SKILL.md | MIT; https://raw.githubusercontent.com/jovd83/acceptance-criteria-designer/main/LICENSE | Criteria are atomic, observable, source-grounded, risk-aware, and can be emitted as Gherkin, checklist, TDD-ready, or sentence formats depending on audience. Gaps and assumptions must be explicit. | Do not copy the JSON response contract or treat every request as acceptance-criteria authoring. |
| `systems-architect` | `architecture-review` | https://www.skills.sh/marcus/marcus-skills/architecture-review | https://raw.githubusercontent.com/marcus/marcus-skills/main/skills/architecture-review/SKILL.md | No repository license found through GitHub license API or raw `LICENSE` lookup during audit. | Make decisions explicit; align strategy before solutioning; use an architecture decision cascade; prefer guardrails/golden paths over bureaucratic gates; record ADR-worthy consequences. | Do not copy ADR templates or assume greenfield SaaS/project phases. |
| `principal-engineer` | `code-review-and-quality` | https://www.skills.sh/addyosmani/agent-skills/code-review-and-quality | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/code-review-and-quality/SKILL.md | MIT; https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | Review across correctness, readability/simplicity, architecture, security, and performance; read tests first; classify severity; avoid both rubber-stamping and perfectionism. | Do not import full review checklists or dependency/license scanning as mandatory for every implementation assignment. |
| `principal-engineer` | `code-simplification` | https://www.skills.sh/addyosmani/agent-skills/code-simplification | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/code-simplification/SKILL.md | MIT; https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | Preserve behavior exactly, follow project conventions, prefer clarity over cleverness, apply Chesterton's fence, simplify incrementally, and verify after the change. | Do not make simplification a license to rewrite unrelated code or run broad codemods by default. |
| `principal-engineer` | `refactor-safely` | https://www.skills.sh/mshindi-labs/agent-skills/refactor-safely | https://raw.githubusercontent.com/mshindi-labs/agent-skills/main/skills/refactor-safely/SKILL.md | No repository license found through GitHub license API or raw `LICENSE` lookup during audit. | Define the refactor boundary, inspect current behavior and usage, establish a behavior baseline, choose the smallest safe strategy, protect public behavior, and report behavior-preservation evidence. | Do not inherit its exact step headings or any assumption that refactoring is always the requested action. |
| `verification-lead` | `test-driven-development` | https://www.skills.sh/addyosmani/agent-skills/test-driven-development | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/test-driven-development/SKILL.md | MIT; https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | Discover test tooling first, drive RED/GREEN/REFACTOR when durable behavior is being added, reproduce bugs before fixing, test behavior and state rather than implementation interactions, prefer DAMP clarity over DRY test cleverness. | Do not require TDD for every proof task; one-time smoke evidence remains valid for runtime verification. |
| `verification-lead` | `verification-before-completion` | https://www.skills.sh/obra/superpowers/verification-before-completion | https://raw.githubusercontent.com/obra/superpowers/main/skills/verification-before-completion/SKILL.md | MIT; https://raw.githubusercontent.com/obra/superpowers/main/LICENSE | No completion/fixed/passing claim without fresh evidence; identify proof, run it, read full output/exit code, and align the claim exactly to observed evidence. | Do not import Superpowers-specific invocation rules into this standalone role plugin. |
| `security-architect` | `security-threat-model` | https://www.skills.sh/openai/skills/security-threat-model | https://raw.githubusercontent.com/openai/skills/main/skills/.curated/security-threat-model/SKILL.md | Apache-2.0; https://raw.githubusercontent.com/openai/skills/main/skills/.curated/security-threat-model/LICENSE.txt | Scope the system model, separate runtime from CI/dev/tests, map trust boundaries/assets/entry points, calibrate realistic attacker capabilities, enumerate abuse paths, prioritize by likelihood and impact, and make assumptions explicit. | Do not require its repository-summary prompt template, reference-file workflow, or final threat-model file naming convention. |
| `security-architect` | `api-security-review` | https://www.skills.sh/OWASP/secure-agent-playbook/api-security-review | https://raw.githubusercontent.com/OWASP/secure-agent-playbook/main/plugins/code-security-skills/skills/api-security-review/SKILL.md | CC-BY-4.0 in skill frontmatter and repository license; https://raw.githubusercontent.com/OWASP/secure-agent-playbook/main/LICENSE.md | Inventory API surface and auth mechanisms; assess OWASP API Top 10 risks, including BOLA/IDOR, broken auth, mass assignment/over-exposure, rate limits/DoS, BFLA, SSRF, misconfiguration, inventory/versioning, and unsafe upstream consumption. | Do not promise scanner execution, proof-of-concept payloads, or full OWASP report depth unless the assignment asks for that level of audit. |
| `delivery-lead` | `ship` | https://www.skills.sh/helderberto/agent-skills/ship | https://raw.githubusercontent.com/helderberto/agent-skills/main/skills/ship/SKILL.md | MIT; https://raw.githubusercontent.com/helderberto/agent-skills/main/LICENSE | Use a pre-launch gate before commit/push, inspect status/diff, preserve explicit git boundaries, avoid force push, and stop on validation or sensitive-data failures. | Do not import `validate-code`, `safe-repo`, heredoc commit style, automatic rebase, or direct push defaults. |
| `delivery-lead` | `release` | https://www.skills.sh/skrrt-sh/skills/release | https://raw.githubusercontent.com/skrrt-sh/skills/main/skills/ship/release/SKILL.md | MIT; https://raw.githubusercontent.com/skrrt-sh/skills/main/LICENSE | Classify release requests before mutation; derive release notes from tags/commits/diffs; validate branch/tag policy; treat tags as immutable; never invent tests, changes, contributors, or links. | Requested direct paths were absent; do not import `.agents/ship.md`, Claude plugin release references, forge scripts, gitmoji conventions, or direct publish/push authority. |
| `delivery-lead` | `pre-release` | https://www.skills.sh/marcfargas/skills/pre-release | https://raw.githubusercontent.com/marcfargas/skills/main/pre-release/SKILL.md | MIT; https://raw.githubusercontent.com/marcfargas/skills/main/LICENSE | Release readiness needs explicit check results, license/package metadata review, secret/template scans, README/readiness review, user-facing release notes from real history, and blocker/warning classification. | Do not require npm, Changesets, Trusted Publishers, or package-release mechanics for non-package delivery work. |

## Screened candidates not used as shipped instruction sources

These candidates were discovered from skills.sh/search results and were useful for coverage mapping, but their raw source was not inspected deeply enough for shipped instruction synthesis in this pass.

| Category | Candidate | Source | Status |
|---|---|---|---|
| Architecture | `architecture-scaffold` | https://www.skills.sh/petekp/claude-code-setup/architecture-scaffold | Discovery lead only. |
| Architecture | `system-architecture` | https://skills.sh/hieutrtr/ai1-skills/system-architecture | Discovery lead only. |
| Architecture | `api-designer` | https://skills.sh/jeffallan/claude-skills/api-designer | Discovery lead only. |
| Architecture | `backend-architect` | https://www.skills.sh/rmyndharis/antigravity-skills/backend-architect | Discovery lead only. |
| Architecture | `implementation-planner` | https://www.skills.sh/jumppad-labs/jumppad/implementation-planner | Discovery lead only. |
| Product/spec | `requirements-specification` | https://www.skills.sh/nicepkg/ai-workflow/requirements-specification | Discovery lead only. |
| Product/spec | `deliver-prd` | https://www.skills.sh/product-on-purpose/pm-skills/deliver-prd | Discovery lead only. |
| Product/spec | `deliver-acceptance-criteria` | https://www.skills.sh/product-on-purpose/pm-skills/deliver-acceptance-criteria | Discovery lead only. |
| Product/spec | `specification` | https://www.skills.sh/0xranx/agentbrief/specification | Discovery lead only. |
| Product/spec | `deliver-user-stories` | https://www.skills.sh/product-on-purpose/pm-skills/deliver-user-stories | Discovery lead only. |
| Product/spec | `user-stories` | https://www.skills.sh/phuryn/pm-skills/user-stories | Discovery lead only. |
| Code quality | `code-reviewer` | https://www.skills.sh/jeffallan/claude-skills/code-reviewer | Discovery lead only. |
| Code quality | `code-quality` | https://www.skills.sh/xbklairith/kisune/code-quality | Discovery lead only. |
| Code quality | `forge-review` | https://www.skills.sh/mgiovani/cc-arsenal/forge-review | Discovery lead only. |
| Code quality | `code-review` | https://skills.sh/jwynia/agent-skills/code-review | Discovery lead only. |
| Code quality | `comprehensive-review-full-review` | https://skills.sh/rmyndharis/antigravity-skills/comprehensive-review-full-review | Discovery lead only. |
| Code quality | `technical-advisory` | https://skills.sh/404kidwiz/claude-supercode-skills/technical-advisory | Discovery lead only. |
| Verification | `verify-this` | https://www.skills.sh/cursor/plugins/verify-this | Discovery lead only. |
| Verification | `verify-behavior` | https://www.skills.sh/mthines/agent-skills/verify-behavior | Discovery lead only. |
| Verification | `forge-qa` | https://www.skills.sh/mgiovani/cc-arsenal/forge-qa | Discovery lead only. |
| Verification | `principle-prove-it-works` | https://www.skills.sh/cursor/plugins/principle-prove-it-works | Discovery lead only. |
| Verification | `verifykit` | https://www.skills.sh/mimukit/skills/verifykit | Discovery lead only. |
| Security | `code-review-security` | https://skills.sh/hieutrtr/ai1-skills/code-review-security | Discovery lead only. |
| Security | `api-security-tester` | https://www.skills.sh/kalshamsi/claude-security-skills/api-security-tester | Discovery lead only. |
| Security | `security-test-generator` | https://www.skills.sh/kalshamsi/claude-security-skills/security-test-generator | Discovery lead only. |
| Security | `security-requirement-extraction` | https://skills.sh/rmyndharis/antigravity-skills/security-requirement-extraction | Discovery lead only. |
| Security | `security-pr-checklist-skill` | https://skills.sh/patricio0312rev/skills/security-pr-checklist-skill | Discovery lead only. |
| Delivery | `pre-merge-checklist` | https://skills.sh/hieutrtr/ai1-skills/pre-merge-checklist | Discovery lead only. |
| Delivery | `git-pr-workflows-git-workflow` | https://skills.sh/rmyndharis/antigravity-skills/git-pr-workflows-git-workflow | Discovery lead only. |
| Delivery | `release` | https://www.skills.sh/skrrt-sh/skills/release | Requested `skills/release/SKILL.md` and `release/SKILL.md` paths were absent; audited alternate raw source `skills/ship/release/SKILL.md` in the source matrix. |
| Delivery | `rollout` | https://www.skills.sh/firetiger-oss/skills/rollout | Discovery lead only. |
| Delivery | `release workflow` | https://skills.sh/parcadei/continuous-claude-v3/release | Discovery lead only. |
| Delivery | `ship` | https://www.skills.sh/eigent-ai/agent-skills/ship | Repository/license resolved, but no matching raw `ship/SKILL.md` or `skills/ship/SKILL.md` found during audit. |

## Per-role synthesis

### `product-architect`

Source-grounded principles:

- Own behavior, not implementation. Consumer-visible surface, operations, states, and invariants are the artifact.
- Measure success with outcomes, not shipped outputs.
- Acceptance criteria must be independently testable and cover happy path, error cases, edge cases, and negative behavior.
- Non-goals are mandatory when scope can expand.
- Open questions should name the owner and whether they block downstream work.

### `systems-architect`

Source-grounded principles:

- Own boundaries, interfaces, dependency direction, migration/cutover, and architectural consequences.
- Compare material options and document rejected alternatives.
- Prefer guardrails and typed/public contracts over process-heavy gates.
- Choose the smallest end-to-end slice that validates the riskiest boundary.
- Escalate unclear behavior to product ownership instead of inventing product intent.

### `principal-engineer`

Source-grounded principles:

- Fix causes, preserve behavior unless explicitly asked, and migrate every caller in a clean cutover.
- Reuse existing patterns; avoid needless abstractions and compatibility shims.
- Review implementation across correctness, simplicity, architecture, security, and performance, with severity tied to production impact.
- Refactor in small behavior-preserving increments with baseline evidence.
- Verify before reporting success.

### `verification-lead`

Source-grounded principles:

- Proof precedes completion claims.
- Select proof by observable contract: unit/integration/contract/e2e/browser/CLI/API/job smoke as appropriate.
- Bug fixes require a reproduction path and confirmation that the original failure no longer triggers.
- Durable tests are for new or changed observable contracts; smoke evidence is enough for one-off runtime proof when no durable test is warranted.
- Report raw result, verdict, and remaining ambiguity.

### `security-architect`

Source-grounded principles:

- Model assets, trust boundaries, entry points, attackers, assumptions, and controls before findings.
- Prioritize realistic abuse paths over checklist completion.
- API review must cover authn/authz, object/field-level access, resource consumption, business-flow abuse, SSRF, misconfiguration, version inventory, and unsafe upstream consumption where in scope.
- Findings need evidence, exploitability, impact, remediation, and proof expectations.
- Security tests or exploit payloads are generated only when explicitly requested.

### `delivery-lead`

Source-grounded principles:
- Delivery is evidence packaging and risk decisioning, not a rubber stamp.
- Commit, push, PR, merge, deploy, publish, and release are separate explicitly authorized actions.
- Pre-launch/release gates must read actual diff/status/check output and stop on blocking failures.
- Release notes and readiness reports come from real tags, commits, diffs, and observed checks, not invented summaries.
- Tags and release artifacts are immutable unless a human explicitly authorizes a corrective release operation.
- Risky production-facing work needs rollback/recovery ownership and post-launch monitoring expectations.
