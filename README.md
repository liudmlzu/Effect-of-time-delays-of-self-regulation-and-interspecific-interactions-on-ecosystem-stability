## Effect-of-time-delays-of-self-regulation-and-interspecific-interactions-on-ecosystem-stability

This project contains MATLAB scripts to simulate delayed generalized Lotka–Volterra ecological dynamics. The scripts evaluate system stability under two distinct time delays and generate phase diagrams and population time-series plots.

## Scripts

**function delayed_LV_2species_perturbation**
Simulates perturbed population time series for two-species delayed LV models, used to validate phase boundaries and reproduce Fig.3.

**function phase_diagram_delayed_LV_2species**
Computes stability phase diagrams for two-species communities, corresponding to Fig.2.

**multi-species_systems_with_S**
Explores how species richness S shapes stability in random multi-species communities.

**multi-species_systems_with_sigma**
Explores how interaction strength \(\sigma\) shapes stability in random multi-species communities. The above two scripts together produce Fig.5.

**multi_species_systems**
Implements the construction of random multi-species interaction networks and the core routine for stability phase diagrams.

## Usage

1. Open the MATLAB scripts.
2. Adjust parameters such as delay ranges, interaction strength, and species number.
3. Run the scripts to compute stability and generate figures.
