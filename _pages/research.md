---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

My work sits at the intersection of quantum computing, quantum chemistry, and biomolecular simulation. The threads below run from current quantum-hardware research back through QM/MM enzymology, computational spectroscopy for metabolomics, and doctoral work on nanocluster catalysis.

## Quantum Computing for Chemistry

![EWF-SQD workflow for FLiBe molten salt clusters](/images/research/quantumFlibe.jpeg){: .align-right style="width:320px"}

My current research applies near-term quantum hardware to electronic structure problems in chemistry. I implement the Embedded Wavefunction, Sample-based Quantum Diagonalization (EWF-SQD) pipeline on IBM quantum processors, in active collaboration with IBM Research and the Merz group. The current benchmark target is FLiBe (LiF-BeF2) molten salt clusters relevant to advanced nuclear reactors; results recover relative energies within 0.7 kcal/mol of classical full configuration interaction (FCI), including strongly multi-reference cases. Parallel work extends quantum-centric methods to protein-ligand free energy perturbation (FEP) and intermolecular interactions.

## QM/MM and Enzyme Catalysis

![EnzyDock QM/MM docking and QM region convergence](/images/research/qmmm.png){: .align-left style="width:300px"}

At Bar-Ilan University, with Prof. Dan T. Major, I developed EnzyDock, a CHARMM-based QM/MM docking code for modeling multiple reactive states along enzymatic reaction coordinates. Applications include terpene synthases (selinadiene and limonene synthase), Diels-Alder reactions, and racemases. A separate study on QM region size convergence in DNA proton transfer established practical guidelines for QM/MM system construction (*J. Chem. Theory Comput.* 2018, 2019).

## Computational NMR and CCS Prediction

![QM/ML workflow for collisional cross section prediction](/images/research/ccs.png){: .align-right style="width:340px"}

With Prof. Kenneth M. Merz Jr. at Michigan State University, I built combined quantum mechanics and machine learning (QM/ML) pipelines to predict nuclear magnetic resonance (NMR) chemical shifts and ion mobility collisional cross sections (CCS) for metabolite identification. These predictions support structure elucidation in untargeted metabolomics (*Anal. Chem.* 2020; *J. Am. Soc. Mass Spectrom.* 2022; *J. Chem. Inf. Model.* 2023, 2024).

## Conformational Clustering and Metabolite Elucidation

![AutoGraph conformational clustering](/images/research/metabolomics.png){: .align-left style="width:300px"}

To make conformational analysis reproducible, I developed AutoGraph, an automated, graph-based clustering algorithm for molecular dynamics ensembles. This work is part of a broader QM/ML metabolomics program reviewed in *Chem. Rev.* 2025, and feeds the POMICS web portal (pomics.org) for metabolite characterization.

## Nanocluster Catalysis

My doctoral research at CSIR-National Chemical Laboratory, with Prof. Sourav Pal, applied density functional theory (DFT), ab initio molecular dynamics, and coupled-cluster methods to the reactivity of aluminum nanoclusters. Topics included dinitrogen activation by silicon and phosphorus doped clusters, oxidative addition of carbon-iodine bonds, and site selectivity rationalized through conceptual DFT reactivity descriptors.
