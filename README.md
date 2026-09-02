# Constrained Emergent Coupling (CEC)

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.22184632-blue)
![Release](https://img.shields.io/badge/Release-v3.4.2-green)

**Constrained Emergent Coupling (CEC)** is the reference implementation of the
*Structural Delimitation Framework (SDF)* — a rigorously delimited, ghost-free
cosmological framework in which dark-sector dynamics emerge from a constrained,
bounded substrate $\mathcal{S}$ under topological admissibility rules.

---

## 📡 Executive Summary

CEC formalizes the emergence of effective cosmological behavior from a
micro-configured substrate via a canonical, non-reducible sequence. The
framework is **pre-Friedmannian**: the FRW sector is not assumed, but projected
from constrained substrate observables through a delimited mapping
$\mathcal{M}$, with all couplings subject to ghost-free and kinetic-stability
criteria.

$$
\mathcal{G} \xrightarrow{\quad\mathrm{Cid}\quad} \mathcal{S} \longrightarrow \mathcal{R} \longrightarrow \mathcal{M} \longrightarrow \mathcal{L} \longrightarrow \mathcal{F}
$$

---

## 🔬 Core Theoretical Pillars

- **Topological Admissibility** — $\mathcal{C}_{\mathrm{id}}$ and $\hat{\mathcal{C}}_{\mathrm{top}}$: Enforce strict mathematical admissibility criteria on the substrate $\mathcal{S}$, eliminating non-physical (ghost) degrees of freedom.

- **Pre-Friedmannian Projection** — Maps micro-configurations $\mathcal{D}_{\mathcal{O}}, \mathcal{C}$ directly into macro-scale hydrodynamic observables $\rho_{\mathrm{tot}}, p_{\mathrm{tot}}, H$.

- **Lyapunov-Stable Interaction Vectors** — Implements non-perturbative energy–momentum exchange vectors $Q^{\mu}$ that satisfy dynamic closure and kinetic stability $\mathrm{Re}(\lambda_i) \leq 0$.

- **Audit & Identifiability Pipeline** ($\mathcal{M}_0$) — Integrates Fisher Information Matrix (FIM) criteria and residual floor bounds $\Delta\mathrm{BIC}$ for observational falsifiability.

---

## 🗂 Canonical Repository Structure

The following structure represents the complete, delimited modular domains of
the v3.4.2 release:

- **`00_Map/`** — [SDF Master Map](00_Map/SDF_Master_Map.md)
- **`01_Foundation/`** — Substrate $\mathcal{S}$, Admissibility Principle (AA), Identity Constraint $\mathcal{C}_{\mathrm{id}}$, Relational Regime $\mathcal{R}$, Geometric Boundary Conditions
- **`02_Ontological_Architecture/`** — Emergent Law $\mathcal{L}$
- **`04_Dynamics/`** — Effective Fluid Projection
- **`05_Formalism/`** — Formalism $\mathcal{F}$, Effective Action
- **`06_Projection/`** — Canonical Equations, Projection Map $\mathcal{D}_{\mathcal{O}},\mathcal{C} \to \rho, p, H$
- **`07_Cosmology/`** — Modified FRW Dynamics, Coupling Functional Forms
- **`99_Audit/`** — Null Models ($\mathcal{M}_0$), Closure & Stability Criteria, Parameter Identifiability, Residual Floor & Observational Convergence

---

## 📜 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE)
file for details. Copyright (c) 2025 Adel Gachkar.

---

## 📚 Citation

If you use this framework, please cite the Zenodo record:
```bibtex
@misc{gachkar2025cec,
  author       = {Gachkar, Adel},
  title        = {Constrained Emergent Coupling: Structural Delimitation Framework (SDF) v3.4.2},
  year         = {2025},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.22184632},
  url          = {https://doi.org/10.5281/zenodo.22184632}
}
