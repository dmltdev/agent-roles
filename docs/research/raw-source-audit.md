# Raw source audit for agent-roles

Scope: primary GitHub raw/API evidence for the named skills.sh candidate repositories only. GitHub API requests were intermittently rate-limited with HTTP 403 during this pass, so license conclusions below use raw `LICENSE`/`LICENSE.md`/skill `LICENSE.txt` text unless an API result is explicitly named. Sources whose requested path 404ed are marked as unresolved at that requested path even when an alternate raw path was found.

## Source matrix

| Source | Role mapping | Inspection status | skills.sh URL | Raw instruction URL | License URL | SPDX/license result | Exact inspected files |
|---|---|---|---|---|---|---|---|
| `anthropics/knowledge-work-plugins` `product-management/skills/write-spec` | `product-architect` | Inspected at requested path on `main` | Not in prior matrix; candidate implies `https://www.skills.sh/anthropics/knowledge-work-plugins/write-spec` | https://raw.githubusercontent.com/anthropics/knowledge-work-plugins/main/product-management/skills/write-spec/SKILL.md | https://raw.githubusercontent.com/anthropics/knowledge-work-plugins/main/LICENSE | Apache-2.0 text in raw license; raw file contains odd trailing non-license text after the Apache appendix | `product-management/skills/write-spec/SKILL.md`, `LICENSE` |
| `warpdotdev/common-skills` `.agents/skills/write-product-spec` | `product-architect` | Inspected at requested path on `main` | https://www.skills.sh/warpdotdev/common-skills/write-product-spec | https://raw.githubusercontent.com/warpdotdev/common-skills/main/.agents/skills/write-product-spec/SKILL.md | https://raw.githubusercontent.com/warpdotdev/common-skills/main/LICENSE | MIT text in raw license | `.agents/skills/write-product-spec/SKILL.md`, `LICENSE` |
| `jovd83/acceptance-criteria-designer` `SKILL.md` | `product-architect` | Inspected at requested path on `main` | https://www.skills.sh/jovd83/acceptance-criteria-designer | https://raw.githubusercontent.com/jovd83/acceptance-criteria-designer/main/SKILL.md | https://raw.githubusercontent.com/jovd83/acceptance-criteria-designer/main/LICENSE | MIT text in raw license; `SKILL.md` frontmatter also says `License: MIT` | `SKILL.md`, `LICENSE` |
| `marcus/marcus-skills` `skills/architecture-review` | `systems-architect` | Inspected at requested path on `main`; license unresolved | https://www.skills.sh/marcus/marcus-skills/architecture-review | https://raw.githubusercontent.com/marcus/marcus-skills/main/skills/architecture-review/SKILL.md | Tried https://raw.githubusercontent.com/marcus/marcus-skills/main/LICENSE, `/LICENSE.md`, `/LICENSE.txt`, and `master` `/LICENSE`; all 404 in this pass | Unresolved; do not infer license | `skills/architecture-review/SKILL.md`; failed license probes listed at left |
| `addyosmani/agent-skills` `skills/code-review-and-quality` | `principal-engineer` | Inspected at requested path on `main`; reader showed core sections and truncated tail | https://www.skills.sh/addyosmani/agent-skills/code-review-and-quality | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/code-review-and-quality/SKILL.md | https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | MIT text in raw license | `skills/code-review-and-quality/SKILL.md`, `LICENSE` |
| `addyosmani/agent-skills` `skills/code-simplification` | `principal-engineer` | Inspected at requested path on `main`; reader showed core sections and truncated tail | https://www.skills.sh/addyosmani/agent-skills/code-simplification | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/code-simplification/SKILL.md | https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | MIT text in raw license | `skills/code-simplification/SKILL.md`, `LICENSE` |
| `addyosmani/agent-skills` `skills/test-driven-development` | `verification-lead` | Inspected at requested path on `main`; reader showed core sections and truncated tail | https://www.skills.sh/addyosmani/agent-skills/test-driven-development | https://raw.githubusercontent.com/addyosmani/agent-skills/main/skills/test-driven-development/SKILL.md | https://raw.githubusercontent.com/addyosmani/agent-skills/main/LICENSE | MIT text in raw license | `skills/test-driven-development/SKILL.md`, `LICENSE` |
| `mshindi-labs/agent-skills` `skills/refactor-safely` | `principal-engineer` | Inspected at requested path on `main`; license unresolved | https://www.skills.sh/mshindi-labs/agent-skills/refactor-safely | https://raw.githubusercontent.com/mshindi-labs/agent-skills/main/skills/refactor-safely/SKILL.md | Tried https://raw.githubusercontent.com/mshindi-labs/agent-skills/main/LICENSE, `/LICENSE.md`, `/LICENSE.txt`, and `master` `/LICENSE`; all 404 in this pass | Unresolved; do not infer license | `skills/refactor-safely/SKILL.md`; failed license probes listed at left |
| `openai/skills` `security-threat-model` | `security-architect` | Requested/direct paths unresolved; inspected alternate curated skill path on `main` | https://www.skills.sh/openai/skills/security-threat-model | Requested `skills/security-threat-model/SKILL.md` and `security-threat-model/SKILL.md` 404. Inspected https://raw.githubusercontent.com/openai/skills/main/skills/.curated/security-threat-model/SKILL.md | https://raw.githubusercontent.com/openai/skills/main/skills/.curated/security-threat-model/LICENSE.txt | Apache-2.0 text in skill-level raw `LICENSE.txt`; repo-level `LICENSE`/`LICENSE.md` probes 404 | `skills/.curated/security-threat-model/SKILL.md`, `skills/.curated/security-threat-model/LICENSE.txt`; scout also inspected `references/prompt-template.md`, `references/security-controls-and-assets.md`, and repo `README.md` |
| `OWASP/secure-agent-playbook` `api-security-review` | `security-architect` | Requested/direct paths unresolved; inspected alternate plugin skill path on `main` | https://www.skills.sh/OWASP/secure-agent-playbook/api-security-review | Requested `skills/api-security-review/SKILL.md` and `api-security-review/SKILL.md` 404. Inspected https://raw.githubusercontent.com/OWASP/secure-agent-playbook/main/plugins/code-security-skills/skills/api-security-review/SKILL.md | https://raw.githubusercontent.com/OWASP/secure-agent-playbook/main/LICENSE.md | `LICENSE.md` states `SPDX-License-Identifier: CC-BY-4.0`; skill frontmatter says `license: CC-BY-4.0` | `plugins/code-security-skills/skills/api-security-review/SKILL.md`, `plugins/code-security-skills/plays/api-security-review.md` beginning, `LICENSE.md`; requested paths 404 |
| `helderberto/agent-skills` or `helderberto/skills` `ship` | `delivery-lead` | Inspected both raw repository aliases on `main`; both served the same skill content | https://www.skills.sh/helderberto/agent-skills/ship and https://www.skills.sh/helderberto/skills/ship | https://raw.githubusercontent.com/helderberto/agent-skills/main/skills/ship/SKILL.md and https://raw.githubusercontent.com/helderberto/skills/main/skills/ship/SKILL.md | https://raw.githubusercontent.com/helderberto/agent-skills/main/LICENSE and https://raw.githubusercontent.com/helderberto/skills/main/LICENSE | MIT text in both raw license URLs | `skills/ship/SKILL.md` from both repo names, `LICENSE` from both repo names |
| `skrrt-sh/skills` `release` | `delivery-lead` | Requested/direct paths unresolved; inspected bucketed ship release path on `main` | https://www.skills.sh/skrrt-sh/skills/release | Requested `skills/release/SKILL.md` and `release/SKILL.md` 404. Inspected https://raw.githubusercontent.com/skrrt-sh/skills/main/skills/ship/release/SKILL.md | https://raw.githubusercontent.com/skrrt-sh/skills/main/LICENSE | MIT text in raw license | `skills/ship/release/SKILL.md`, `README.md`, `LICENSE`; requested paths 404 |
| `obra/superpowers` `verification-before-completion` | `verification-lead` | Inspected at requested path on `main` | https://www.skills.sh/obra/superpowers/verification-before-completion | https://raw.githubusercontent.com/obra/superpowers/main/skills/verification-before-completion/SKILL.md | https://raw.githubusercontent.com/obra/superpowers/main/LICENSE | MIT text in raw license | `skills/verification-before-completion/SKILL.md`, `LICENSE` |

## Adopted principles and rejected upstream-specific assumptions

### Product/spec sources

- `anthropics/knowledge-work-plugins` `write-spec`
  - Adopted: treat vague ideas, user requests, and problem statements as valid spec inputs; gather user problem, target users, success metrics, constraints, and prior art; write problem, goals, non-goals, user stories, P0/P1/P2 requirements with acceptance criteria, success metrics, open questions, and timeline considerations; keep success metrics measurable; be ruthless about P0 scope.
  - Rejected/upstream-specific: connector placeholders for project tracker, knowledge base, and design tools are not portable to agent-roles; slash-command usage and follow-up artifact offers are workflow-specific; do not carry over the raw file's trailing malformed license-adjacent text.

- `warpdotdev/common-skills` `write-product-spec`
  - Adopted: product specs should describe consumer-visible behavior, operations, invariants, states, transitions, edge cases, accessibility/focus expectations, and non-regressions without prescribing internal implementation; behavior should be numbered and testable; optional sections should earn their place.
  - Rejected/upstream-specific: Warp-specific `PRODUCT.md`/`TECH.md` file naming, Linear/GitHub directory IDs, Figma-question workflow, and Warp-specific related skills are not agent-roles defaults.

- `jovd83/acceptance-criteria-designer`
  - Adopted: separate source facts from assumptions; expose unsupported gaps; choose Gherkin, TDD-style, or sentence criteria based on the input; keep criteria atomic, observable, and independent; include negative/error/boundary/state-transition coverage when justified by the source.
  - Rejected/upstream-specific: mandatory JSON contract, CQS scoring, dispatcher metadata, and bundled schema file references are useful for that skill runtime but too heavy for default agent-role instructions.

### Architecture source

- `marcus/marcus-skills` `architecture-review`
  - Adopted: make significant decisions explicit; prefer guardrails/golden paths over bureaucratic gates; use a decision cascade for style, boundaries, API/data, security, observability, testing, CI/CD, and agent workflow; evaluate quality attributes; flag anti-patterns; return clear review outcomes.
  - Rejected/upstream-specific: enterprise ARB framing, mandatory ADR for every decision, fixed `docs/adr/` numbering, and its bundled reference taxonomy should not be copied wholesale; license is unresolved, so do not reuse text beyond summarized principles without legal review.

### Principal-engineer and verification/code-quality sources

- `addyosmani/agent-skills` `code-review-and-quality`
  - Adopted: review across correctness, readability/simplicity, architecture, security, and performance; understand change intent first; inspect tests before implementation; categorize severity; lead with high-leverage findings; propose structural remedies instead of vague criticism; review dependency additions and upgrades.
  - Rejected/upstream-specific: exact line-count thresholds, multi-model review choreography, and specific related-skill names are guidance, not plugin policy; reader truncated the tail, so only inspected core sections should influence agent-roles.

- `addyosmani/agent-skills` `code-simplification`
  - Adopted: simplify only while preserving exact behavior; match project conventions; prefer clarity over cleverness; understand before touching; use concrete complexity signals; avoid over-simplification; scope to recently changed or requested code; verify after incremental changes.
  - Rejected/upstream-specific: language-specific examples and the exact “Rule of 500” should be examples, not hard global policy; reader truncated the tail, so uninspected tail content is not adopted.

- `addyosmani/agent-skills` `test-driven-development`
  - Adopted: discover the repository’s real test tooling; write failing tests before behavior changes; use a bug reproduction test before fixing; prefer behavior/state assertions, DAMP test readability, real implementations over mocks, Arrange-Act-Assert, and descriptive test names.
  - Rejected/upstream-specific: universal full-suite-before-completion wording conflicts with this plugin’s delegated-agent constraint to avoid project-wide validation mid-flight; browser-testing references are not part of principal-engineer role text; reader truncated the tail.

- `mshindi-labs/agent-skills` `refactor-safely`
  - Adopted: define the refactor boundary, unchanged behavior, and non-goals; inspect callers/tests/types/contracts; establish a behavior baseline; choose the smallest safe strategy; protect public APIs and contracts; make reviewable increments; state partial verification and remaining risks.
  - Rejected/upstream-specific: no license was found, so do not copy source wording; its generic “ask user” stops should be adapted to agent-roles’ default of deriving safe boundaries from repo context when possible.

### Security sources

- `openai/skills` curated `security-threat-model`
  - Adopted: scope the system model from repo evidence; separate runtime from CI/dev/tests; enumerate trust boundaries, assets, entry points, attacker capabilities and non-capabilities; prioritize concrete abuse paths by likelihood/impact; distinguish existing mitigations from recommendations; keep assumptions explicit and quality-check coverage.
  - Rejected/upstream-specific: requested path was absent and actual skill lives under `.curated`; do not assume skills.sh installs that internal path unchanged; OpenAI-specific prompt-template/reference-file workflow and “pause before final report” requirement are not always appropriate for agent-roles.

- `OWASP/secure-agent-playbook` plugin `api-security-review`
  - Adopted: align API review with OWASP API Security Top 10 2023; enumerate API surface, auth mechanisms, versions, gateway/middleware; assess JWT/OAuth/API key/session issues, BOLA, BOPA/mass assignment, resource exhaustion, BFLA, SSRF, misconfiguration, inventory, and unsafe consumption; produce risk matrix, exploit/business impact, remediation, and evidence.
  - Rejected/upstream-specific: requested path was absent and actual skill lives under `plugins/code-security-skills`; automated scanner commands and penetration-test payload procedures should not be auto-run by agent-roles unless requested and authorized; the long play was only inspected at the beginning, so later play sections remain unresolved.

### Delivery/verification sources

- `helderberto` `ship`
  - Adopted: delivery role should gate shipping by default, review status/diff, group atomic commits, stage named files rather than `git add -A`, never force-push, and make skipped gates explicit.
  - Rejected/upstream-specific: the skill directly commits and pushes; agent-roles should preserve operator/harness branch-protection policy and not encode `--fast` semantics as a universal bypass.

- `skrrt-sh/skills` `release`
  - Adopted: classify release requests as notes-only, prepare, or publish before mutation; derive release notes from tags/commits/diffs; validate branch/tag policy and tag absence; treat tags as immutable; never invent tests, changes, contributors, or links; never force-push/delete/retag.
  - Rejected/upstream-specific: requested path was absent and actual skill lives under `skills/ship/release`; `.agents/ship.md`, Claude plugin release references, exact forge CLI script, and gitmoji/namespace conventions are repo-specific.

- `obra/superpowers` `verification-before-completion`
  - Adopted: evidence before claims; identify the proving command/scenario, run it fresh, read full output/exit/failures, compare the evidence to the exact claim, and only then make a completion claim; distrust agent self-reports and partial checks.
  - Rejected/upstream-specific: Superpowers-specific invocation rules and broad “always before any positive statement” framing should be adapted into a verification-lead responsibility rather than global agent-roles prose.

## Short synthesis

The strongest portable patterns are role boundaries, evidence discipline, and explicit output contracts: product roles own user-visible behavior and acceptance criteria; architecture roles own decisions, boundaries, and quality attributes; principal engineering roles own behavior-preserving implementation quality; security roles own concrete attack surfaces and abuse paths; delivery roles own release readiness and operator-safe shipping; verification roles own fresh proof before claims.

Do not copy upstream workflow mechanics blindly. Several high-value sources are embedded in repo-specific plugin layouts (`openai/skills` `.curated`, OWASP `plugins/code-security-skills`, skrrt `skills/ship/release`) or carry harness-specific assumptions about slash commands, connectors, Figma, forge scripts, commit/push authority, scanners, or validation scope. For agent-roles, reuse the audited principles, keep the raw URLs as provenance, and keep unresolved licenses (`marcus/marcus-skills`, `mshindi-labs/agent-skills`) out of any text reuse path until license evidence is found.
