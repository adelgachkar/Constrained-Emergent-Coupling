---
id: sdf-ont-l-001
title: "Emergent Law (L): Gap Pattern & Constraint Relaxation"
version: 3.4.0
status: canonical
canonical: true
layer: 02_Ontological_Architecture
depends_on:
  - 01_Foundation/Relational_Regime_R.md
  - 01_Foundation/Bounded_Substrate_S.md
downstream:
  - 05_Formalism/Formalism_F.md
  - 99_Audit/Null_Models_M0.md
---

# Emergent Law (L): Gap Pattern & Constraint Relaxation

## 1. Structural Genesis & Mathematical Definition
قانون برآمده $L$ بیانگر گذار دینامیکی از جبر عملگرهای غیرتعویضی زیربنای کراندار ($S$) تحت قید رابطه ($R$) به سمت یک ساختار پیوسته و موضعی است. شکست تقارن بازتابی در جبر موضعی برآمده به صورت شکست تقارن تانسوری تجلی می‌یابد:
$$\mathrm{SO}(3) \longrightarrow \mathrm{SO}(2)$$

طیف ویژه‌عملگر هامیلتونی محدود شده روی زیرفضای مجاز تحت تصویر عملگر $\Pi_{C_{\text{adm}}}$، در یک باند فرکانسی مشخص تعریف می‌شود:
$$\omega_F \le \omega \le \omega_D$$
که در آن $\omega_F$ فرکانس گاف برآمده (Constraint Gap Frequency) و $\omega_D$ فرکانس قطع دوبروی موضعی در مشبکه زیربنا است.

## 2. Emergent Dynamics vs. Continuum Approximation
عملگرهای میدان تانسوری موضعی برآمده روی زیرفضا به صورت جمع مقدار میانگین ساختاری و افت‌وخیزهای کوانتومی مقید تجزیه می‌شوند:
$$\hat{Q}_q^\alpha = \bar{Q}_q^\alpha + \hat{\varphi}_q^\alpha$$

### 2.1 Phenomenological Continuum Realization
در تقریب محیط پیوسته و حد ماکروسکوپیک، رابطه پراکندگی مدهای برشی برآمده از قیدهای شبکه‌ای با رابطه هیدرودینامیکی ویسکوالاستیک مدل بولماتوف (Bolmatov et al.) منطبق می‌شود:
$$\omega_F \equiv \frac{2\pi G_\infty}{\eta}$$
که در آن $G_\infty$ مدول برشی ذاتی شبکه و $\eta$ ضریب اتلاف استپ قید است. رابطه پاشش فونون‌های برشی مجاز روی منیفولد مقید عبارت است از:
$$\omega(k) = \sqrt{c_t^2 k^2 - \omega_F^2} \quad \text{for } k \ge k_F \equiv \frac{\omega_F}{c_t}$$

## 3. Structural Constraints on Substrate
قانون برآمده $L$ به صورت درون‌زاد شرایط مرزی زیر را روی مدهای برشی فضا-زمان مؤثر تحمیل می‌کند:
1. **طیف پوچ زیر گاف:** برای تمامی مدهای برشی در ناحیه مادون‌قرمز، رابطه عدم پذیرش برقرار است:
   $$\operatorname{Spec}(\hat{\Omega}) \cap (0, \omega_F) = \emptyset$$
2. **پایداری اسپکترال:** بازگشت به تعادل موضعی تحت تولیدکننده لیندبلاد با زمان ریلکسیشن $\tau = \frac{1}{\omega_F}$ مقید به کران پایداری لیوپانوف است.
