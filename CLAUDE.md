# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About this project

This is **yourcoach-integration-docs**, a documentation site for the YourCoach integration platform, built with [Mintlify](https://mintlify.com). All content is written in MDX (Markdown + JSX components). Configuration lives in `docs.json`.

## Commands

```bash
# Install CLI (requires Node.js 19+)
npm i -g mint

# Preview locally at http://localhost:3000
mint dev

# Preview on a custom port
mint dev --port 3333

# Check for broken links
mint broken-links

# Update CLI to match production version
npm mint update
```

There is no build step or test suite — the Mintlify CLI handles rendering. Deployment happens automatically when changes are pushed to the default branch (via the Mintlify GitHub app).

## Architecture

**`docs.json`** — the single source of truth for site configuration: navigation tabs/groups/pages, colors, logo, navbar, footer, and contextual AI menu options. Every `.mdx` page must be registered here to appear in the nav.

**Content directories:**
- `essentials/` — guides on Mintlify's writing and configuration features
- `agent-ready/` — docs for Mintlify's AI-specific components (`Prompt`, `Visibility`, `Contextual`)
- `ai-tools/` — setup guides for Claude Code, Cursor, and Windsurf
- `api-reference/` — API docs driven by `api-reference/openapi.json` (OpenAPI 3.1)
- `snippets/` — reusable MDX partials, imported via `<Snippet>` in pages

**`AGENTS.md`** — instructions for AI coding tools working in this repo (mirrors the style guidance below). This is the Mintlify-standard file that AI tools read for project context.

## Content conventions

- Active voice, second person ("you")
- Sentence case for headings
- Bold for UI elements: **Settings**
- Code formatting for file names, commands, paths, and inline code references
- One idea per sentence; lead instructions with the user's goal

## AI skill for Mintlify

For comprehensive Mintlify component and configuration reference, install the skill:

```bash
npx skills add https://mintlify.com/docs
```

