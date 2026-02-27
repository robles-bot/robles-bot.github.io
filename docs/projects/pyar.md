# Particle Physics Data Analysis with Python

**Program:** PYAR/CrEST Outreach
**Institution:** UC Santa Cruz
**Role:** Curriculum Developer & Instructor

[View on GitHub](https://github.com/robles-bot/physics-195-pyar){ .md-button }

---

## Overview

A series of Jupyter notebooks designed to introduce high school and early undergraduate students to particle physics data analysis. The curriculum guides students from Python basics through analyzing real CERN Open Data to discover the Z boson.

Developed as part of the **PYAR (Physics Young Achievers in Research)** and **CrEST (Creating Equity in STEM)** programs at UC Santa Cruz, which aim to increase diversity and access to physics research for underrepresented students.

## Curriculum

| Notebook | Topics |
|----------|--------|
| 1. Python Intro | Variables, lists, loops, functions, modules |
| 2. Plotting | NumPy, Matplotlib, histograms, scatter plots |
| 3. Coordinate Systems | Cartesian, polar, spherical, cylindrical transforms |
| 4. Particle Physics Primer | Four-vectors, collider coordinates, mass reconstruction |
| 5. Data Extraction | Pandas, CSV parsing, CERN Open Data |
| 6. Invariant Mass Plotting | Full analysis pipeline, Z boson identification |

## Physics Concepts

### Collider Coordinates

Students learn the coordinate system used at particle colliders:

- **Transverse momentum** ($p_T$): Momentum perpendicular to beam
- **Pseudorapidity** ($\eta$): Related to polar angle, $\eta = -\ln\tan(\theta/2)$
- **Azimuthal angle** ($\phi$): Angle in the transverse plane

### Invariant Mass

The key analysis technique - reconstructing parent particle mass from decay products:

$$
m = \sqrt{(E_1 + E_2)^2 - |\vec{p}_1 + \vec{p}_2|^2}
$$

Students apply this to identify the Z boson (~91 GeV) from its decays to lepton pairs.

## Data

Real collision data from the [CERN Open Data Portal](https://opendata.cern.ch/):

- `Zee.csv` - Z → e⁺e⁻ (electron-positron pairs)
- `Zmumu.csv` - Z → μ⁺μ⁻ (muon-antimuon pairs)

## Acknowledgments

This curriculum was developed through the **PYAR** and **CrEST** programs at UC Santa Cruz. These programs provide research opportunities and mentorship to students from underrepresented backgrounds in physics and STEM fields.

- [PYAR Program](https://physics.ucsc.edu/outreach/pyar/)
- [CrEST Program](https://crest.ucsc.edu/)
