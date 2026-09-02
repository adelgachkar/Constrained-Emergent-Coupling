---
id: sdf-dyn-frw-001
title: Modified FRW Dynamics
version: 3.4.0
status: canonical
canonical: true
layer: 07_Cosmology
depends_on:
  - 06_Projection/Projection_Map_DO_C_to_rho_p_H.md
  - 04_Dynamics/Effective_Fluid_Projection.md
downstream:
  - 99_Audit/Closure_Stability_Criteria.md
---

# Modified FRW Dynamics

## 1. Modified Friedmann Equation
انرژی چگالی مؤثر ناشی از تصویر قیدهای شبکه‌ای $\rho_{\text{SDF}}$ مستقیماً به رد عملگر محدودشده نسبت داده می‌شود:
$$H^2 = \left(\frac{\dot{a}_{\text{eff}}}{a_{\text{eff}}}\right)^2 = \frac{8\pi G}{3}\left(\rho_m + \rho_r + \rho_{\text{SDF}}\right) - \frac{k c^2}{a_{\text{eff}}^2}$$
که در آن انرژی قید برآمده برابر است با:
$$\rho_{\text{SDF}} \equiv \frac{1}{V_{\text{cell}}} \operatorname{Tr}\left(\hat{\rho}_{\text{state}} \hat{H}_{\text{constraint}}\right)$$

## 2. Raychaudhuri / Acceleration Equation
معادله شتاب کیهانی اصلاح‌شده تحت تأثیر فشار ناهمسانگرد و اتلاف حجمی ناشی از گاف فونونی عبارت است از:
$$\dot{H} = -4\pi G \left(\rho_{\text{tot}} + \frac{p_{\text{tot}}}{c^2}\right) + \frac{k c^2}{a_{\text{eff}}^2}$$
که در آن تانسور فشار مؤثر از رابطه زیر پیروی می‌کند:
$$p_{\text{tot}} = p_r + w_{\text{eff}}(\alpha_{\text{eff}})\rho_{\text{SDF}} - \zeta(\omega_F)\Theta_{\text{exp}}$$

## 3. Continuity and Non-Equilibrium Exchange
به دلیل تبادل اطلاعاتی/آنتروپیک میان زیربنای کوانتومی و سیال کیهانی، معادله پیوستگی حاوی ترم چشمه غیرخطی $\Gamma_{\text{coupling}}$ است:
$$\dot{\rho}_{\text{SDF}} + 3H(1 + w_{\text{eff}})\rho_{\text{SDF}} = \Gamma_{\text{coupling}}(\alpha_{\text{eff}}, H)$$
$$\dot{\rho}_m + 3H\rho_m = -\Gamma_{\text{coupling}}(\alpha_{\text{eff}}, H)$$
