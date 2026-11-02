# Probabilistic Quantitative Risk Assessment: Florfenicol in Nile Tilapia (RAS)

[![One Health Framework](https://img.shields.io/badge/One%20Health-QRA%20%26%20AMR-blue)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)

## Overview
This repository contains the complete codebase, data pipelines, pharmacokinetic-environmental models, and integrated quality assurance checks for the quantitative risk assessment (QRA) of florfenicol in Nile Tilapia recirculating aquaculture systems (RAS).

The study bridges a critical gap in aquaculture research by integrating **food safety (fillet withdrawal times and ADI shares)** and **environmental stewardship (antimicrobial resistance selection and effluent load optimization)** into a single mass-conserving QRA framework under a **One Health** approach.

---

## Key Model Features
1. **Pharmacokinetic (PK) & Environmental Modeling:** Combines multi-compartment disposition kinetics with RAS water mass-balance, tracking fish compartments, water, sludge, and discharge.
2. **Thermal & Allometric Scaling:** Incorporates temperature dependence ($Q_{10}$) and body-mass scaling to simulate withdrawal dynamics across variable commercial conditions (25–30 °C, 100–500 g fish).
3. **Dynamic AMR & Climate Stress:** Simulates resistance gene selection ($ARGs$) dynamics in biofilters and evaluates fluctuating thermal regimes (heatwaves).
4. **Global Sensitivity Analysis (Sobol Indices):** Evaluates parameter uncertainty and identifies primary drivers of environmental emissions.
5. **Eco-Economic Optimization:** Balances operational water exchange costs, effluent treatment efficiency, and environmental emission penalties.
6. **Inline Automated QA Checks:** Features built-in verification tests for mass conservation, temperature ratios, and environmental sink stress-tests.

---

## Repository Structure
```text
├── florfenicol_qra_ras.ipynb       # Main unified Jupyter Notebook (Model, Sobol GSA, Optimization, & QA)
└── README.md                      # Project documentation
