# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal India trip planner website for a family of 3 (Raksha, Inchara, Raghu). Trip dates: July 26 – September 5, 2026. The site is a single self-contained HTML file with interactive checklists.

## Architecture

**`india-trip-2026.html`** — the canonical, latest file. Everything else is legacy reference material.

- Single HTML file with inline CSS and JS (no build system, no dependencies, no server needed)
- Open directly in a browser to use; edit in any text editor
- Design: dark-mode-first with light/dark toggle, glassmorphism cards, bento grid dashboard, Playfair Display + Inter fonts via Google Fonts CDN
- Checklist state persists in `localStorage` under key `india-trip-2026-v2`

### Where to edit content

All checklist/task data lives in the **`DATA` object** inside the `<script>` block near the bottom of the file. It has four top-level keys: `canada`, `packing`, `admin`, `shopping`. Each contains arrays of category objects with `tasks` arrays.

Static content (itinerary timeline, family visits, places, accommodation table) is in the HTML body above the script block — edit the markup directly.

### Navigation

8 tabs controlled by `data-tab` attributes on `.nav-btn` buttons, mapping to `#sec-{tab}` section divs.

## Legacy files (do not edit)

`India_Checklist2.html`, `India_StayPlan_2026.html`, `India_ToDo_2026.html`, `India_Trip_Plan_2026.html` — older drafts. The `.docx`, `.xlsx`, and `.pdf` files are reference snapshots. Use only for cross-checking information if needed.

## Preview

No server required. Double-click `india-trip-2026.html` to open in a browser. If a local server is needed for tools, a Python http.server config exists in `.claude/launch.json` but requires Python to be installed.
