---
name: ecc-skill-index
description: Router/index over "ECC" (ecc.tools) — an agent-harness bundle of 38 SKILL.md files covering engineering, content/marketing, research, ops, and meta-workflows (from ECC-main.zip). Use when a task matches one of the named skills below (API design, TDD workflow, security review, deep research, content engine, investor materials, video editing, MCP server patterns, etc.) so you know which bundled SKILL.md to open from the extracted repo at .agents/skills/<name>/SKILL.md.
---

# ECC — Everything Claude Code (skill index)

ECC bills itself as an "agent harness operating system": a large bundle of
composable skills under `.agents/skills/<name>/SKILL.md`, plus commands,
hooks, and marketplace metadata. This file is the **index** — read the real
SKILL.md for the matching entry below once you've unzipped `ECC-main.zip`
(path: `ECC-main/.agents/skills/<name>/SKILL.md`).

## Engineering
- **api-design** — REST resource naming, status codes, pagination, versioning, rate limits.
- **backend-patterns** — Node/Express/Next.js API route & data-access patterns.
- **frontend-patterns** — React/Next.js component, state, and render-performance patterns.
- **bun-runtime** — Bun vs Node tradeoffs, migration notes, Vercel support.
- **nextjs-turbopack** — Next.js 16+/Turbopack bundling and dev-speed notes.
- **coding-standards** — baseline naming/readability/immutability conventions when no framework-specific skill applies.
- **e2e-testing** — Playwright, Page Object Model, CI integration, flaky-test strategies.
- **tdd-workflow** — test-first development, 80%+ coverage across unit/integration/E2E.
- **security-review** — checklist for auth, secrets, input handling, payments.
- **mcp-server-patterns** — building MCP servers (Node/TS SDK): tools, resources, prompts, transports.
- **mle-workflow** — production ML engineering: data contracts, reproducible training, eval, deploy, rollback.
- **resolving-merge-conflicts / verification-loop / eval-harness** — merge conflict handling, pre-completion verification, formal eval-driven-development harness for agent sessions.

## Research & analysis
- **deep-research** — multi-source research via Firecrawl/Exa MCPs with cited reports.
- **market-research** — market sizing, competitor comparisons, due diligence.
- **competitive-platform-analysis / competitive-report-structure** — structured competitor analysis output.
- **documentation-lookup** — pull current library/framework docs via Context7 MCP instead of relying on training data.
- **exa-search** — neural web/code/company search via Exa MCP.
- **benchmark-methodology** — designing benchmarks for agent/system evaluation.

## Content & growth
- **content-engine** — platform-native content systems (X, LinkedIn, TikTok, YouTube, newsletters).
- **crosspost** — multi-platform distribution, never posting identical copy across platforms.
- **article-writing / brand-voice / brand-discovery** — long-form writing and voice-profile extraction from source material.
- **frontend-slides** — animation-rich HTML decks, incl. PPT→web conversion.
- **investor-materials / investor-outreach** — pitch decks, memos, cold outreach, fundraising comms.
- **video-editing** — FFmpeg/Remotion/ElevenLabs/fal.ai pipeline for cutting and augmenting footage.
- **fal-ai-media** — unified image/video/audio generation via fal.ai MCP.
- **x-api** — X/Twitter API integration (OAuth, posting, search, analytics).

## Orchestration & meta
- **agent-sort** — build an evidence-backed install plan sorting ECC's own skills into DAILY vs LIBRARY buckets for a given repo.
- **agent-introspection-debugging** — structured self-debugging workflow (capture → diagnose → recover → report) for failed agent runs.
- **dmux-workflows** — multi-agent orchestration across Claude Code/Codex/OpenCode via tmux.
- **unified-memory** — shared context/handoffs between agents via a local "Memory Vault."
- **strategic-compact** — suggests manual context compaction at natural task-phase boundaries.
- **plan-canvas** — review plans/HTML artifacts in a local browser canvas with inline annotation.
- **product-capability** — turn PRD/roadmap asks into an implementation-ready capability plan (constraints, invariants, interfaces).
- **everything-claude-code** — project-specific conventions for the ECC repo itself (JS, conventional commits).

## How to use this index
1. Match the user's task to a skill name above.
2. Extract just that skill's SKILL.md from the zip:
   ```bash
   unzip -p ECC-main.zip "ECC-main/.agents/skills/<name>/SKILL.md"
   ```
3. Follow that skill's instructions in full — this index only tells you
   *which* one to load, not the workflow itself.
4. Many ECC skills assume specific MCP servers (Firecrawl, Exa, Context7,
   fal.ai) or a "Memory Vault" convention that may not exist in this
   environment — check tool availability before assuming they're wired up.
