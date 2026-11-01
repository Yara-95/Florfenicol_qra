Probabilistic Quantitative Risk Assessment (QRA) of Florfenicol in Nile Tilapia RAS

Overview

This repository contains the probabilistic One Health risk assessment framework for florfenicol administration in Nile tilapia (Oreochromis niloticus) reared in Recirculating Aquaculture Systems (RAS). The model unifies food safety endpoints (tissue depletion, withdrawal periods, and acceptable daily intake) with environmental stewardship and resistance selection dynamics.

Manuscript Title: Florfenicol in Nile tilapia recirculating aquaculture: a probabilistic risk assessment of withdrawal, dietary exposure and effluent load

Key Features

Integrated PK & Mass-Balance Model: Links dynamic fish pharmacokinetic compartments (gut, central, muscle) directly to system water, biofilter sorption, and effluent discharges.

Biofilter AMR Dynamics: Simulates resistance selection pressure versus fitness cost in active biofilters under varying residual exposure.

Thermal Regime Modeling: Incorporates $Q_{10}$ temperature scaling to evaluate operational scenarios, thermal variations, and climate-driven heatwave surges.

Global Sensitivity Analysis (Sobol Indices): Quantifies variance-based first-order ($S_1$) parameter sensitivities governing environmental discharge loads.

Eco-Economic Optimization: Evaluates optimal daily water exchange rates ($q_{ex}$) paired with effluent treatment efficiency ($\eta$) to minimize operational cost and active drug emissions.

Automated Quality Assurance: Includes inline checks for analytical correctness, experimental anchor validation, and environmental sink stress testing.

Repository Structure

├── florfenicol_qra_ras.ipynb       # Complete Jupyter Notebook (Model, QA Checks, Sobol GSA, & Optimization)
├── scenario_summary.csv           # Model outputs across temperature and water exchange scenarios
├── sensitivity_prcc.csv           # Partial rank correlation coefficients for key parameters
└── README.md                      # Project documentation


Quick Start & Dependencies

Prerequisites

Ensure Python 3.8+ is installed along with the required numerical and analytical packages:

pip install numpy pandas scipy matplotlib


Running the Notebook

Open and execute florfenicol_qra_ras.ipynb using Jupyter Notebook or Google Colab:

jupyter notebook florfenicol_qra_ras.ipynb


The notebook executes sequentially:

Parameter sampling via Latin Hypercube Sampling (LHS).

Dynamic ordinary differential equation (ODE) mass-balance simulations.

Inline Quality Assurance (QA) and identifiability checks.

Sobol global sensitivity analysis.

Eco-economic optimization using L-BFGS-B minimization.

Main Conclusions

Food Safety: The 99th-percentile fillet tissue depletion falls reliably below the maximum residue limit ($\text{MRL} = 1.0\ \mu\text{g/g}$) well within standard label withdrawal periods (median $t_{99}$ ranges from 3.0 to 11.9 days).

The Exchange Paradox: Increasing daily water exchange lowers in-system water concentrations but proportionally escalates total discharged active drug load into receiving aquatic ecosystems.

AMR Risk & Mitigation: System water concentrations exceed resistance selection thresholds ($\text{PNEC}_{res} = 1.3\ \mu\text{g/L}$) during therapeutic courses; high-efficiency effluent treatment ($\ge 90\%$) serves as the primary environmental control measure.

License

This project is licensed under the MIT License - see the LICENSE file for details.
