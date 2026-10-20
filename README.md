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

**multi_species_systems_with_X**
Conducts equilibrium abundance sensitivity analysis for multi-species communities, reproducing Fig.6 in the Appendix.

## Usage

1. Modify model parameters as needed: delay ranges, self‑regulation strength s, interaction magnitude, connectance C, species number S, equilibrium abundance.
2. Run the script to solve delay‑differential equations or compute leading eigenvalues.
3. Output stability phase diagrams or population time‑series figures.

## Model setup

We study generalized Lotka‑Volterra systems incorporating **self‑regulation delay (tau_s)** and **interspecific interaction delay (tau_c)**.

- X_i(t): Population abundance of species i
- tau_s: Self‑regulation delay, accounts for intraspecific time lags such as maturation, reproduction and density‑dependent feedback. Population growth depends on its own past abundance.
- tau_c: Interspecific interaction delay, describes time lags of species interaction effects including predation response, competition and mutualism. Species respond to other species’ past population states.
- s: Magnitude of intraspecific self‑regulation.
- A_ij: Interaction matrix. Different sign combinations define community types: predator‑prey (+/‑), competition (‑/‑), mutualism (+/+), and random mixed interactions.
- r_i: Intrinsic growth rate, solved self‑consistently to guarantee feasible co‑existence equilibrium.

System stability is quantified by the real part of the leading eigenvalue obtained from linearized delay‑differential equations:

- Leading eigenvalue real part < 0: the coexistence equilibrium is locally stable
- Leading eigenvalue real part > 0: the coexistence equilibrium is unstable
- Leading eigenvalue real part = 0: critical Hopf bifurcation boundary

## Notes on reproduction

- Intrinsic growth rates r_i are solved self‑consistently given the co‑existence equilibrium condition.
- Multi‑species results are averaged over multiple random realizations to reduce sampling noise.
