# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Who I Am

**Susanta Das, PhD** — Research Associate (Staff), Cleveland Clinic Lerner Research Institute, Cleveland OH.
Computational chemist working at the intersection of quantum computing, quantum chemistry, and biomolecular simulation.
PI: Prof. Kenneth M. Merz Jr. ("Kennie").

- Email: susanta.chemistry@gmail.com
- Google Scholar: https://scholar.google.co.in/citations?user=aroIfpMAAAAJ&hl=en
- GitHub: https://github.com/isusanta
- Source site (old): https://sites.google.com/view/susanta/home

## This Project

**Personal academic website** hosted on GitHub Pages.
- Live URL: https://isusanta.github.io
- Repo: https://github.com/isusanta/isusanta.github.io
- Template: Academic Pages (Jekyll) — forked from academicpages/academicpages.github.io
- Workflow: edit files here → `git add . && git commit -m "..." && git push` → check live site (~30s rebuild)
- No local Jekyll install. Push-and-check only.

## Current Build Status

### Done
- [x] Fork + GitHub Pages live
- [x] `_config.yml` — name, bio, email, Google Scholar, GitHub username set
- [x] `CLAUDE.md` — session context file created
- [x] Git push authentication — PAT token stored in macOS Keychain (works silently now)

### Next: Step 3 — `_data/navigation.yml`
Then steps 4–10 in order (see Build Order below).

## GitHub Accounts

| Account | Email | Use |
|---|---|---|
| `isusanta` | susanta.chemistry@gmail.com | **This website — always use this** |
| `dass11` | dass11@ccf.org | CCF enterprise — never use for personal site |

CCF laptop — no admin password. `code .` doesn't work from terminal; open VS Code manually via File → Open Folder.

## Design Decisions (final)

| Decision | Choice |
|---|---|
| Homepage | Research statement full-width first, photo below (`author_profile: false`, `layout: single`) |
| Research page | 5 project blocks, each with graphical abstract image (alternating left/right, 300px) |
| Publications | YAML data file `_data/publications.yml` rendered by Liquid loop in `publications.md` |
| Color accent | Deep teal `#006d77` — edit `$primary-color` in `_sass/theme/_default_light.scss` |
| Audience | Hiring committees + general academic audience |

## Files to Edit (only these — never touch other template files)

```
_config.yml               ← DONE
_data/navigation.yml      ← next
_data/publications.yml    ← create new
_pages/about.md           ← homepage
_pages/research.md        ← 5 project blocks
_pages/publications.md    ← loops over publications.yml
_pages/cv.md              ← CV + PDF download
_sass/theme/_default_light.scss  ← teal color ($primary-color, line 5)
images/profile.png        ← headshot (copy from ~/Documents/myWebPage/)
images/research/          ← graphical abstracts
files/cv.pdf              ← CV PDF (copy from ~/Documents/myWebPage/)
```

## Jekyll Architecture

This is a Jekyll static site. GitHub Pages rebuilds on every push (~30s). No local build needed.

**Theme:** Academic Pages (fork of Minimal Mistakes). `site_theme: "default"` in `_config.yml` loads `_sass/theme/_default_light.scss` (light) and `_default_dark.scss` (dark). The accent color is `$primary-color` in `_default_light.scss` — changing it updates links, base color, and hover states via CSS custom properties.

**Layouts** (in `_layouts/`):
- `single` — standard page; sidebar shown when `author_profile: true`
- `archive` — collection listing pages
- `cv-layout` — dedicated CV layout
- `talk` — talk entries

**Collections** (`_publications/`, `_talks/`, `_teaching/`, `_portfolio/`) output individual pages. This site skips the `_publications/` collection and uses `_data/publications.yml` + a Liquid loop in `_pages/publications.md` instead — gives full control over formatting.

**`_config.yml` is not hot-reloaded** by `jekyll serve`. Restart server after editing it.

## Build Order

| Step | File | Status |
|---|---|---|
| 1 | Clone + VS Code | ✓ Done |
| 2 | `_config.yml` | ✓ Done |
| 2b | `CLAUDE.md` + Git auth (PAT) | ✓ Done |
| 3 | `_data/navigation.yml` | **Next** |
| 4 | Copy assets (photo, images, CV PDF) | Pending |
| 5 | `_sass/variables.scss` — teal color | Pending |
| 6 | `_pages/about.md` — homepage | Pending |
| 7 | `_pages/research.md` — 5 projects | Pending |
| 8 | `_data/publications.yml` — 9 papers | Pending |
| 9 | `_pages/publications.md` — loop | Pending |
| 10 | `_pages/cv.md` — CV page | Pending |

## Research (for writing page content)

### Current (2023–Present)
- **Quantum computing:** SQD with LUCJ circuits on IBM quantum hardware. Benchmarked on NH3, CH4, H2O vs CASCI/FCI.
- **FLiBe/EWF/IBM:** DFT single-point energies (B3LYP, M06-2X, wB97X-D3, 6-31+G*/6-311+G*) on AIMD FLiBe molten salt clusters. Collaborators: Joe Morrone, Mario Motta (IBM Research).
- **QM/MM AIMD:** Proton transfer in malonaldehyde; PMF free energy; DFTB3/HF/STO-3G benchmarks; NEB.

### Prior (2019–2023, MSU)
- Computational NMR and metabolomics; QM/ML workflow for NMR/CCS prediction; AutoGraph clustering; POMICS web portal (pomics.org); enzyme catalysis (EnzyDock, QM/MM docking).

### Prior (2015–2019, Bar-Ilan)
- Nanocatalysis; heterogeneous catalysis of nano metal clusters via DFT and ab initio MD; Coupled Cluster studies.

## Key Publications (9 seed papers)

1. Computational NMR review — *Chemical Reviews* (R1 submitted 2026, coauthor)
2. SQD/LUCJ QM/MM AIMD — *JCTC* (in preparation)
3. Alchemical free energy (quantum-centric) — coauthor
4. Intermolecular interactions (quantum-centric) — coauthor
5. Molecular quantum computations on proteins — coauthor
6. CCS prediction — *Analytical Chemistry* — DOI: 10.1021/acs.analchem.0c00768
7. NMR/metabolite structure — *Chemical Reviews* — DOI: 10.1021/acs.chemrev.0c00901
8. QM/MM method — *JCTC* — DOI: 10.1021/acs.jctc.7b00964
9. Metabolomics — *JASMS* — DOI: 10.1021/jasms.1c00315

## Career Timeline

| Period | Position | Institution |
|---|---|---|
| Oct 2023–Present | Research Associate (Staff) | Cleveland Clinic LRI, USA |
| Apr 2019–Oct 2023 | Postdoc | Michigan State University, USA |
| Aug 2015–Apr 2019 | Postdoc | Bar-Ilan University, Israel |
| Jan 2010–Aug 2015 | PhD Candidate | CSIR-NCL, Pune, India |

## Education

| Degree | Field | Institution | Year |
|---|---|---|---|
| PhD | Computational Chemistry | CSIR-NCL, India | 2010–2015 |
| MSc | Chemistry | Visva-Bharati Central University | 2007–2009 |
| BSc | Chemistry (Hons.) | University of Burdwan | 2004–2007 |

## Assets in ~/Documents/myWebPage/ (to copy into repo)

| File | Copy to | Purpose |
|---|---|---|
| `ccsWorkflowV2Color.png` | `images/research/` | Project 4: NMR/metabolomics graphical abstract |
| `analchem1.png` | `images/research/` | Project 4/5 |
| `Gallery/Nuclear_quantum_effect.png` | `images/research/` | Project 1/2 |
| Your headshot photo | `images/profile.png` | Homepage photo |
| Your CV PDF | `files/cv.pdf` | CV page download |

## Writing Style

- Professional but direct. No fluff.
- Lead with quantum computing (current work), then metabolomics/NMR (prior).
- No em dashes. Use commas or semicolons instead.
- Publications: text list with DOI links only — no image thumbnails.
- Define acronyms on first use: e.g., "stochastic quantum dynamics (SQD)".
- Technical but accessible to a broad chemistry audience.

## Daily Git Workflow

```bash
git add .
git commit -m "short descriptive message"
git push
# wait ~30 seconds → check https://isusanta.github.io
```
