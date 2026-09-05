---
name: real-engineer-skills-index
description: Router/index over Matt Pocock's "Skills For Real Engineers" (skills-main.zip) — small, composable engineering and productivity skills for spec-driven development, code review, TDD, domain modeling, and interview-style planning ("grilling"). Use when the user's task matches one of the workflows below (turning a conversation into a spec/tickets, reviewing a branch against standards+spec, diagnosing a bug, resolving a merge conflict, running TDD, or a "grill me"/handoff/retro style interaction).
license: Per repo (see LICENSE); designed to be forked/edited, not used as an opaque bundle.
---

# Skills For Real Engineers — index

A collection of small, hackable skills (not a monolithic methodology) for
day-to-day engineering work, organized into `engineering/`, `productivity/`,
`misc/`, and `in-progress/` under `skills/`. Philosophy: small, composable,
model-agnostic — meant to be edited, not just installed.

## Meta / entry point
- **ask-matt** — router over this whole repo; if unsure which skill fits,
  start here.
- **setup-matt-pocock-skills** — one-time repo setup (issue tracker, triage
  labels, domain-doc layout) required before the other engineering skills
  work as intended.

## Engineering — planning & specs
- **research** — investigate a question against high-trust primary sources,
  capture findings as a Markdown file (delegable to a background agent).
- **domain-modeling** — build/sharpen a project's domain model via
  CONTEXT.md and ADRs.
- **codebase-design** — vocabulary for designing "deep modules": where a
  seam goes, what makes code testable/AI-navigable.
- **grill-with-docs** — a relentless interview to sharpen a plan/design,
  producing ADRs and a glossary as a side effect.
- **to-spec** — turn the current conversation directly into a spec and
  publish it to the issue tracker (synthesis only, no interview).
- **to-tickets** — break a plan/spec/conversation into tracer-bullet tickets
  with explicit blocking edges.
- **wayfinder** — plan work too large for one agent session as a shared map
  of decision tickets, resolved one at a time.
- **prototype** — build a throwaway prototype to answer a design question
  (sanity-check a state model or UI direction).

## Engineering — implementation & review
- **implement** — implement work from a spec or set of tickets.
- **tdd** — test-driven, red/green/refactor development.
- **diagnosing-bugs** — a diagnosis loop for hard bugs/perf regressions.
- **resolving-merge-conflicts** — resolve an in-progress git merge/rebase
  conflict.
- **code-review** — review changes since a fixed point along two axes
  (repo coding standards; match to the originating spec/issue), via
  parallel sub-agent reviews reported side by side.
- **improve-codebase-architecture** — scan for "deepening opportunities",
  present as an HTML report, then grill through the one picked.
- **triage** — move issues/external PRs through a state machine: categorize,
  verify, grill if needed, write agent-ready briefs.
- **wizard** — generate an interactive bash wizard for steps only a human
  can do (provisioning, credentials, unfamiliar dashboards) — not for steps
  the agent could do itself.

## Productivity ("grilling" family)
- **grilling / grill-me** — relentless interview to stress-test a plan,
  decision, or idea.
- **wait-what** — "that last message didn't land" — forces a re-pitch.
- **to-questionnaire** — turn an unanswerable decision into a questionnaire
  for someone else to fill in.
- **teach** — teach the user a new skill/concept within the workspace.
- **handoff** — compact the current conversation into a handoff doc for
  another agent.
- **writing-for-agents** — guidance for writing/editing skills or
  AGENTS.md/CLAUDE.md files themselves.

## In-progress / misc utilities
- **claude-handoff** — hand the conversation to a fresh background agent.
- **retro** — run a retrospective on a coding session.
- **loop-me** — grill about specs for workflows within the workspace.
- **writing-beats / writing-fragments / writing-shape** — a three-stage
  writing pipeline (explore fragments → assemble beats → shape into an
  article).
- **git-guardrails-claude-code** — hooks that block dangerous git commands
  (push, reset --hard, clean, branch -D) before execution.
- **setup-pre-commit** — wire up Husky + lint-staged + typecheck + tests.
- **migrate-to-shoehorn** — migrate tests off `as` assertions onto
  `@total-typescript/shoehorn`.
- **scaffold-exercises** — scaffold course-exercise directory structures.
- **setup-ts-deep-modules** — wire `dependency-cruiser` so each package is a
  deep module with implementation hidden behind entry points.

## How to use this index
Match the user's request to a skill above, then extract just that one:
```bash
unzip -p skills-main.zip "skills-main/skills/<category>/<name>/SKILL.md"
```
(category is `engineering/`, `productivity/`, `misc/`, or `in-progress/` per
the lists above). Several skills assume a configured issue tracker — run
`setup-matt-pocock-skills` first if the user wants the full spec→tickets→
implement→review pipeline rather than a single standalone skill.
