---
name: portfolio-styling
description: Enforce consistent CSS variables and styling across portfolio pages
autoInvoke:
  - pattern: "*.html"
---

# Portfolio Styling Conventions

All portfolio pages share a consistent CSS variable system and visual style. Follow these rules when adding or modifying any HTML page.

## CSS Variables (must be in every page's `:root`)
```css
:root {
  --color-bg: #fafafa;
  --color-text: #1a1a1a;
  --color-muted: #555;
  --color-accent: #2563eb;
  --color-accent-light: #eff6ff;
  --color-border: #e5e7eb;
  --color-card-bg: #fff;
  --max-width: 820px;  /* 940px for index.html only */
}
```

## Rules
1. **Always use CSS variables** — never hardcode colors that have a variable equivalent
2. **Font stack**: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`
3. **Content width**: `--max-width: 820px` for detail pages, `940px` for index.html
4. **Accent color**: `#2563eb` (blue) is the brand color — use `--color-accent`

## Page type label colors
Different page types use different label background colors (hardcoded, not variables):
- PRD pages: `#2563eb` (blue)
- Case studies: `#1e3a5f` (dark blue)
- Teardown: `#611f69` (purple)
- Metrics: `#059669` (green)
- Research: check existing page for its color

## Exceptions
The demo apps (todo-prioritizer.html, meeting-summarizer.html, pm-toolkit.html, collab-focus-mode.html) have their own independent styling systems — this skill does not apply to those files.
