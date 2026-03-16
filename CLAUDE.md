# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Yarnlly is a static "link in bio" landing page for a handmade crochet business based in Sydney, Australia. It is hosted on GitHub Pages at `yarnlly.com` (configured via `CNAME`).

## Architecture

This is a single-file static site with no build tools, frameworks, or dependencies:

- `index.html` — the entire site: inline CSS, HTML structure, and inline JS (analytics only)
- `assets/images/` — logo and other images
- `sitemap.xml` — single URL sitemap for SEO
- `robots.txt` — allows all crawlers and points to sitemap

All styling lives in a `<style>` block inside `index.html`. There is no separate CSS file, no JavaScript file, and no package manager.

## Deployment

Push to the `main` branch. GitHub Pages serves the site automatically via the `CNAME` record pointing to `yarnlly.com`.

## Brand Design Tokens

CSS variables defined in `:root` — match these when making visual changes:

| Variable | Value | Usage |
|---|---|---|
| `--primary-pink` | `#d69896` | Primary buttons |
| `--accent-teal` | `#7caca8` | Secondary buttons, subtitle text |
| `--bg-color` | `#fbf9f9` | Page background |
| `--text-color` | `#4a3e3d` | Body text |

Font: **Nunito** (loaded from Google Fonts).

## Analytics

Two analytics integrations are embedded in `index.html`:
- **Google Analytics** — tracking ID `G-NZZ2JFJ0R3`
- **Microsoft Clarity** — tracking ID `vseyvxljm5`
