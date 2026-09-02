---
title: Closure Stability Criteria
id: closure-stability-criteria
version: 3.4.2
status: audit
layer: 99_Audit
depends_on:
  - "06_Projection/Canonical_Equations.md"
  - "07_Cosmology/Modified_FRW_Dynamics.md"
  - "06_Projection/Effective_Fluid_Projection.md"
last_validated: 2026-09-02
---

# Closure Stability Criteria

## 1. Scope

This node defines technical criteria for evaluating the stability and admissibility of a reduced dynamical closure.

The analysis is restricted to:

- local fixed-point stability;
- linearized dynamics;
- Lyapunov stability;
- closure consistency;
- numerical validation requirements.

No stability claim is made unless the state vector, evolution equations, parameter domain, and perturbation convention are explicitly specified.

---

## 2. State 2. State-Space Representation

Let the reduced state vector be

$$
\mathbf)
=
\begin{pmatrix}
X_1(t) \\
X_2(t) \\
X_3(t)
\end{pmatrix},
$$

with evolution equation

$$
\dot{\mathbf{X}}
=
\mathbf{f}(\mathbf{X},\boldsymbol{\theta},t),
$$

where:

- $\mathbf{f}$ is the reduced dynamical vector field;
- $\boldsymbol{\theta}$ is the vector of model parameters;
- $t$ denotes the evolution variable.

For an autonomous closure, the explicit time dependence is absent:

$$
\dot{\mathbf{X}}
=
\mathbf{f}(\mathbf denoted by

boldsymbol{\theta}).
$$

The physical or admissible state domain is denoted by

$$
\mathcal{D}_{\mathrm{adm}}
\subseteq
\mathbb{R}^{3}.
$$

Any stability statement is conditional on the trajectory remaining inside the declared domain $\mathcal{D}_{\mathrm{adm}}$.

---

## 3. Fixed-Point Definition

A point $\mathbf{X}^{\ast}$ is a fixed point of the autonomous closure if

$$
\mathbf{f}(\mathbf{X}^{\ast},\boldsymbol{\theta})
=
\mathbf{0}.
$$

The fixed point is admissible only if

$$
\mathbf{X}^{\ast}
\in
\mathcal{D}_{\mathrm{adm}}.
$$

Therefore, admissibility requires both:

1. satisfaction of the dynamical equations;
2. satisfaction of all declared domain, positivity, boundedness, and constraint conditions.

A formal solution outside $\mathcal{D}_{\mathrm{adm}}$ must not be classified as a physical fixed point.

---

## 4. Linearization Around a Fixed Point

Introduce a perturbation

$$
\delta\mathbf{X}
=
\mathbf{X}
-
\mathbf{X}^{\ast}.
$$

To first order, the perturbed dynamics are

$$
\delta\dot{\mathbf{X}}
=
\mathbf{J}_{\ast}\,
\delta\mathbf{X}
+
\mathcal{O}
\left(
\left\|
\delta\mathbf{X}
\right\|^{2}
\right),
$$

where $\mathbf{J}_{\ast}$ is the Jacobian evaluated at the fixed point:

$$
\mathbf{J}_{\ast}
=
\left.
\frac{\partial\mathbf{f}}
{\partial\mathbf{X}}
\right|_{\mathbf{X}=\mathbf{X}^{\ast}}.
$$

For a three-dimensional state vector,

$$
\mathbf{J}_{\ast}
=
\begin{pmatrix}
\displaystyle\frac{\partial f_1}{\partial X_1}
&
\displaystyle\frac{\partial f_1}{\partial X_2}
&
\displaystyle\frac{\partial f_1}{\partial X_3}
\\[10pt]
\displaystyle\frac{\partial f_2}{\partial X_1}
&
\displaystyle\frac{\partial f_2}{\partial X_2}
&
\displaystyle\frac{\partial f_2}{\partial X_3}
\\[10pt]
\displaystyle\frac{\partial f_3}{\partial X_1}
&
\displaystyle\frac{\partial f_3}{\partial X_2}
&
\displaystyle\frac{\partial f_3}{\partial X_3}
\end{pmatrix}_{\mathbf{X}=\mathbf{X}^{\ast}}.
$$

The Jacobian must be derived from the explicitly stated vector field. It must not be inferred solely from a qualitative description of the model.

---

## 5. Eigenvalue Criterion

Let $\lambda_i$ denote the eigenvalues of $\mathbf{J}_{\ast}$:

$$
\det
\left(
\mathbf{J}_{\ast}
-
\lambda\mathbf{I}
\right)
=
0.
$$

For continuous-time autonomous dynamics:

### 5.1 Locally asymptotically stable fixed point

A sufficient linear criterion is

$$
\operatorname{Re}(\lambda_i)<0
\qquad
\text{for all }i.
$$

Under this condition, sufficiently small perturbations decay exponentially in the linear approximation.

### 5.2 Linearly unstable fixed point

The fixed point is linearly unstable if at least one eigenvalue satisfies

$$
\operatorname{Re}(\lambda_i)>0.
$$

### 5.3 Marginal or nonhyperbolic case

If at least one eigenvalue satisfies

$$
\operatorname{Re}(\lambda_i)=0,
$$

linearization alone is inconclusive. In this case, the analysis must be extended using one or more of:

- higher-order normal-form analysis;
- center-manifold reduction;
- direct nonlinear integration;
- a Lyapunov-function construction;
- bounded-perturbation experiments.

No definitive asymptotic-stability claim should be made from linearization alone in the marginal case.

---

## 6. Lyapunov Stability Test

Let $V(\delta\mathbf{X})$ be a continuously differentiable candidate Lyapunov function satisfying

$$
V(\mathbf{0})=0,
$$

and

$$
V(\delta\mathbf{X})>0
\qquad
\text{for }
\delta\mathbf{X}\neq\mathbf{0}
$$

in a neighborhood of the origin.

A common quadratic candidate is

$$
V(\delta\mathbf{X})
=
\delta\mathbf{X}^{T}
\mathbf{K}
\delta\mathbf{X},
$$

where $\mathbf{K}$ is symmetric positive definite:

$$
\mathbf{K}=\mathbf{K}^{T},
\qquad
\mathbf{K}\succ0.
$$

For the linearized system,

$$
\delta\dot{\mathbf{X}}
=
\mathbf{J}_{\ast}\delta\mathbf{X},
$$

the derivative of $V$ along trajectories is

$$
\dot{V}
=
\delta\mathbf{X}^{T}
\left(
\mathbf{J}_{\ast}^{T}\mathbf{K}
+
\mathbf{K}\mathbf{J}_{\ast}
\right)
\delta\mathbf{X}.
$$

The Lyapunov matrix inequality is

$$
\mathbf{J}_{\ast}^{T}\mathbf{K}
+
\mathbf{K}\mathbf{J}_{\ast}
\prec0.
$$

Equivalently, for a selected positive-definite matrix $\mathbf{Q}$,

$$
\mathbf{J}_{\ast}^{T}\mathbf{K}
+
\mathbf{K}\mathbf{J}_{\ast}
=
-\mathbf{Q},
\qquad
\mathbf{Q}\succ0.
$$

If such a matrix $\mathbf{K}\succ0$ exists, the linearized fixed point is asymptotically stable.

The Lyapunov criterion is a local criterion unless the domain of validity and global properties of the vector field are separately established.

---

## 7. Constraint Preservation

If the closure contains an algebraic constraint

$$
\mathcal{C}(\mathbf{X},\boldsymbol{\theta})=0,
$$

then a valid trajectory must satisfy

$$
\mathcal{C}
\left(
\mathbf{X}(t),\boldsymbol{\theta}
\right)
=
0
$$

throughout its evolution.

A necessary tangency condition for an autonomous system isabla_{\mathbf{X}}\mathcalmathcal{C}}{dt}
=
\nabla_{\mathbf{X}}\mathcal{C}
\cdot
\mathbf{f}(\mathbf{X},\boldsymbol{\theta})
=
0
$$

on the constraint surface.

If this condition is not satisfied, the reduced dynamics do not preserve the constraint and the proposed closure is structurally inconsistent.

For numerical calculations, the constraint residual should be monitored:

$$
\varepsilon_{\mathcal{C}}(t)
=
\left|
\mathcal{C}
\left(
\mathbf{X}(t),\boldsymbol{\theta}
\right)
\right|.
$$

A numerical run is acceptable only after specifying a tolerance $\tau_{\mathcal{C}}$ such that

$$
\varepsilon_{\mathcal{C}}(t)
\leq
\tau_{\mathcal{C}}
$$

over the declared integration interval.

---

## 8. Boundedness and Positivity

If the admissible domain imposes boundedness,

$$
\left\|
\mathbf{X}(t)
\right\|
\leq
B
\qquad
\text{for all }
t\in I,
$$

then the bound $B$, the norm, and the time interval $I$ must be explicitly reported.

If a component is required to be non-negative,

$$
X_i(t)\geq0,
$$

the numerical and analytical treatment must verify that the corresponding boundary is invariant or identify the conditions under which the trajectory can leave the domain.

A finite-time numerical trajectory that remains positive does not, by itself, prove global positivity.

---

## 9. Closure Consistency Conditions

A closure is technically consistent only if the following items are specified:

1. the complete state vector $\mathbf{X}$;
2. the complete parameter vector $\boldsymbol{\theta}$;
3. the evolution equations $\mathbf{f}$;
4. the admissible domain $\mathcal{D}_{\mathrm{adm}}$;
5. all algebraic constraints;
6. the fixed-point equations;
7. the Jacobian definition;
8. the perturbation convention;
9. the stability criterion;
10. the numerical tolerances and integration interval.

If any of these items is missing, the correct classification is:

> Stability status: under-specified

rather than stable or unstable.

---

## 10. Numerical Validation Protocol

For every claimed stable fixed point, report:
```text
State vector:
Parameter values:
Fixed-point residual:
Jacobian:
Eigenvalues:
Largest real eigenvalue:
Lyapunov matrix K, if used:
Constraint residual:
Integration interval:
Initial perturbation norm:
Numerical solver:
Absolute tolerance:
Relative tolerance:
