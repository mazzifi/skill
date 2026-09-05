---
name: anthropic-skills-index
description: Reference index over Anthropic's official public skills repo (skills-main__1_.zip) — document/artifact-creation and workflow skills (docx, pdf, pptx, xlsx, frontend-design, mcp-builder, skill-creator, algorithmic-art, canvas-design, brand-guidelines, internal-comms, theme-factory, doc-coauthoring, webapp-testing, web-artifacts-builder, slack-gif-creator, claude-api). Most of these already exist as public/example skills in this environment — use this file mainly to spot the few NOT already available (brand-guidelines, canvas-design, internal-comms, slack-gif-creator, claude-api, academy-guide, discernment-nudge, web-artifacts-builder, webapp-testing) and to know where to pull one from the zip if needed.
---

# Anthropic official skills repo — index & overlap map

This zip is Anthropic's own public `skills` repo. Cross-referencing its
`skills/` directory against what's already mounted in this environment at
`/mnt/skills/public/` and `/mnt/skills/examples/`:

## Already available in this environment — use the installed one, not the zip
| Skill | Installed at |
|---|---|
| docx | `/mnt/skills/public/docx/SKILL.md` |
| pdf | `/mnt/skills/public/pdf/SKILL.md` |
| pptx | `/mnt/skills/public/pptx/SKILL.md` |
| xlsx | `/mnt/skills/public/xlsx/SKILL.md` |
| frontend-design | `/mnt/skills/public/frontend-design/SKILL.md` |
| mcp-builder | `/mnt/skills/examples/mcp-builder/SKILL.md` |
| skill-creator | `/mnt/skills/examples/skill-creator/SKILL.md` |
| algorithmic-art | `/mnt/skills/examples/algorithmic-art/SKILL.md` |
| doc-coauthoring | `/mnt/skills/examples/doc-coauthoring/SKILL.md` |
| theme-factory | `/mnt/skills/user/theme-factory/SKILL.md` (user-installed) |

Prefer the environment's own copy for these — it's kept current for this
sandbox (paths, package availability) even if the zip's version differs
slightly.

## Present in the zip but NOT already installed here
- **academy-guide** — (frontmatter was a folded scalar; open the file
  directly to read its purpose) — appears to be a guided-learning/course
  skill.
- **brand-guidelines** — applies Anthropic's own brand colors/typography to
  artifacts; only relevant if the user explicitly wants Anthropic-branded
  output.
- **canvas-design** — create original visual art (.png/.pdf) using a design
  philosophy; for posters/static art pieces, never copying existing artists'
  work.
- **claude-api** — reference material for calling the Anthropic API
  directly (frontmatter used a literal block scalar; read in full before
  relying on it, since API details go stale — cross-check against
  `product-self-knowledge` skill guidance in this environment instead where
  they conflict).
- **discernment-nudge** — a short behavioral nudge skill; read directly, its
  description was a folded scalar too terse to summarize reliably here.
- **internal-comms** — templates/resources for status reports, leadership
  updates, incident reports, FAQs, and other internal communications in a
  company's house format.
- **slack-gif-creator** — constraints/tools for building Slack-optimized
  animated GIFs.
- **web-artifacts-builder** — building elaborate multi-component HTML
  artifacts (React/Tailwind/shadcn) for claude.ai, for cases beyond a
  simple single-file artifact.
- **webapp-testing** — Playwright-based toolkit for testing local web apps
  (screenshots, browser logs, functional verification).

## How to use this
1. Check the "already available" table first — if the task matches one of
   those, use the environment's own skill, not this zip.
2. Otherwise, extract the specific SKILL.md for a not-yet-installed entry:
   ```bash
   unzip -p skills-main__1_.zip "skills-main/skills/<name>/SKILL.md"
   ```
   and any bundled `references/`, `templates/`, or `scripts/` alongside it —
   several of these (canvas-design, academy-guide) ship supporting assets
   that the SKILL.md body will point to.
3. If a skill from the zip duplicates one already installed but the user
   specifically uploaded this zip to get a *different/updated* version,
   defer to what's actually in the zip and note the difference rather than
   silently using the installed copy.
