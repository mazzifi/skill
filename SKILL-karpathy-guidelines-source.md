---
name: karpathy-guidelines-source
description: Source/attribution reference for andrej-karpathy-skills-main.zip — a single-file CLAUDE.md distilling Andrej Karpathy's observations on common LLM coding pitfalls into four behavioral principles. This is the upstream repo behind the already-installed `karpathy-guidelines` skill; use this file when the user wants the fuller rationale, examples, or the repo's own framing rather than just the compact skill.
license: MIT
---

# Karpathy-Inspired Coding Guidelines (source repo digest)

This repo (`andrej-karpathy-skills-main.zip`) packages one idea into a
`CLAUDE.md`/`SKILL.md`: four principles addressing pitfalls Andrej Karpathy
described in coding-agent behavior — wrong silent assumptions, overcomplicated
code, non-surgical edits, and vague success criteria. It's the same content
already available in this environment as the `karpathy-guidelines` user
skill; treat this file as the fuller-context companion (problem statement +
rationale table), not a replacement.

## The problem it targets
Agents tend to: pick an interpretation silently and run with it; overbuild
abstractions/APIs beyond what's needed; touch code they don't fully
understand as a side effect of an unrelated change; and accept vague
completion criteria ("make it work") instead of verifiable ones.

## The four principles

| Principle | Addresses |
|---|---|
| **Think Before Coding** | Wrong assumptions, hidden confusion, missing tradeoffs |
| **Simplicity First** | Overcomplication, bloated abstractions |
| **Surgical Changes** | Orthogonal edits, touching code you shouldn't |
| **Goal-Driven Execution** | Verifiable success criteria over vague ones |

### 1. Think Before Coding
State assumptions explicitly rather than guessing; if multiple
interpretations exist, present them instead of silently picking one; push
back when a simpler approach exists; stop and ask when something is
genuinely unclear.

### 2. Simplicity First
Write the minimum code that solves the stated problem — no speculative
features, no single-use abstractions, no unrequested configurability, no
error handling for impossible scenarios. Test: "would a senior engineer call
this overcomplicated?"

### 3. Surgical Changes
Touch only what the task requires. Don't "improve" adjacent code, comments,
or formatting while making an unrelated change; match existing style even if
you'd choose differently; remove only the imports/variables your own change
orphaned, not pre-existing dead code (mention it instead). Every changed line
should trace back to the user's request.

### 4. Goal-Driven Execution
Turn tasks into verifiable goals before starting — e.g. "fix the bug" →
"write a failing test that reproduces it, then make it pass." For multi-step
work, state a short plan with a verification check per step. Strong success
criteria let an agent iterate independently; weak ones ("make it work")
force constant clarification.

## Relationship to the installed skill
The environment's `/mnt/skills/user/karpathy-guidelines/SKILL.md` already
encodes this same content in skill form and triggers automatically on
coding/review/refactor tasks. This file exists so the repo's own framing
(problem statement, "why this matters" table, and the note that this is a
speed/caution tradeoff to apply with judgment on trivial tasks) isn't lost —
reach for it if the user wants the reasoning behind the rules, not just the
rules.
