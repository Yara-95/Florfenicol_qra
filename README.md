# Probabilistic Quantitative Risk Assessment (QRA) of Florfenicol in Nile Tilapia Recirculating Aquaculture Systems (RAS)

[![One Health Framework](https://img.shields.io/badge/One%20Health-QRA%20%26%20AMR-blue)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)

## Overview
This repository contains the complete codebase, data pipelines, pharmacokinetic-environmental models, and quality assurance checks for the manuscript:

> **"Florfenicol in Nile tilapia recirculating aquaculture: a probabilistic risk assessment of withdrawal, dietary exposure and effluent load"**

The study bridges a critical gap in aquaculture research by integrating **food safety (fillet withdrawal times and ADI shares)** and **environmental stewardship (antimicrobial resistance selection and effluent load optimization)** into a single mass-conserving quantitative risk assessment (QRA) framework under a **One Health** approach.

---

## Key Model Features
1. **Bayesian Pharmacokinetic (PK) Modeling:** Calibrated using MCMC (Adaptive Metropolis sampling) against published Nile tilapia muscle-skin florfenicol amine (FFA) and serum datasets.
2. **Thermal & Allometric Scaling:** Incorporates temperature dependence ($Q_{10}$) and body-mass exponents ($b$) to simulate withdrawal dynamics across variable commercial conditions (25–30 °C, 100–500 g fish).
3. **RAS Mass-Balance Environmental Fate:** Couples fish excretion, unabsorbed feed/faeces, and uneaten feed dynamics to water exchange rates ($q_{ex}$), biofilter sorption ($k_{sed}$), and degradation ($k_{deg}$).
4. **AMR Risk Characterization:** Evaluates in-system Predicted Environmental Concentrations (PEC) against the resistance-selection Predicted No-Effect Concentration ($\text{PNEC}_{res} = 2\ \mu\text{g/L}$).
5. **Robust Quality Assurance:** Includes independent automated verification scripts (`qa_checks.py`) for mass conservation, analytical solutions, and sensitivity analyses.

---

## Repository Structure
```text
├── florfenicol_qra_v3.ipynb       # Main Jupyter Notebook (Model, MCMC calibration, scenarios, & plots)
├── qa_checks.py                   # Automated QA script for reproducibility and stress tests
├── qa_checks_results.txt          # Output logs from QA verification checks
├── manuscript.docx                # Full manuscript draft (npj Science of Food format)
└── README.md                      # Project documentation
