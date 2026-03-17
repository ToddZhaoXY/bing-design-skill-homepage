# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A static HTML presentation deck showcasing the capabilities of **Bing Design Skill 1.2**. Used for stakeholder demos and team presentations. No build system — open `deck.html` directly in a browser.

## Files

- `deck.html` — Single-file interactive presentation (~2200 lines of HTML/CSS/JS). Contains all styles inline using "Exceptional Horizons" design language.
- `*.png` / `*.jpeg` — Visual proof-of-concept screenshots embedded in or supporting the deck (card, layout, page, styling, showcase).

## Deck Design Language

The presentation uses its own visual identity ("Exceptional Horizons"), separate from the Bing Design Skill tokens it showcases:

| Variable | Value | Purpose |
|----------|-------|---------|
| `--c-cream` | `#EBE8E3` | Light section background |
| `--c-taupe` | `#6B655F` | Dark section background (even sections) |
| `--c-moss` | `#2A3826` | Dark accent |
| `--c-black` | `#111111` | Primary text |
| `--f-sans` | Helvetica Neue | Body text |
| `--f-serif` | Times New Roman | Display/accent text |

Sections alternate light (`--c-cream`) / dark (`--c-taupe`) backgrounds via `section:nth-child(even)`. Layout is full-viewport sections (`min-height: 80vh`) with centered content capped at `960px`.

## Relationship to Parent Skill

This deck presents the parent skill's capabilities. Supporting content lives in the sibling docs directory:

- `../deck-formal.md` — Formal slide outline (sections 1–9, some TODOs remain)
- `../deck-speaker-notes.md` — Speaker notes (Chinese/English)
- `../exceptional-horizons/` — Companion React+Vite app (`npm run dev` to start)

The parent skill (`bing-design-skill-1.2/`) contains the actual design system: tokens in `design-tokens/`, component specs in `references/`, icons in `icons/`.

## Editing Guidelines

- `deck.html` is self-contained — all CSS, HTML, and JS are in one file. No external dependencies.
- When editing section content, maintain the alternating light/dark pattern and the `.inner` wrapper for consistent max-width.
- Image assets are referenced by relative path from the HTML file.
- The parent `CLAUDE.md` (at `bing-design-skill-1.2/CLAUDE.md`) contains the authoritative rules for the design skill itself — particularly the constraint to never modify token names or values.
