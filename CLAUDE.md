# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Ilena is a static marketing/landing page for an AI-powered songwriting assistant app. The site is deployed via GitHub Pages to `www.ilena.app`.

## Deployment

No build step required. The site is a single `index.html` file served directly by GitHub Pages. Push to `main` to deploy.

## Architecture

**Single-file site:** All HTML, CSS, and layout lives in `index.html` (~770 lines). There is no JavaScript, no external stylesheets, and no build tooling.

**Key design tokens (CSS variables in `index.html`):**
- Primary accent: `#7c5cfc` (purple)
- Dark background theme
- Typography uses `clamp()` for fluid scaling

**Assets:**
- `assets/ilena.png` — logo
- `assets/favicon.ico` / `assets/ilena.ico` — favicons
- `assets/BrandBook_v3.pdf` — brand guidelines (reference before making visual changes)

## Content Structure

Sections in `index.html` (in order): Hero → Problem → Features → How It Works → Credibility → Pricing → Tech Stack → Footer.

Pricing tiers: Free, Pro, Studio.

## Conventions

- All styling is inline within `index.html` via a `<style>` block — do not create separate `.css` files unless the user requests it.
- `robots.txt` intentionally blocks all crawlers (`Disallow: /`) — this is by design for the beta period.
- The `.gitignore` contains Java/Helm/Skaffold entries inherited from a template; these can be ignored.
