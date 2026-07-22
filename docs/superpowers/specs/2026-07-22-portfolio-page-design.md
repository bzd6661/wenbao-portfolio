# Architecture Portfolio Page — Design

Date: 2026-07-22
Status: Approved by user (approach A)

## Goal

A single-page English portfolio to share with prospective employers. Two projects,
each telling the story "parametric process (GIF) → physical artefact (photo)" via a
scroll-driven crossfade. Tone: gallery-minimal, large type, generous whitespace.

## Assets

| Project | Process GIF | Final model photo |
|---|---|---|
| Private House (2022) | `assets/220228-private-house.gif` | `IMG_3850.jpg` → compressed web copy |
| Rijksdorf Tourist Complex | `assets/Rijksdorf Tourist Complex.gif` | `assets/IMG_9806.JPG` |

`IMG_3850.jpg` (4.7 MB) is resized/compressed to ~2000 px wide web copy; original untouched.

## Structure (single `index.html`)

1. **Hero** — near-black background, large serif name (placeholder "YOUR NAME"),
   subtitle "Architecture & Computational Design", scroll hint.
2. **Project 1 — Private House** — full-viewport pinned section. GIF plays full-bleed
   with caption; scrolling crossfades GIF → model photo (photo scales 1.05→1),
   caption text swaps ("Parametric study" → "From algorithm to artefact").
3. **Project 2 — Rijksdorf Tourist Complex** — same pinned crossfade pattern.
4. **Contact** — email placeholder + copyright.

## Tech

- Plain HTML/CSS/JS, GSAP + ScrollTrigger from CDN. No build step.
- `prefers-reduced-motion`: no pinning, sections stack normally.
- Mobile (<768px): no pin; GIF and photo shown stacked sequentially.
- Images `loading="lazy"` below the fold.

## Out of scope (later)

- Deployment (GitHub Pages) — user wants local first.
- Real name / email / project blurb revisions — placeholders now, user edits after.
