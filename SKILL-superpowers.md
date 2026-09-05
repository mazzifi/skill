---
name: superpowers-methodology
description: Router/index over "Superpowers" (superpowers-main.zip) — a complete software-development methodology built from 14 composable skills covering spec discovery (brainstorming), planning, TDD, systematic debugging, parallel/sub-agent execution, git worktrees, code review, and pre-completion verification. Use when the user wants a structured, spec-first development workflow rather than jumping straight to code, or when a task matches one of the specific stages below (writing a plan, debugging systematically, requesting/receiving code review, verifying before claiming "done").
---

# Superpowers — methodology index

Superpowers is a full dev-methodology stack, not a grab-bag: it expects to
run from the start of a coding session (`using-superpowers` establishes that
skills must be consulted before any response, including clarifying
questions) and moves a task through spec → plan → implement → verify → ship.

## The core loop, in order
1. **brainstorming** — mandatory before any creative/feature work; explores
   user intent and requirements before implementation starts.
2. **writing-plans** — once there's a spec/requirements, write the
   multi-step implementation plan before touching code.
3. **test-driven-development** — write the failing test before the
   implementation, for any feature or bugfix.
4. **executing-plans** — execute a written plan in a separate session with
   review checkpoints.
5. **subagent-driven-development** — for independent tasks *within* the
   current session, delegate to sub-agents.
6. **dispatching-parallel-agents** — for 2+ genuinely independent tasks with
   no shared state, run them in parallel.
7. **verification-before-completion** — before claiming anything is
   complete/fixed/passing: run the verification commands and confirm actual
   output — evidence before assertions, always.
8. **requesting-code-review** — when completing tasks or before merging, get
   a review against requirements.
9. **receiving-code-review** — when feedback comes back, verify it
   technically rather than performatively agreeing or blindly implementing
   unclear/questionable suggestions.
10. **finishing-a-development-branch** — once tests pass and the work is
    done, decide how to integrate (merge, PR, etc.).

## Supporting skills
- **systematic-debugging** — use for *any* bug, test failure, or unexpected
  behavior, before proposing fixes — a diagnosis discipline, not "try
  things until it works."
- **using-git-worktrees** — isolate feature work from the current workspace
  before executing a plan, via native tools or a git-worktree fallback.
- **writing-skills** — for creating/editing skills, or verifying a skill
  works before deployment (i.e. the methodology for maintaining this very
  repo).
- **using-superpowers** — the meta-skill: how to find and invoke the others,
  and the rule that skill-checking happens before any response.

## How to use this index
```bash
unzip -p superpowers-main.zip "superpowers-main/skills/<name>/SKILL.md"
```
If the user's ask maps cleanly onto one stage (e.g. "help me debug this" →
`systematic-debugging`, "review my PR" → `requesting-code-review`), pull
just that skill. If they want the *whole* workflow applied to a new feature
end-to-end, start from `brainstorming` and follow the core loop above in
order rather than skipping to implementation.

## Fit check before adopting
This methodology is opinionated (mandatory brainstorming step, strict
TDD-first, worktree isolation) and assumes an agent session structure with
sub-agents and review checkpoints. It's a good fit for larger, higher-stakes
feature work; for a one-line fix or a quick script, applying the full loop
is likely overkill — use judgment rather than mechanically running all 10
steps.
