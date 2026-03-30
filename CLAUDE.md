# CLAUDE.md — samuelrward.github.io

## What this repo is
Personal academic website for Samuel Ward, computational astrophysicist.
Built on the [Strata template by HTML5 UP](https://html5up.net/strata).
Hosted via GitHub Pages — pushing to `main` deploys live immediately.

## Stack
- Plain HTML/CSS — no build step, no framework, no JavaScript bundler
- Template assets live in `assets/` (CSS, JS, webfonts)
- Images live in `images/`
- Each page is a standalone `.html` file in the repo root

## File conventions
- All pages share the same header/nav and footer structure — copy from `index.html` as the reference
- Nav links are relative (e.g. `research.html`, not `/research.html`)
- Image paths are relative (e.g. `images/foo.jpg`)

## Off-limits files — do not modify
- `assets/` — all CSS, JS, and webfont files (template internals)
- `images/` — all image files

## Handling images
When a page calls for an image that doesn't exist yet:
- Create an inline SVG placeholder directly in the HTML — a simple grey rectangle with the filename written on it (e.g. `PLACEHOLDER: images/research_fig1.jpg`)
- Never add actual image files
- Never reference image files that don't already exist without adding a placeholder

## Writing style
- Accessible but professional — clear to a non-specialist, credible to an expert
- Avoid jargon without explanation on public-facing pages (Research, Outreach)
- CV & Publications can be more technical
- First person is fine; avoid puffery ("groundbreaking", "cutting-edge")

## When uncertain about content
- Make your best attempt and flag it with a `<!-- REVIEW: ... -->` HTML comment inline
- Don't ask before proceeding — complete the task and surface questions at the end

## Git behaviour
- Stage and commit changes when a task is complete
- Write clear, specific commit messages (e.g. `Add CV & Publications page content`)
- **Do not push** — the user will push manually after reviewing

## Page inventory
| File | Status |
|------|--------|
| `index.html` | Complete — treat as reference, edit conservatively |
| `research.html` | Complete, edit conservatively |
| `cv_publications.html` | Complete, edit conservatively |
| `outreach.html` | Stub — needs content |
| `interests.html` | Stub — needs content |