# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static HTML clone of the Nanjing Anjuke (安居客) real estate homepage. Single-file, zero-dependency page that replicates the look and structure of `https://nanjing.anjuke.com/`.

## Commands

```bash
# Local development server
python -m http.server 8080
# Or: npx --yes serve .

# Start temporary public tunnel
npx --yes localtunnel --port 8080 --subdomain nanjing-anjuke

# Push to production (GitHub Pages)
git push github master      # pushes to xx668-com/-
git push github master:gh-pages
```

## Architecture

- **`index.html`** — Self-contained page (~1800 lines, ~70KB). All CSS and JS are embedded; no external dependencies except the favicon.ico reference to anjukestatic.com.
- Design follows the real Anjuke pattern: green `#27aa26` brand color, `#f6fdf6` background, 1180px centered layout, 880px main column + 285px sidebar.
- Content is hardcoded with representative Nanjing real estate data (districts, listings, price trends) — all simulated for demo purposes.

## Deployments

| Remote | URL |
|--------|-----|
| GitHub Pages | `https://xx668-com.github.io/-/` (source: `gh-pages` branch) |
| GitHub repo | `git@github.com:xx668-com/-.git` |
| Gitee remote | `https://gitee.com/xu-jingzhish/nanjing-anjuke-clone.git` |

GitHub Pages must be manually enabled at `https://github.com/xx668-com/-/settings/pages` → "Deploy from a branch" → `gh-pages` / `/(root)`.
