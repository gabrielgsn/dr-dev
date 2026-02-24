# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

dr.dev is a MkDocs Material site that teaches AI coding / vibe coding to non-programmers. All content is in Brazilian Portuguese using plain ASCII only (no accented characters like `é`, `ã`, `ç` — use `e`, `a`, `c` instead).

Live site: https://gabrielgsn.github.io/dr-dev/

## Commands

```bash
# Local dev server (Windows requires encoding fix)
PYTHONIOENCODING=utf-8 mkdocs serve

# Build site
PYTHONIOENCODING=utf-8 mkdocs build

# Deploy happens automatically via GitHub Actions on push to main
```

Dependencies are installed globally via Miniconda (`mkdocs-material`, `mkdocs-minify-plugin`). No virtualenv needed. If installing fresh: `pip install -r requirements.txt`.

## Architecture

- `docs/` — All Markdown content pages
  - `index.md` — Homepage (hero section, feature cards, module overview table)
  - `sobre.md` — About the project, target audience, prerequisites
  - `primeiros-passos.md` — Step-by-step setup guide (GitHub, VS Code, Git, Node.js, Claude Code install)
  - `modulos/` — Learning modules (numbered `01-`, `02-`, etc.)
    - `index.md` — Trilha overview with Mermaid roadmap diagram
    - `01-o-que-e-ai-coding.md` — Module 1: What is AI Coding
    - `02-prompt-engineering.md` — Module 2: Prompt Engineering techniques
    - `03-ferramentas.md` — Module 3: Tools ecosystem (Claude, Cursor, Bolt, etc.)
  - `recursos/` — Reference pages
    - `glossario.md` — Glossary of technical terms
    - `links-uteis.md` — Curated links
    - `faq.md` — FAQ
- `includes/abbreviations.md` — Abbreviation definitions auto-appended to every page via `pymdownx.snippets` (adds hover tooltips for terms like LLM, API, etc.)
- `overrides/` — Material theme template overrides (extends `base.html`)
- `docs/assets/stylesheets/extra.css` — Custom CSS (hero, grid cards, trilha styling)
- `mkdocs.yml` — Site config, navigation structure, extensions, and plugins
- `.github/workflows/ci.yml` — Auto-deploys to GitHub Pages on push to `main`

## Content Conventions

- **Target audience:** Experienced professionals (engineering background) with no programming experience
- Keep content concise and practical; use engineering analogies
- Navigation structure is defined in `mkdocs.yml` under `nav:` — update it when adding new pages
- New abbreviations/terms go in `includes/abbreviations.md`
- 7 modules planned; modules 1-3 exist, modules 4-7 are future work

## Current State (as of 2026-02)

### Completed
- Full MkDocs Material site setup with dark/light mode, search, code copy, tabs
- Homepage with hero section, 3 feature cards, 7-module overview table
- About page (`sobre.md`) with audience description and learning outcomes
- Primeiros Passos guide (`primeiros-passos.md`): 6-step setup walkthrough (GitHub account, VS Code, Git, Node.js, Claude Code install, first conversation)
- Module 1: What is AI Coding (concepts, vibe coding, use cases)
- Module 2: Prompt Engineering (techniques, examples, best practices)
- Module 3: Tools ecosystem (Claude, Cursor, Bolt, Lovable comparisons)
- Trilha overview page with Mermaid roadmap
- Resources: Glossary, FAQ, Curated Links
- GitHub Actions CI/CD for auto-deploy
- Custom CSS for hero, cards, trilha items
- Abbreviations system for technical term tooltips
- Homepage prominently links to Primeiros Passos as primary CTA for beginners
- Ready-made Claude prompt on Primeiros Passos page for users who need AI-guided setup help

### Not Yet Built
- Module 4: First App (build something real)
- Module 5: Agent Orchestration
- Module 6: Deploy and Launch
- Module 7: Staying Updated

## Key Design Decisions

- Homepage primary CTA goes to Primeiros Passos (not Modulos) since target users need environment setup first
- Primeiros Passos includes a copy-paste prompt for Claude.ai so users who are completely non-technical can get AI-guided help with setup
- Mermaid diagrams used for visual roadmap (blue = available, gray = coming soon)
- Material theme features: instant navigation, sticky tabs, footer nav, search suggestions
- Font: Inter for text, JetBrains Mono for code
- Color scheme: indigo primary, deep purple accent
