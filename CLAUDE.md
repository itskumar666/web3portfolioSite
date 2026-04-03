# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file vanilla HTML5 portfolio website for a Blockchain Engineer. There is no build system, package manager, or framework — all HTML, CSS, and JavaScript live in `index.html`.

## Running Locally

Open `index.html` directly in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8000
# or
npx serve .
```

## Architecture

Everything is in `web3portfolioSite/index.html`:

- **CSS**: Embedded in `<style>` tags — uses CSS Grid, Flexbox, and keyframe animations with a purple gradient theme (`#667eea` → `#764ba2`)
- **JavaScript**: Embedded in `<script>` tags at the bottom — vanilla JS only, no libraries. Three behaviors:
  1. Smooth scroll for nav anchor links
  2. Sticky nav backdrop blur on scroll
  3. Intersection Observer for scroll-triggered fade-in animations on `.animate-in` elements
- **Icons**: Font Awesome loaded via CDN (`cdnjs.cloudflare.com`)

## Page Structure

Sections in order: Hero/Header → sticky `<nav>` → `#experience` → `#projects` → `#skills` → `#certificates`

Responsive breakpoints: `768px` (tablet) and `480px` (mobile).

## Deployment

Static site — deploy to GitHub Pages, Vercel, Netlify, or any static host. The git remote is `https://github.com/itskumar666/web3portfolioSite.git`.
