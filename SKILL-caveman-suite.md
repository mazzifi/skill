---
name: caveman-suite
description: Router/index over the full "Caveman" plugin suite (caveman-main.zip) — a family of 20+ skills for token-efficient, evidence-driven agent behavior (terse output mode, scoped bug-fixing, safe refactors, migrations, repo exploration, cost/usage tracking). This is the full upstream repo behind the already-installed `caveman` skill (which only covers the terse-speak mode); use this index when the user wants the rest of the suite — scoping discipline, investigation-first debugging, or usage stats — not just brevity.
license: MIT + BSL (per repo)
---

# Caveman — full suite index

`caveman-main.zip` is a plugin with ~20 skills under `skills/<name>/SKILL.md`
(also mirrored under `plugins/caveman/skills/`). The environment already has
the core **caveman** terse-output skill installed; this index covers the
rest of the suite, which is really a discipline system for *scope control
and evidence-based changes*, with brevity as one part of it.

## Communication mode
- **caveman** — ultra-compressed output mode (lite/full/ultra + wenyan
  variants); drops articles/filler/hedging while preserving technical
  accuracy, exact numbers, negations, and code. *(Already installed
  separately as the `caveman` skill.)*
- **caveman-help** — explains the suite's commands/modes on request.
- **cavecrew** — coordinates multiple caveman-style sub-agents on a task.

## Scoped engineering workflows
- **investigate-first** — diagnose ambiguous failures (unknown cause,
  intermittent behavior, perf regressions) *before* editing anything;
  produces evidence-ranked hypotheses.
- **lean-build** — build new feature work under an explicit stop condition,
  biased against overbuilding; prefers reusing existing repo code.
- **surgical-patch** — fix bugs/small behavior changes at the narrowest
  responsible layer, with regression proof and preserved surrounding
  behavior.
- **safe-refactor** — restructure code (extraction, consolidation, ownership
  moves) while proving behavior is unchanged, verification bracketing the
  edit.
- **migration** — reversible, compatibility-safe schema/data/API/protocol/
  dependency migrations with rollback and preservation proof.
- **verify-and-stop** — validate that existing work meets acceptance
  conditions without expanding scope; a "last-mile proof" / completion gate.
- **caveman-explore** — read-only repo explorer for cold-start orientation or
  broad cross-file localization; returns `path:line` citations only and
  keeps its own reads out of the main context window.

## Cost/usage management
- **caveman-stats** — reports token/cost savings from using the suite.
- **caveman-learn** — reviews a ranked "token sink" report and applies
  cost-lowering fixes (e.g. trimming a bloated CLAUDE.md, offloading
  re-pasted context) with per-edit consent.
- **caveman-optimize / caveman-compress** — targeted output/context
  compression passes distinct from the always-on `caveman` speech mode.
- **caveman-review / caveman-evidence-review** — review changes/claims
  against evidence before accepting them.
- **caveman-manage / caveman-setup / caveman-discover / caveman-commit** —
  suite configuration, onboarding/discovery of what's available, and
  commit-message handling in the caveman house style.

## How to use this index
1. If the user just wants shorter responses → the already-installed
   `caveman` skill covers that; no need to reach into this zip.
2. If the user's request is about **not overbuilding**, **fixing a bug
   without collateral changes**, **safely refactoring**, or **investigating
   before touching code** → extract the matching SKILL.md:
   ```bash
   unzip -p caveman-main.zip "caveman-main/skills/<name>/SKILL.md"
   ```
3. These skills assume a caveman-specific proxy/CLI setup (per the repo's
   `INSTALL.md`) for some features (stats tracking, cavemem context
   offload) — treat those parts as reference material rather than something
   wired up in this chat environment unless the user has actually installed
   the caveman CLI/proxy.
