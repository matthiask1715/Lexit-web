# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

LexIT Executive Governance Website - a static consulting business website for IT-Compliance and IT-Governance consulting services targeting SMEs in Austria and Germany.

## Tech Stack

- **Framework:** Astro 5.x (Static Site Generation)
- **Styling:** Tailwind CSS v4
- **Typography:** IBM Plex Sans (Google Fonts)
- **JavaScript:** None in frontend (pure SSG)

## Commands

```bash
npm run dev      # Start dev server on localhost:4321
npm run build    # Production build to /dist
npm run preview  # Preview production build locally
```

## Architecture

### Single-Page Structure
The site is a single homepage (`src/pages/index.astro`) with four sections navigated via anchor links:
1. Hero/Opening Statement
2. Leistungsübersicht (Services) - 3 service cards
3. Positionierungsaussage (Positioning)
4. Zielgruppen-Qualifikation (Target Audience)

### Key Directories
- `src/components/` - Header.astro (navigation), Footer.astro (contact & legal)
- `src/layouts/BaseLayout.astro` - Master layout with SEO meta tags, Open Graph, and font loading
- `src/styles/global.css` - Design system with Tailwind theme tokens (colors, typography, spacing)
- `src/styles/print.css` - Print-optimized stylesheet
- `public/` - Logo variants (Lexit_Textlogo.png, Lexit_x.png) and favicons

### Design Principles
- **Board Document Aesthetic:** Clean, professional design with generous whitespace
- **Print-First:** Website optimized for printing as professional documents
- **Zero Runtime JS:** Pure static HTML/CSS output
- **Mobile-First:** Responsive with md breakpoints

## Design System

Colors defined in `src/styles/global.css` under `@theme`:
- Trust Blue (#1F3A5F) - Headlines, links
- Ink (#111827) - Body text
- Controlled Amber (#E07A2F) - Hover states, accents

## Content

All page content is in German and located directly in `src/pages/index.astro`. New pages go in `src/pages/` (e.g., `impressum.astro`).
