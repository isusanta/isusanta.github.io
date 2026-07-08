---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="news-hero">
  <span class="news-badge">★ In the News · July 2026</span>
  <h2 class="news-headline">First-Ever Quantum-Computer Calculations of Fusion Reactor Materials</h2>
  <p class="news-text">Our team at Cleveland Clinic, Oak Ridge National Laboratory, and IBM reported the first known quantum-computer calculations of fusion blanket molten salts (FLiBe), a key step toward tritium extraction for fusion energy. I am first author on the study.</p>
  <div class="news-links">
    <a class="news-btn" href="https://newsroom.ibm.com/2026-07-06-oak-ridge-national-lab,-cleveland-clinic,-and-ibm-achieve-first-known-computations-of-fusion-materials-on-a-quantum-computer">IBM Newsroom →</a>
    <a class="news-btn" href="https://www.ornl.gov/news/oak-ridge-national-lab-cleveland-clinic-and-ibm-achieve-first-known-computations-fusion">Oak Ridge National Lab →</a>
    <a class="news-btn news-btn-solid" href="https://doi.org/10.48550/arXiv.2606.30402">Read the Preprint →</a>
  </div>
</div>

<style>
.news-hero {
  background: linear-gradient(135deg, #006d77 0%, #00363d 100%);
  color: #fff;
  border-radius: 14px;
  padding: 1.6em 1.8em 1.7em;
  margin: 1.2em 0 2em;
  box-shadow: 0 10px 30px rgba(0,54,61,0.28);
}
.news-badge {
  display: inline-block;
  background: rgba(255,255,255,0.16);
  color: #fff;
  font-size: 0.72em;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  padding: 0.35em 0.8em;
  border-radius: 999px;
  margin-bottom: 0.7em;
}
.news-headline {
  color: #fff !important;
  margin: 0.1em 0 0.4em;
  font-size: 1.5em;
  line-height: 1.2;
  border: none;
}
.news-text {
  color: #e6f2f3;
  font-size: 0.95em;
  line-height: 1.55;
  margin: 0 0 1.1em;
  max-width: 60ch;
}
.news-links { display: flex; flex-wrap: wrap; gap: 0.7em; }
.news-btn {
  display: inline-block;
  text-decoration: none !important;
  font-size: 0.85em;
  font-weight: 600;
  color: #fff !important;
  padding: 0.55em 1.1em;
  border: 1px solid rgba(255,255,255,0.5);
  border-radius: 8px;
  transition: background 0.16s ease, transform 0.16s ease;
}
.news-btn:hover { background: rgba(255,255,255,0.15); transform: translateY(-2px); }
.news-btn-solid { background: #fff; color: #006d77 !important; border-color: #fff; }
.news-btn-solid:hover { background: #e6f2f3; }
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

| Period | Position | Institution |
|---|---|---|
| Oct 2023 – present | Research Associate | Cleveland Clinic, Cleveland, OH, USA |
| Apr 2019 – Oct 2023 | Postdoctoral Fellow | Michigan State University, East Lansing, MI, USA |
| Aug 2015 – Apr 2019 | Postdoctoral Research Fellow | Bar-Ilan University, Ramat-Gan, Israel |
| Jan 2010 – Aug 2015 | Doctoral Researcher | CSIR-NCL / AcSIR, Pune, India |

## Research Overview

### Quantum Computing for Chemistry

Current work focuses on near-term quantum hardware for electronic structure. I implement the Embedded Wavefunction-Sample-based Quantum Diagonalization (EWF-SQD) pipeline on IBM quantum processors, in active collaboration with IBM Research and the Merz group. Current benchmark target: FLiBe (LiF-BeF2) molten salt clusters relevant to advanced nuclear reactors. Results demonstrate recovery of relative energies within 0.7 kcal/mol of classical FCI, including strongly multi-reference cases. Parallel work with the Merz group extends quantum-centric methods to protein-ligand free energy perturbation and intermolecular interactions.

### QM/MM and Enzyme Catalysis

At Bar-Ilan University (with Prof. Dan T. Major), I developed EnzyDock — a CHARMM-based QM/MM docking code for studying multiple reactive states along enzymatic reaction coordinates, applied to terpene synthases, Diels-Alder reactions, and racemases. Separate work on QM region size convergence in DNA proton transfer established practical guidelines for QM/MM system construction (*J. Chem. Theory Comput.* 2018, 2019).

### Computational NMR and Metabolomics

At Michigan State University (with Prof. Kenneth M. Merz Jr.), I built QM/ML pipelines for NMR chemical shift and collisional cross section (CCS) prediction to support metabolite structure elucidation, along with the AutoGraph conformational clustering algorithm. This work is reviewed in *Chemical Reviews* (2025). Select papers: *Anal. Chem.* 2020, *J. Am. Soc. Mass Spectrom.* 2022, *J. Chem. Inf. Model.* 2023, 2024.

### Nanocluster Catalysis

Doctoral research at CSIR-National Chemical Laboratory applied DFT, ab initio MD, and Coupled-Cluster methods to aluminum nanocluster reactivity: dinitrogen activation by Si/P-doped clusters, oxidative addition of C-I bonds, and site selectivity via conceptual DFT reactivity descriptors.

