---
id: sdf-proj-canon-eq-001
title: Canonical Projection Equations
version: 3.4.0
status: canonical
canonical: true
layer: 06_Projection
depends_on:
  - 05_Formalism/Formalism_F
downstream:
  - 04_Dynamics/Effective_Fluid_Projection
  - 07_Cosmology/Modified_FRW_Dynamics
---

# Canonical Equations

## 1. Canonical State Vector
The autonomous dynamical vector of the projected cosmos:
$$\mathbf{X} \equiv \begin{pmatrix} \rho_{\text{SDF}} \\ H_{\text{eff}} \\ \alpha_{\text{eff}} \end{pmatrix} \in \mathbb{R}^+ \times \mathbb{R} \times [0, 1]$$

## 2. Canonical Dynamical System
1. **Kinematic Constraint:**
   $$H_{\text{eff}} \equiv \frac{\dot{a}_{\text{eff}}}{a_{\text{eff}}} = \frac{c}{3} \nabla_\mu u^\mu$$
2. **Geometric Constraint (Friedmann Metric Anchor):**
   $$H_{\text{eff}}^2 = \frac{8\pi G}{3} \left( \rho_m + \rho_{\text{SDF}} \right) - \frac{k c^2}{a_{\text{eff}}^2}$$
3. **Dynamical Generator (Raychaudhuri):**
   $$\dot{H}_{\text{eff}} = -4\pi G \left( \rho_{\text{tot}} + p_{\text{tot}}/c^2 \right) + \frac{k c^2}{a_{\text{eff}}^2}$$
4. **Relational Continuity:**
   $$\dot{\rho}_{\text{SDF}} = -3 H_{\text{eff}} [1 + w_{\text{eff}}(\alpha_{\text{eff}})] \rho_{\text{SDF}} + \Gamma_{\text{coupling}}(\alpha_{\text{eff}}, H_{\text{eff}})$$
