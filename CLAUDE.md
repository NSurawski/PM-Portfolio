# PM Portfolio

## Project Overview

Personal Product Management portfolio site for Nicole Surawski. Showcases the transition from Solutions Consulting to Product Management in B2B SaaS. Hosted on GitHub Pages at https://nsurawski.github.io/PM-Portfolio/.

## Repository Structure

```
PM-Portfolio/
├── index.html                  # Main portfolio page (single-page, self-contained)
├── prd-meeting-summarizer.html # PRD for Meeting Summarizer app
├── prd-todo-prioritizer.html   # PRD for To-Do Prioritizer app
├── meeting-summarizer.html     # Live demo — Meeting Summarizer (standalone, no API key needed)
├── todo-prioritizer.html       # Live demo — To-Do Prioritizer (standalone)
├── README.md                   # Repo README
└── CLAUDE.md                   # This file
```

## Tech Stack

- **Static HTML/CSS** — no build step, no bundler, no framework for the portfolio pages and PRDs
- **React 18 + Tailwind CSS via CDN** — used in the two app demos (loaded from unpkg/cdn.tailwindcss.com)
- **Babel standalone** — in-browser JSX transpilation for the demo apps
- **GitHub Pages** — hosting, deployed from the `source` branch

## Key Architecture Decisions

- All files are self-contained HTML — no dependencies, no `npm install`, no build pipeline
- The Meeting Summarizer demo uses a **hardcoded sample response** instead of calling the Claude API, so visitors can try it without an API key
- The To-Do Prioritizer demo includes dark mode support with CSS class overrides on `body.dark-mode`
- All app state persists to `localStorage` (separate keys: `meetingSummariesDemo`, `todo-prioritizer-tasks`, etc.)

## Git Conventions

- **Branch:** `source` is the main/deploy branch (GitHub Pages deploys from here)
- **Remote:** `origin` → `https://github.com/NSurawski/PM-Portfolio.git`
- **Commit style:** conventional commits (`feat:`, `fix:`, `docs:`)

## Style Guidelines

- Portfolio pages use a consistent CSS variable system (see `:root` in `index.html`)
- Color accent: `#2563eb` (blue)
- PRD pages share the same visual style as the portfolio (same CSS variables, same font stack)
- Demo apps have their own independent styling (Meeting Summarizer: dark theme, To-Do Prioritizer: light/dark with Tailwind)

## When Making Changes

- After editing any file, push to `source` — GitHub Pages auto-deploys
- If adding a new portfolio artifact (PRD, demo, etc.), also add a link from the relevant project card in `index.html`
- The To-Do Prioritizer source of truth is in `/Users/nicolesurawski/Documents/PM projects/todo-prioritizer/todo-prioritizer.html` — the copy in this repo should stay in sync
- The Meeting Summarizer source of truth is in `/Users/nicolesurawski/Documents/PM projects/meeting-summarizer/` (Vite project) — the demo version in this repo is a simplified standalone copy
