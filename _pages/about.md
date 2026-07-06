---
permalink: /
title: "Susanta Das, Ph.D."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

Research Associate at Cleveland Clinic developing quantum algorithms, QM/MM methods, and QM/ML workflows for problems in chemical energetics, enzyme catalysis, and metabolomics.

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

## Quantum Computing for Chemistry

Current work focuses on near-term quantum hardware for electronic structure. I implement the Embedded Wavefunction-Sample-based Quantum Diagonalization (EWF-SQD) pipeline on IBM quantum processors, in active collaboration with IBM Research and the Merz group. Current benchmark target: FLiBe (LiF-BeF2) molten salt clusters relevant to advanced nuclear reactors. Results demonstrate recovery of relative energies within 0.7 kcal/mol of classical FCI, including strongly multi-reference cases. Parallel work with the Merz group extends quantum-centric methods to protein-ligand free energy perturbation and intermolecular interactions.

## QM/MM and Enzyme Catalysis

At Bar-Ilan University (with Prof. Dan T. Major), I developed EnzyDock — a CHARMM-based QM/MM docking code for studying multiple reactive states along enzymatic reaction coordinates, applied to terpene synthases, Diels-Alder reactions, and racemases. Separate work on QM region size convergence in DNA proton transfer established practical guidelines for QM/MM system construction (*J. Chem. Theory Comput.* 2018, 2019).

## Computational NMR and Metabolomics

At Michigan State University (with Prof. Kenneth M. Merz Jr.), I built QM/ML pipelines for NMR chemical shift and collisional cross section (CCS) prediction to support metabolite structure elucidation, along with the AutoGraph conformational clustering algorithm. This work is reviewed in *Chemical Reviews* (2025). Select papers: *Anal. Chem.* 2020, *J. Am. Soc. Mass Spectrom.* 2022, *J. Chem. Inf. Model.* 2023, 2024.

## Nanocluster Catalysis

Doctoral research at CSIR-National Chemical Laboratory applied DFT, ab initio MD, and Coupled-Cluster methods to aluminum nanocluster reactivity: dinitrogen activation by Si/P-doped clusters, oxidative addition of C-I bonds, and site selectivity via conceptual DFT reactivity descriptors.

