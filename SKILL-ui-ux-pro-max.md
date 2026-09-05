---
name: ui-ux-pro-max-source-index
description: Index over the upstream "UI UX Pro Max" repo (ui-ux-pro-max-skill-main.zip) and its 7 sub-skills (design, ui-ux-pro-max, ui-styling, design-system, brand, banner-design, slides). This environment already has a `ui-ux-pro-max` skill installed covering the same searchable design-intelligence data (79 styles, 192 palettes, 74 font pairings, 119 UX guidelines, chart types, stack-specific implementation); use this file to know which of the 7 sub-skills to reach for when the installed skill's top-level entry doesn't cover the specific need (e.g. banner design or slide-deck strategy specifically).
---

# UI UX Pro Max — sub-skill index

The zip ships as a bundle of 7 skills under `.claude/skills/<name>/SKILL.md`.
The environment already has the top-level `ui-ux-pro-max` skill installed
(`/mnt/skills/user/ui-ux-pro-max/SKILL.md`), which is this same design
intelligence system — searchable styles, product-palette reasoning, font
pairings, UX guidelines, icons, chart types, and stack-specific
implementation guidance (React, Next.js, Vue, Svelte, Angular, shadcn/ui,
SwiftUI, React Native, Flutter, HTML+Tailwind).

## The 7 sub-skills
- **ui-ux-pro-max** — the umbrella skill: design intelligence for web,
  mobile, and desktop UI — pages, components, design systems, accessibility,
  interaction, responsive layout, typography, color, charts. This is what's
  already installed in this environment.
- **design** — the broadest of the set: brand identity, design tokens, UI
  styling, logo generation (55 styles), corporate identity programs (50
  deliverables + mockups), HTML presentations with Chart.js, banner design
  (22 styles), icon design (15 styles, SVG), and social-platform photo
  generation (HTML→screenshot) across Facebook/Twitter/LinkedIn/YouTube/
  Instagram/Pinterest/TikTok/Threads/Google Ads.
- **design-system** — token architecture specifically: three-layer tokens
  (primitive → semantic → component), CSS variables, spacing/typography
  scales, component specs, and brand-compliant strategic slide creation.
- **ui-styling** — implementation-focused: shadcn/ui (Radix + Tailwind)
  components, Tailwind utility-first styling, canvas-based visuals,
  accessible components (dialogs, dropdowns, forms, tables), theming and
  dark mode.
- **brand** — brand voice, visual identity, messaging frameworks, asset
  management, and brand-compliance review for marketing assets and style
  guides.
- **banner-design** — banners specifically: social media, ads, website
  heroes, print — with named art-direction styles (minimalist, gradient,
  bold typography, photo-based, illustrated, geometric, retro,
  glassmorphism, 3D, neon, duotone, editorial, collage) across named
  platform dimensions (Facebook, Twitter/X, LinkedIn, YouTube, Instagram,
  Google Display, hero, print).
- **slides** — strategic HTML presentations with Chart.js, design tokens,
  responsive layouts, copywriting formulas, and slide-by-slide strategy.

## When to reach into this zip vs. use the installed skill
- General UI/UX design, review, or implementation work → use the installed
  `ui-ux-pro-max` skill; it already covers this ground.
- The task is narrowly about **banners**, a **slide deck's specific
  copywriting/chart strategy**, or **design-token architecture** in more
  depth than the umbrella skill surfaces → pull the matching sub-skill
  directly:
  ```bash
  unzip -p ui-ux-pro-max-skill-main.zip \
    ".claude/skills/<name>/SKILL.md" \
    # (prefix with the top-level repo dir, e.g.
    # "ui-ux-pro-max-skill-main/.claude/skills/banner-design/SKILL.md")
  ```
- Several sub-skills reference generated logos/icons via external AI image
  services (Gemini, Atlas Cloud, MuAPI) — treat those integrations as
  reference material; use this environment's own image-generation/visualize
  tooling instead where the two overlap.
