---
id: node-proj-map-001
title: "Projection Map: Discrete Substrate to Effective Cosmological Quantities"
version: 3.4.0
status: canonical
canonical: true
layer: 06_Projection
upstream:
  - 02_Ontological_Architecture/Emergent_Law_L
  - 05_Formalism/Formalism_F
downstream:
  - 06_Projection/Canonical_Equations
  - 07_Cosmology/Modified_FRW_Dynamics
---

# Projection Map: $D_0, C \to \rho_{\text{eff}}, p_{\text{eff}}, H(z)$

## 1. Operator Mapping Relations
The bridge from discrete operator configuration $(\mathcal{D}_0, \mathcal{C})$ to continuum cosmological variables is defined by:
* **Emergent Structural Energy Density:**
  $$\rho_{\text{SDF}} \equiv \frac{1}{V_{\text{cell}}} \operatorname{Tr}\left( \hat{\rho}_{\text{state}} \hat{H}_{\text{constraint}} \right)$$
* **Emergent Structural Pressure:**
  $$p_{\text{SDF}} \equiv -\frac{1}{3 V_{\text{cell}}} \operatorname{Tr}\left( \hat{\rho}_{\text{state}} \hat{\sigma}_{\text{stress}} \right)$$
* **Expansion Scale:**
  $$H_{\text{eff}} \equiv \frac{c}{3} \nabla_\mu u^\mu$$

## 2. Topological Partition Weighting
$$\sum_i \Omega_i = 1 \implies \Omega_{\text{topo}} = \frac{\rho_{\text{SDF}}}{\rho_{\text{crit}}}$$
In the single-dominance limit ($\Omega_{\text{topo}} \to 1$), $\alpha_{\text{eff}} \to \alpha_0$.

## 3. Invariance and Consistency
* **Dimensional Consistency:** $[\rho_{\text{eff}}] = [p_{\text{eff}}] = M L^{-1} T^{-2}$, $[H] = T^{-1}$.
* **Gauge & Diffeomorphism Invariance:** The projection map preserves local 4-diffeomorphism invariance on the constraint boundary manifold $\mathcal{S}_{\text{adm}}$.
