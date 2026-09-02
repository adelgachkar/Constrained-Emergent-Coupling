---
id: sdf-fnd-aa-001
title: Admissibility Principle (AA)
version: 3.4.0
status: active
canonical: true
last_validated: 2026-08-31
domain: Quantum ML | Many-Body Topology
upstream: sdf-master-map-001
downstream:
  - 01_Foundation/Identity_Constraint_Cid
  - 01_Foundation/Bounded_Substrate_S
  - 01_Foundation/Relational_Regime_R
tags:
  - admissibility
  - projection-operator
  - foundational-axiom
---

# Admissibility Principle ($\mathrm{AA}$)

## 1. Operational Definition

The Admissibility Principle dictates that physical/informational states are not globally unrestricted; rather, raw degrees of freedom are filtered through boundary and topological projection operators:

$$\Pi_{C_{\mathrm{adm}}}: \mathcal{H}_{\mathrm{raw}} \longrightarrow \mathcal{H}_{\mathrm{adm}} \subseteq \mathcal{H}_{\mathrm{raw}}$$

where $\Pi_{C_{\mathrm{adm}}}$ satisfies idempotency and self-adjointness:
$$\Pi_{C_{\mathrm{adm}}}^2 = \Pi_{C_{\mathrm{adm}}}, \quad \Pi_{C_{\mathrm{adm}}}^\dagger = \Pi_{C_{\mathrm{adm}}}$$

## 2. Core Axioms

1. **Local Admissibility Axiom:** No relational interaction can be established across states $|\psi\rangle$ for which $\langle \psi | \Pi_{C_{\mathrm{adm}}} | \psi \rangle = 0$.
2. **Norm Preservation:** For any admissible state $|\phi\rangle \in \mathcal{H}_{\mathrm{adm}}$, $\|\Pi_{C_{\mathrm{adm}}} \phi\| = \|\phi\|$.
3. **No Dynamic Imposition:** $\Pi_{C_{\mathrm{adm}}}$ acts purely as a geometric filter (boundary condition) and does not introduce exogenous dynamical trajectories.
