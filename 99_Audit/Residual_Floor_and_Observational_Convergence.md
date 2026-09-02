---
id: sdf-audit-residual-floor-001
title: Residual Floor and Observational Convergence
version: 3.4.0
last_validated: 2026-09-01
status: canonical
canonical: true
layer: 99_Audit
depends_on:
  - 04_Dynamics/Effective_Fluid_Projection
  - 99_Audit/Null_Models_M0
  - 99_Audit/Closure_Stability_Criteria
downstream: []
---

# Residual Floor and Observational Convergence

## 1. Context and Scope
This node formalizes the falsifiability boundary and the residual information floor ($\mathcal{R}_{\text{floor}}$) of the SDF emergent framework. It establishes the limits where microscopic or condensed-matter transitions cease to provide discriminating macroscopic observational signatures.

## 2. Residual Floor & Blind Observable Definition
The observational residual metric is defined against the unconstrained baseline $M_0$:
$$\mathcal{R}_{\text{floor}} \equiv \min_{\theta \in \mathcal{B}} \chi^2_{\text{SDF}}(\theta) - \chi^2_{\text{best}}(M_0)$$

### 2.1 EMS Invariance and the Observational Blindness Limit
Electron Momentum Spectroscopy (EMS) cross-sections $\sigma_{\text{EMS}}$ in binary $(e, 2e)$ regimes map directly to the spherically averaged Dyson orbital momentum density:
$$\sigma_{\text{EMS}}(\mathbf{p}) \propto \int |\langle \mathbf{p} \Psi^{(N-1)} | \Psi^{(N)} \rangle|^2 d\Omega \approx \int |\phi_j(\mathbf{p})|^2 d\Omega$$

As established empirically in the gas-to-liquid phase transition of water (Hafez, Hierro et al., 2007):
$$\left\| \frac{\partial \rho_{\text{orb}}(\mathbf{p})}{\partial \omega_F} \right\| \approx 0$$
Where $\omega_F$ is the Frenkel shear-wave frequency gap. Therefore, binary single-particle momentum projections represent a **Blind Observable** ($\mathcal{O}_{\text{blind}}$) that cannot discriminate shear-mode emergence.

**Falsifiability Gate:**
$$\Delta \text{BIC}(M_3, M_0) \ge 10 \quad (\text{Strong empirical preference for } M_3)$$
If $\mathcal{R}_{\text{floor}} \ge 0$ and $\Delta \text{BIC} < 10$, the emergent sector is classified as *non-falsified-but-uninformative*.

## 3. Admissible Observational Probes
| Probe | Observable | Theoretical Boundary / Target |
| :--- | :--- | :--- |
| **CMB (Planck-class)** | $H_0, \Omega_b, \ell_A$ | $\rho_{\text{SDF}}$ at recombination epoch |
| **Baryon Acoustic Osc. (BAO)** | $D_V(z)/r_d$ | $H_{\text{eff}}(z)$ evolution |
| **Type Ia Supernovae** | $\mu(z)$ Distance Modulus | $\int [1+w_{\text{eff}}(z)] d\ln(1+z)$ |
| **Growth of Structure** | $f\sigma_8(z)$ | Sign and scale of $\Gamma_{\text{coupling}}$ |
| **EMS High-Momentum Tail** | $\rho(p > 1.5\,\text{a.u.})$ | Intramolecular Identity Invariant ($C_{\text{id}}$) |

## 4. Multi-Index Convergence Criteria
A cosmological trajectory is canonically valid if and only if all four conditions hold across $z \in [0, 1100]$:
1. **Spectral Stability:** $\max \operatorname{Re}(\operatorname{Spec}(J)) \le 0$
2. **Equation of State Bound:** $-1 \le w_{\text{eff}}(\alpha_{\text{eff}}) \le 1$
3. **Statistical Information Gate:** $\Delta \text{BIC}(M_3, M_0) \ge 10$
4. **Independent Residual Closure:** $\mathcal{R}_{\text{floor}} < 0$ at $2\sigma$ confidence level.

## 5. Audit Vector Reporting Contract
Every audit run must yield the canonical 5-tuple:
$$\mathfrak{A} = \left( \mathcal{R}_{\text{floor}},\ \Delta\text{BIC},\ \max\operatorname{Re}(\operatorname{Spec}(J)),\ \min_z w_{\text{eff}},\ \max_z w_{\text{eff}} \right)$$
