# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Who I Am

**Susanta Das, PhD** — Research Associate, Cleveland Clinic, Cleveland OH.
Computational chemist working at the intersection of quantum computing, quantum chemistry, and biomolecular simulation.
PI: Prof. Kenneth M. Merz Jr. ("Kennie").

- Email: susanta.chemistry@gmail.com
- Google Scholar: https://scholar.google.co.in/citations?user=aroIfpMAAAAJ&hl=en (594 citations, April 2026)
- GitHub: https://github.com/isusanta
- LinkedIn: https://www.linkedin.com/in/dr-das/
- Source site (old): https://sites.google.com/view/susanta/home

## This Project

**Personal academic website** hosted on GitHub Pages.
- Live URL: https://isusanta.github.io
- Repo: https://github.com/isusanta/isusanta.github.io
- Template: Academic Pages (Jekyll) — forked from academicpages/academicpages.github.io
- Workflow: edit files here → `git add . && git commit -m "..." && git push` → check live site (~30s rebuild)
- No local Jekyll install. Push-and-check only.

## GitHub Accounts

| Account | Email | Use |
|---|---|---|
| `isusanta` | susanta.chemistry@gmail.com | **This website — always use this** |
| `dass11` | dass11@ccf.org | CCF enterprise — never use for personal site |

CCF laptop — no admin password. `code .` doesn't work from terminal; open VS Code manually via File → Open Folder.

## Current Build Status (as of 2026-04-26)

| Step | File | Status |
|---|---|---|
| 1 | Clone + VS Code | ✓ Done |
| 2 | `_config.yml` — name, bio, email, Google Scholar, GitHub, LinkedIn | ✓ Done |
| 3 | `_data/navigation.yml` — Research, Publications, CV | ✓ Done |
| 4 | Copy assets (headshot, research images, CV PDF) | **Pending** |
| 5 | `_sass/theme/_default_light.scss` — deep teal `#006d77` | **Pending** |
| 6 | `_pages/about.md` — landing page (Option A: opener + 4 research blocks + career table) | ✓ Done |
| 7 | `_pages/research.md` — 5 project blocks with graphical abstracts | **Pending** |
| 8 | `_data/publications.yml` — 26 papers (24 journal + 2 book chapters) | ✓ Done |
| 9 | `_pages/publications.html` — Liquid loop, two sections, Susanta Das bolded | ✓ Done |
| 10 | `_pages/cv.md` — positions, education, awards, skills, review service | ✓ Done |
| 11 | `assets/css/main.scss` — Inter font (Google Fonts, weights 300–700) | ✓ Done |

**Next priority:** Step 4 (copy assets) — headshot unlocks the sidebar photo; CV PDF unlocks the download button.

## Design Decisions (final)

| Decision | Choice |
|---|---|
| Homepage | `author_profile: true` (sidebar shown); opener + 4 research blocks + career table |
| Research page | 5 project blocks, each with graphical abstract image (alternating left/right, 300px) |
| Publications | `_data/publications.yml` rendered by Liquid loop; two sections: Journal Articles & Preprints / Book Chapters |
| Color accent | Deep teal `#006d77` — edit `$primary-color` in `_sass/theme/_default_light.scss` (line 5) |
| Font | Inter (Google Fonts, weights 300–700) — loaded in `assets/css/main.scss` |
| Audience | Hiring committees + general academic audience |
| Citation count | Manual update — edit `_pages/publications.html` line 9 |

## Files to Edit (only these — never touch other template files)

```
_config.yml                          ← DONE (name, bio, social links)
_data/navigation.yml                 ← DONE (Research, Publications, CV)
_data/publications.yml               ← DONE (26 papers)
_pages/about.md                      ← DONE (landing page)
_pages/publications.html             ← DONE (Liquid loop, 2 sections)
_pages/cv.md                         ← DONE (positions, education, skills)
_pages/research.md                   ← PENDING (5 project blocks)
_sass/theme/_default_light.scss      ← PENDING (teal color, $primary-color line 5)
assets/css/main.scss                 ← DONE (Inter font, Google Fonts import)
images/profile.png                   ← PENDING (copy headshot from ~/Documents/myWebPage/)
images/research/                     ← PENDING (copy graphical abstracts)
files/cv.pdf                         ← PENDING (copy CV PDF)
```

## Jekyll Architecture

This is a Jekyll static site. GitHub Pages rebuilds on every push (~30s). No local build needed.

**Theme:** Academic Pages (fork of Minimal Mistakes). `site_theme: "default"` in `_config.yml` loads `_sass/theme/_default_light.scss` (light) and `_default_dark.scss` (dark). The accent color is `$primary-color` in `_default_light.scss` — changing it updates links, base color, and hover states via CSS custom properties.

**Layouts** (in `_layouts/`):
- `single` — standard page; sidebar shown when `author_profile: true`
- `archive` — collection listing pages (used by publications.html and cv.md)
- `cv-layout` — dedicated CV layout
- `talk` — talk entries

**Collections** (`_publications/`, `_talks/`, `_teaching/`, `_portfolio/`) output individual pages. This site skips the `_publications/` collection and uses `_data/publications.yml` + a Liquid loop in `_pages/publications.html` instead — gives full control over formatting.

**`_config.yml` is not hot-reloaded** by `jekyll serve`. Restart server after editing it.

## Assets in ~/Documents/myWebPage/ (still to copy into repo)

| File | Copy to | Purpose |
|---|---|---|
| `ccsWorkflowV2Color.png` | `images/research/` | NMR/metabolomics graphical abstract |
| `analchem1.png` | `images/research/` | NMR/metabolomics |
| `Gallery/Nuclear_quantum_effect.png` | `images/research/` | Quantum computing |
| Headshot photo | `images/profile.png` | Sidebar photo |
| CV PDF | `files/cv.pdf` | CV page download button |

## Publications Data

All 26 papers are in `_data/publications.yml` with fields: `title`, `authors`, `venue`, `year`, `doi`, `type`.
- `type: "journal"` — 24 entries (journal articles + arXiv preprints)
- `type: "book_chapter"` — 2 entries
- "Susanta Das" is bolded automatically via Liquid `replace` in `_pages/publications.html`
- Citation count is hardcoded in `_pages/publications.html` line 9 — update manually each quarter

## Writing Style

- Professional but direct. No fluff.
- Lead with quantum computing (current work), then QM/MM, then metabolomics/NMR (prior).
- No em dashes. Use commas or semicolons instead.
- Publications: text list with DOI links only — no image thumbnails.
- Define acronyms on first use: e.g., "stochastic quantum dynamics (SQD)".
- Technical but accessible to a broad chemistry audience.

## Phase 3 (Future)

- Apply deep teal color `#006d77` once Phase 2 assets are in
- Add News/Updates section
- Connect custom domain (e.g., susantadas.com)
- Add quantum computing project page
- Add POMICS portal section

## Daily Git Workflow

```bash
git add <files>
git commit -m "short descriptive message"
git push
# wait ~30 seconds → check https://isusanta.github.io
```
