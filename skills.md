# Installed Skills

Project-level skills in `.claude/skills/` (installed 2026-11-10 via `npx skills add`).
Invoke with `/<name>` or let Claude trigger them automatically.

## Workflow (obra/superpowers)

| Skill | Use when |
|---|---|
| using-superpowers | Start of any session. Teaches Claude to find and use skills first. |
| brainstorming | Before any new feature or design. Clarifies requirements before code. |
| writing-plans | Turn a spec into a step-by-step implementation plan. |
| executing-plans | Run a plan inline, task by task. |
| subagent-driven-development | Run a plan's independent tasks via subagents. |
| dispatching-parallel-agents | 2+ independent tasks with no shared state. |
| using-git-worktrees | Isolate feature work in its own worktree. |
| test-driven-development | Write the failing test first, then the code. |
| systematic-debugging | Any bug or failing test. Find root cause before fixing. |
| verification-before-completion | Run tests and confirm output before claiming "done". |
| requesting-code-review | Ask for a review after finishing a feature. |
| receiving-code-review | Evaluate review feedback critically before applying it. |
| finishing-a-development-branch | Decide how to merge/integrate once tests pass. |
| writing-skills | Create or edit a skill. |
| diagnosing-superpowers | Figure out why a session went badly. |

## Lean coding (dietrichgebert/ponytail)

| Skill | Use when |
|---|---|
| ponytail | Smallest change that fully solves the task. Levels: lite, full, ultra. |
| ponytail-review | Review a change: logic, safety, load, tests, bloat. |
| ponytail-audit | Whole-repo audit: bugs, security, slow paths, dead code. Report only. |
| ponytail-debt | List deferred `shortcut:` comments as a debt ledger. |
| ponytail-gain | Show ponytail's measured savings. |
| ponytail-help | Quick reference for ponytail commands. |

## Frontend design

| Skill | Source | Use when |
|---|---|---|
| impeccable | pbakaus/impeccable | Design, polish, critique, or audit any UI: layout, type, color, motion, a11y, responsive. |
| hallmark | nutlope/hallmark | Build a brand-new page or site that looks designed, not generated. |

## Backend / system design (anthropics/knowledge-work-plugins)

| Skill | Use when |
|---|---|
| system-design | "Design a system for...", API design, data modeling, service boundaries. |
| architecture | Write or evaluate an ADR. Choosing between technologies. |
| testing-strategy | "How should we test...", test plans, coverage, test architecture. |

## Testing

| Skill | Source | Use when |
|---|---|---|
| tdd | mattpocock/skills | Test-first feature work, red-green-refactor, integration tests. |
| test-driven-development | obra/superpowers | Same discipline, superpowers flavour. |
| testing-strategy | knowledge-work-plugins | Decide what to test and at which layer. |
| webapp-testing | anthropics/skills | Drive the running React app with Playwright: verify UI, screenshots, logs. |
| playwright-best-practices | currents-dev | Write/fix Playwright tests, flaky tests, POM, API mocking, CI, a11y. |
| verification-before-completion | obra/superpowers | Prove it passes before saying it passes. |

## Per-feature flow

1. brainstorming → 2. system-design / architecture (if backend shape matters) → 3. writing-plans
→ 4. tdd / test-driven-development while coding → 5. impeccable / hallmark for UI
→ 6. verification-before-completion + webapp-testing → 7. ponytail-review / requesting-code-review.

## Maintenance

```
npx skills list          # show installed
npx skills update        # update all
npx skills add <owner/repo> --skill <name> -a claude-code -y   # add one (one skill per call)
```
