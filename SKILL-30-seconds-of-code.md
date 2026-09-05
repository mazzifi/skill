---
name: snippet-reference-30soc
description: Reference index for the "30 Seconds of Code" archive (30-seconds-of-code-master.zip) — 775+ short, curated coding articles and snippets covering JavaScript, CSS, HTML, Python, React, and Git. Use when the user wants an idiomatic short snippet, a quick "how do I do X in JS/CSS/Python/React/Git" answer, a sanity-check against an established pattern before writing one from scratch, or wants to browse/search this archive. Not a code-execution tool — it's a searchable reference corpus that must first be unzipped to disk.
license: Content is CC-BY-4.0 (attribution required); site code/branding is not reusable without permission.
---

# 30 Seconds of Code — reference archive

This skill wraps the `30-seconds-of-code-master.zip` archive: the source of
the [30secondsofcode.org](https://30secondsofcode.org) site, maintained by
Angelos Chalaris. It is a **content corpus**, not a live tool — there is no
API or script bundled here, just ~775 short Markdown articles with code
snippets, explanations, and tags.

The zip is large (~400MB, mostly images/build assets). Don't extract the
whole thing into a conversation's working directory by default — extract
only what's needed:

```bash
unzip -p 30-seconds-of-code-master.zip \
  "30-seconds-of-code-master/content/snippets/<lang>/<slug>.md"
```

or list matches first:

```bash
unzip -l 30-seconds-of-code-master.zip | grep "content/snippets/js/"
```

## Layout

```
content/
  snippets/
    js/        JavaScript utility snippets & articles
    css/       CSS techniques and recipes
    html/      HTML patterns
    python/    Python snippets
    react/     React patterns/hooks
    git/       Git command recipes
    articles/  Longer-form dev articles (tooling, VS Code, etc.)
    demo/      Interactive demo snippets
    update-logs/  Changelog-style posts
  collections/ Curated groupings of snippets by theme
  languages/   Per-language metadata
```

Each snippet file is Markdown with YAML frontmatter:

```yaml
---
title: <human title>
shortTitle: <short title>
language: javascript
tags: [array, intermediate]
excerpt: <one-line summary>
dateModified: YYYY-MM-DD
---
```

## How to use this when helping the user

1. **Identify the language/topic** the user is asking about (e.g. "debounce
   function in JS", "center a div", "flatten a git history").
2. Grep the snippet directory for that language/tag rather than guessing:
   ```bash
   unzip -p 30-seconds-of-code-master.zip \
     $(unzip -l 30-seconds-of-code-master.zip | grep -i "content/snippets/js/.*debounce" | awk '{print $4}')
   ```
3. Use the snippet as a **reference/inspiration**, not a verbatim copy-paste
   source for the final answer — rewrite/adapt the code to the user's exact
   context, variable names, and style. Treat the prose explanation as
   background, not something to reproduce at length (per copyright limits:
   short code utilities can be adapted freely for functional use, but don't
   dump large verbatim article text).
4. If the user wants to browse by topic, use `content/collections/` to find
   thematic groupings (e.g. "Array manipulation", "Async programming").
5. If asked for **attribution**, note the content is CC-BY-4.0 licensed by
   Angelos Chalaris / 30 Seconds of Code — link to
   `https://30secondsofcode.org` rather than reproducing full articles.

## When NOT to reach for this

- The user wants current best practices for a fast-moving library/framework
  version — the archive is a fixed snapshot and may be stale on API details;
  verify with docs or web search for anything version-sensitive.
- The user wants production-grade code with tests, types, and edge-case
  handling — these are teaching snippets, not hardened library code.
