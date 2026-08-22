---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<p class="latest-preprint">
  <span class="latest-preprint__label">Latest preprint</span>
  <a href="https://doi.org/10.48550/arXiv.2607.28548">Quantum Computing Enabled <em>ab initio</em> Molecular Dynamics Simulations</a>
  <span class="latest-preprint__id">arXiv:2607.28548</span>
</p>

<style>
.latest-preprint {
  display: flex;
  align-items: baseline;
  flex-wrap: wrap;
  gap: 0.5em 0.8em;
  margin: 1.2em 0 2em;
  padding: 0.85em 1.1em;
  border-left: 4px solid #006d77;
  border-radius: 0 8px 8px 0;
  background: rgba(0,109,119,0.07);
  font-size: 0.93em;
  line-height: 1.5;
}
.latest-preprint__label {
  font-family: 'Exo 2', 'Inter', sans-serif;
  font-weight: 700;
  font-size: 0.76em;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #006d77;
  flex-shrink: 0;
}
.latest-preprint a {
  color: #1f2d2f !important;
  text-decoration: none !important;
  border-bottom: 1px solid #9fc3c7;
  font-weight: 600;
}
.latest-preprint a:hover { color: #006d77 !important; border-bottom-color: #006d77; }
.latest-preprint__id { font-size: 0.85em; color: #7a8688; }
@media (prefers-color-scheme: dark) {
  .latest-preprint { background: rgba(0,109,119,0.2); border-left-color: #4bb3bd; }
  .latest-preprint__label { color: #7fd3db; }
  .latest-preprint a { color: #e6edee !important; border-bottom-color: #3d5153; }
  .latest-preprint a:hover { color: #7fd3db !important; border-bottom-color: #7fd3db; }
  .latest-preprint__id { color: #8f9fa1; }
}
</style>

## In the Press

<div class="press-list">
{% for p in site.data.press %}
  <article class="press-item">
    {% if p.image %}
    <a class="press-thumb" href="{{ p.url }}" target="_blank" rel="noopener noreferrer" tabindex="-1" aria-hidden="true">
      <img src="/images/press/{{ p.image }}" alt="{{ p.image_alt | default: p.outlet }}" loading="lazy">
    </a>
    {% endif %}
    <div class="press-body">
      <div class="press-meta">
        <span class="press-outlet">{{ p.outlet }}</span>
        <span class="press-date">{{ p.date }}</span>
      </div>
      <h3 class="press-title"><a href="{{ p.url }}" target="_blank" rel="noopener noreferrer">{{ p.title }}</a></h3>
      {% if p.note %}<p class="press-note">{{ p.note }}</p>{% endif %}
      {% if p.quote %}
        <blockquote class="press-quote">
          <span class="press-quote__text">{{ p.quote }}</span>
          <cite>{{ p.attrib }}</cite>
        </blockquote>
      {% endif %}
      {% if p.paper %}<a class="press-paper" href="{{ p.paper }}">Read the paper →</a>{% endif %}
    </div>
  </article>
{% endfor %}
</div>

<style>
.press-list { margin: 1.5em 0 0; }
.press-item {
  display: flex;
  align-items: flex-start;
  gap: 1.1em;
  padding: 1.15em 0;
  border-bottom: 1px solid #eef2f2;
}
.press-item:last-child { border-bottom: 0; }
.press-body { flex: 1; min-width: 0; }
/* Fixed-width thumb so the text column starts at the same x on every row,
   whatever the source image aspect ratio happens to be. */
.press-thumb {
  flex: 0 0 116px;
  display: block;
  border-bottom: 0 !important;
}
.press-thumb img {
  display: block;
  width: 116px;
  height: 88px;
  object-fit: cover;
  border-radius: 6px;
  background: #f4f7f7;
  border: 1px solid #e4ecec;
}
/* Stack on phones: a 116px thumb next to two lines of wrapped text reads worse
   than the image sitting above its own headline. */
@media (max-width: 600px) {
  .press-item { flex-direction: column; gap: 0.7em; }
  .press-thumb { flex: none; }
  .press-thumb img { width: 100%; height: 150px; }
}
.press-meta { display: flex; align-items: baseline; gap: 0.7em; flex-wrap: wrap; }
.press-outlet {
  font-family: 'Exo 2', 'Inter', sans-serif;
  font-weight: 700;
  font-size: 0.74em;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #006d77;
}
.press-date { font-size: 0.76em; color: #7a8688; }
.press-title { margin: 0.3em 0 0; font-size: 1.02em; line-height: 1.4; }
.press-title a { color: #1f2d2f !important; text-decoration: none !important; border-bottom: 1px solid #cfdadb; }
.press-title a:hover { color: #006d77 !important; border-bottom-color: #006d77; }
.press-note { margin: 0.4em 0 0; font-size: 0.88em; line-height: 1.55; color: #4a5859; }
.press-paper {
  display: inline-block;
  margin-top: 0.55em;
  font-size: 0.83em;
  font-weight: 600;
  color: #006d77 !important;
  text-decoration: none !important;
  border-bottom: 1px solid transparent;
}
.press-paper:hover { border-bottom-color: #006d77; }
.press-quote {
  margin: 0.8em 0 0;
  padding: 0.1em 0 0.1em 1em;
  border-left: 3px solid #006d77;
  font-size: 0.92em;
  line-height: 1.55;
  font-style: italic;
  color: #33474a;
}
/* Quote marks must wrap the TEXT, not the blockquote: an ::after on the
   blockquote renders below the <cite>, stranding a lone closing mark. */
.press-quote__text::before { content: '\201C'; }
.press-quote__text::after  { content: '\201D'; }
.press-quote cite {
  display: block;
  margin-top: 0.4em;
  font-style: normal;
  font-size: 0.82em;
  color: #7a8688;
}
@media (prefers-color-scheme: dark) {
  .press-item { border-bottom-color: #2c3a3c; }
  .press-thumb img { background: #1c2426; border-color: #2c3a3c; }
  .press-date, .press-quote cite { color: #8f9fa1; }
  .press-title a { color: #e6edee !important; border-bottom-color: #33474a; }
  .press-title a:hover { color: #7fd3db !important; border-bottom-color: #7fd3db; }
  .press-note { color: #a9b8ba; }
  .press-quote { color: #c3d0d2; border-left-color: #4bb3bd; }
  .press-outlet, .press-paper { color: #7fd3db !important; }
  .press-paper:hover { border-bottom-color: #7fd3db; }
}
</style>

## Featured Work

<div class="cover-gallery">
{% for c in site.data.covers %}
  <a class="cover-card"{% if c.doi %} href="https://doi.org/{{ c.doi }}"{% endif %}>
    <img src="/images/covers/{{ c.image }}" alt="{{ c.title }}" loading="lazy">
    <span class="cover-meta">
      <span class="cover-journal">{{ c.journal }}</span>
      <span class="cover-title">{{ c.title }}</span>
    </span>
  </a>
{% endfor %}
</div>

<style>
.cover-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1.4em;
  margin: 1em 0 2em;
}
.cover-card {
  display: flex;
  flex-direction: column;
  text-decoration: none !important;
  color: inherit;
  border-radius: 10px;
  overflow: hidden;
  background: #fff;
  box-shadow: 0 2px 10px rgba(0,0,0,0.10);
  transition: transform 0.18s ease, box-shadow 0.18s ease;
}
.cover-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 22px rgba(0,0,0,0.18);
}
.cover-card img {
  width: 100%;
  aspect-ratio: 3 / 4;
  object-fit: cover;
  object-position: top center;
  display: block;
  border-bottom: 1px solid #eee;
}
.cover-meta { padding: 0.6em 0.75em 0.8em; }
.cover-journal {
  display: block;
  font-weight: 700;
  font-size: 0.78em;
  color: #006d77;
  margin-bottom: 0.25em;
}
.cover-title {
  display: block;
  font-size: 0.78em;
  line-height: 1.35;
  color: #444;
}
@media (prefers-color-scheme: dark) {
  .cover-card { background: #1e2a2c; box-shadow: 0 2px 10px rgba(0,0,0,0.4); }
  .cover-card img { border-bottom-color: #2c3a3c; }
  .cover-title { color: #cbd5d6; }
}
</style>

## Career

<ol class="career">
{% for job in site.data.career %}
  <li class="career-item{% if job.current %} career-item--current{% endif %}">
    <span class="career-logo">
      <img src="/images/logos/{{ job.logo }}" alt="{{ job.institution }} logo" loading="lazy">
    </span>
    <span class="career-body">
      <span class="career-period">
        {{ job.period }}
        {% if job.current %}<span class="career-dot" aria-hidden="true"></span>{% endif %}
      </span>
      <span class="career-role">{{ job.role }}</span>
      <span class="career-inst">{{ job.institution }}</span>
      <span class="career-loc">{{ job.location }}</span>
    </span>
  </li>
{% endfor %}
</ol>

<style>
.career {
  list-style: none;
  margin: 1.2em 0 2.4em;
  padding: 0 0 0 0.4em;
  position: relative;
}
/* the rail */
.career::before {
  content: "";
  position: absolute;
  left: 41px;
  top: 12px;
  bottom: 12px;
  width: 2px;
  background: linear-gradient(180deg, #006d77 0%, #006d77 55%, rgba(0,109,119,0.15) 100%);
}
.career-item {
  position: relative;
  display: flex;
  align-items: center;
  gap: 1.1em;
  margin: 0 0 1.1em;
  padding: 0;
}
.career-logo {
  flex: 0 0 auto;
  z-index: 1;
  width: 72px;
  height: 72px;
  border-radius: 14px;
  background: #fff;
  border: 1px solid #e3e8e9;
  box-shadow: 0 2px 8px rgba(0,54,61,0.10);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.18s ease, box-shadow 0.18s ease;
}
.career-item:hover .career-logo {
  transform: scale(1.05);
  box-shadow: 0 6px 18px rgba(0,54,61,0.20);
}
.career-logo img {
  max-width: 78%;
  max-height: 78%;
  object-fit: contain;
  display: block;
}
.career-body { display: flex; flex-direction: column; min-width: 0; }
.career-period {
  font-size: 0.72em;
  font-weight: 600;
  letter-spacing: 0.07em;
  text-transform: uppercase;
  color: #006d77;
  margin-bottom: 0.18em;
}
.career-dot {
  display: inline-block;
  width: 7px;
  height: 7px;
  margin-left: 0.45em;
  border-radius: 50%;
  background: #2e9e5b;
  vertical-align: 1px;
  box-shadow: 0 0 0 0 rgba(46,158,91,0.7);
  animation: career-pulse 2.2s infinite;
}
@keyframes career-pulse {
  70% { box-shadow: 0 0 0 7px rgba(46,158,91,0); }
  100% { box-shadow: 0 0 0 0 rgba(46,158,91,0); }
}
@media (prefers-reduced-motion: reduce) {
  .career-dot { animation: none; }
  .career-item:hover .career-logo { transform: none; }
}
.career-role {
  font-weight: 600;
  font-size: 1.02em;
  line-height: 1.25;
}
.career-inst { font-size: 0.95em; line-height: 1.35; }
.career-loc { font-size: 0.82em; color: #6b7778; margin-top: 0.1em; }

@media (max-width: 600px) {
  .career::before { display: none; }
  .career-item { gap: 0.9em; }
  .career-logo { width: 58px; height: 58px; border-radius: 12px; }
}
@media (prefers-color-scheme: dark) {
  .career-logo { border-color: #33474a; box-shadow: 0 2px 8px rgba(0,0,0,0.45); }
  .career-loc { color: #9fb0b2; }
}

/* Research Overview bullet list — classic teal diamond marker with soft halo */
.research-points {
  list-style: none;
  margin: 0.55em 0 1.35em;
  padding-left: 0;
}
.research-points li {
  position: relative;
  padding-left: 1.85em;
  margin-bottom: 0.6em;
  line-height: 1.62;
}
.research-points li::before {
  content: "";
  position: absolute;
  left: 0.18em;
  top: 0.62em;
  width: 0.5em;
  height: 0.5em;
  background: #006d77;
  transform: rotate(45deg);
  border-radius: 1.5px;
  box-shadow: 0 0 0 3px rgba(0,109,119,0.14);
  transition: box-shadow 0.2s ease, background 0.2s ease;
}
.research-points li:hover::before {
  background: #00858f;
  box-shadow: 0 0 0 4px rgba(0,109,119,0.20);
}
@media (prefers-reduced-motion: reduce) {
  .research-points li::before { transition: none; }
}
@media (prefers-color-scheme: dark) {
  .research-points li::before {
    background: #4bb3bd;
    box-shadow: 0 0 0 3px rgba(75,179,189,0.18);
  }
  .research-points li:hover::before {
    background: #6fc9d2;
    box-shadow: 0 0 0 4px rgba(75,179,189,0.26);
  }
}
</style>

## Research Overview

### Quantum Computing for Chemistry

- Implement the Embedded Wavefunction-Sample-based Quantum Diagonalization (EWF-SQD) pipeline on IBM quantum processors, in active collaboration with IBM Research and the Merz group.
- Benchmark target: FLiBe (LiF-BeF2) molten salt clusters relevant to advanced nuclear reactors.
- Extend quantum-centric methods with the Merz group to protein-ligand free energy perturbation and intermolecular interactions.
{: .research-points}

### QM/MM and Enzyme Catalysis

- Developed EnzyDock at Bar-Ilan University (with Prof. Dan T. Major), a CHARMM-based QM/MM docking code for multiple reactive states along enzymatic reaction coordinates.
- Applied to terpene synthases, Diels-Alder reactions, and racemases.
- Established QM region size convergence guidelines for DNA proton transfer (*J. Chem. Theory Comput.* 2018, 2019).
{: .research-points}

### Computational NMR and Metabolomics

- Built QM/ML pipelines for NMR chemical shift and collisional cross section (CCS) prediction at Michigan State University (with Prof. Kenneth M. Merz Jr.) to support metabolite structure elucidation.
- Developed the AutoGraph conformational clustering algorithm.
- Reviewed in *Chemical Reviews* (2025); select papers *Anal. Chem.* 2020, *J. Am. Soc. Mass Spectrom.* 2022, *J. Chem. Inf. Model.* 2023, 2024.
{: .research-points}

### Nanocluster Catalysis

- Applied DFT, ab initio MD, and Coupled-Cluster methods to aluminum nanocluster reactivity during doctoral research at CSIR-National Chemical Laboratory.
- Dinitrogen activation by Si/P-doped clusters and oxidative addition of C-I bonds.
- Site selectivity via conceptual DFT reactivity descriptors.
{: .research-points}

