---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<p class="lead">My work sits at the intersection of quantum computing, quantum chemistry, and biomolecular simulation. The threads below run from current quantum-hardware research back through QM/MM enzymology, computational spectroscopy for metabolomics, and doctoral work on nanocluster catalysis.</p>

## Overview
{: .overview-heading}

<ul class="overview-list">
  <li><a href="#quantum-computing">Quantum Computing for Chemistry</a></li>
  <li><a href="#qm-mm">QM/MM and Enzyme Catalysis</a></li>
  <li><a href="#nmr-ccs">Computational NMR, CCS Prediction, and Metabolite Elucidation</a></li>
  <li><a href="#nanoclusters">Nanocluster Catalysis</a></li>
</ul>

<hr class="section-rule">

## Quantum Computing for Chemistry
{: #quantum-computing}

My current research applies near-term quantum hardware to electronic structure problems in chemistry. I implement the Embedded Wavefunction, Sample-based Quantum Diagonalization (EWF-SQD) pipeline on IBM quantum processors, in active collaboration with IBM Research and the Merz group. The current benchmark target is FLiBe (LiF-BeF2) molten salt clusters relevant to advanced nuclear reactors; results recover relative energies within 0.7 kcal/mol of classical full configuration interaction (FCI), including strongly multi-reference cases. Parallel work extends quantum-centric methods to protein-ligand free energy perturbation (FEP) and intermolecular interactions.

<figure class="research-figure">
  <img src="/images/research/quantumFlibe.jpeg" alt="EWF-SQD workflow for FLiBe molten salt clusters" loading="lazy">
  <figcaption>The EWF-SQD pipeline applied to FLiBe molten salt clusters on IBM quantum hardware.</figcaption>
</figure>

<hr class="section-rule">

## QM/MM and Enzyme Catalysis
{: #qm-mm}

At Bar-Ilan University, with Prof. Dan T. Major, I developed EnzyDock, a CHARMM-based QM/MM docking code for modeling multiple reactive states along enzymatic reaction coordinates. Applications include terpene synthases (selinadiene and limonene synthase), Diels-Alder reactions, and racemases. A separate study on QM region size convergence in DNA proton transfer established practical guidelines for QM/MM system construction (*J. Chem. Theory Comput.* 2018, 2019).

<figure class="research-figure">
  <img src="/images/research/images_large_ct-2017-00964f_0009.jpeg" alt="QM region convergence in QM/MM simulations of proton transfer in DNA" loading="lazy">
  <figcaption>Convergence of energy and free energy profiles with QM region size, proton transfer in DNA base pairs.</figcaption>
</figure>

<hr class="section-rule">

## Computational NMR, CCS Prediction, and Metabolite Elucidation
{: #nmr-ccs}

With Prof. Kenneth M. Merz Jr. at Michigan State University, I built combined quantum mechanics and machine learning (QM/ML) pipelines to predict nuclear magnetic resonance (NMR) chemical shifts and ion mobility collisional cross sections (CCS) for metabolite identification. These predictions support structure elucidation in untargeted metabolomics (*Anal. Chem.* 2020; *J. Am. Soc. Mass Spectrom.* 2022; *J. Chem. Inf. Model.* 2023, 2024). To make conformational analysis reproducible, I also developed AutoGraph, an automated, graph-based clustering algorithm for molecular dynamics ensembles. This work is part of a broader QM/ML metabolomics program reviewed in *Chem. Rev.* 2025, and feeds the POMICS web portal (pomics.org) for metabolite characterization.

<figure class="research-figure">
  <img src="/images/research/ccs.png" alt="QM/ML workflow for collisional cross section prediction" loading="lazy">
  <figcaption>Automated QM/ML workflow predicting metabolite collisional cross sections from SMILES input.</figcaption>
</figure>

<hr class="section-rule">

## Nanocluster Catalysis
{: #nanoclusters}

My doctoral research at CSIR-National Chemical Laboratory, with Prof. Sourav Pal, applied density functional theory (DFT), ab initio molecular dynamics, and coupled-cluster methods to the reactivity of aluminum nanoclusters. Topics included dinitrogen activation by silicon and phosphorus doped clusters, oxidative addition of carbon-iodine bonds, and site selectivity rationalized through conceptual DFT reactivity descriptors.

<figure class="research-figure">
  <img src="/images/research/nanocluster-oxidative-addition.jpg" alt="Free energy profile for oxidative addition of a carbon-iodine bond on an aluminum nanocluster" loading="lazy">
  <figcaption>Oxidative addition of the carbon-iodine bond of an aryl iodide on an aluminum nanocluster: reactant complex, transition state, and product along the computed reaction profile (<em>Nanoscale</em> 2015, 7, 12109).</figcaption>
</figure>

<style>
/* Lead paragraph, set larger than body */
.page__content .lead {
  font-size: 1.18em;
  line-height: 1.6;
  font-weight: 400;
  color: #3d4a4c;
  max-width: 68ch;
  margin-bottom: 1.8em;
}

/* Overview jump list */
.page__content .overview-heading {
  font-size: 1.35em;
  margin-bottom: 0.5em;
}
.page__content .overview-list {
  list-style: none;
  padding: 0;
  margin: 0 0 0.5em;
  border-left: 3px solid #006d77;
}
.page__content .overview-list li { margin: 0; padding: 0; }
.page__content .overview-list a {
  display: block;
  padding: 0.42em 0 0.42em 1em;
  font-weight: 500;
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: padding-left 0.16s ease, background 0.16s ease;
}
.page__content .overview-list a:hover {
  padding-left: 1.4em;
  background: rgba(0,109,119,0.06);
  text-decoration: none;
}

/* Hairline rule between stacked sections */
.page__content .section-rule {
  border: 0;
  border-top: 1px solid #e0e6e7;
  margin: 3em 0 2.4em;
}

/* Full-width figures below the prose, not floated */
.research-figure {
  margin: 1.8em 0 0.5em;
  max-width: 100%;
}
.research-figure img {
  width: 100%;
  max-width: 760px;
  height: auto;
  display: block;
  border-radius: 8px;
  border: 1px solid #e6ebec;
}
.research-figure figcaption {
  margin-top: 0.6em;
  font-size: 0.82em;
  line-height: 1.45;
  color: #6b7778;
  max-width: 760px;
}

/* Give each anchored section clearance from the sticky masthead */
.page__content h2[id] { scroll-margin-top: 5rem; }

@media (prefers-color-scheme: dark) {
  .page__content .lead { color: #c3d0d2; }
  .page__content .section-rule { border-top-color: #2c3a3c; }
  .research-figure img { border-color: #2c3a3c; }
  .research-figure figcaption { color: #9fb0b2; }
  .page__content .overview-list a:hover { background: rgba(0,109,119,0.18); }
}
</style>
