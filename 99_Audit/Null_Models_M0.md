---
id: sdf-audit-null-001
title: Null Models & Falsification Suite (M0-M3)
version: 3.4.0
status: canonical
canonical: true
layer: 99_Audit
domain: Falsification Testing | Statistical Validation
depends_on:
  - 05_Formalism/Formalism_F.md
tags: [null-model, falsification, ablation-test]
---

# Null Models & Falsification Suite (M0-M3)

## 1. Null Model Hierarchy
جهت ارزیابی معناداری آماری و ابطال‌پذیری تجربی چارچوب SDF، مجموعه‌ای از مدل‌های تهی ($M_0$ الی $M_3$) به صورت سلسله‌مراتبی و مستقل از فرضیه برآمدگی تعریف شده‌اند:

* **مدل $M_0$ (Unconstrained Random Void):**
  فضای فاقد قید انطباق ($\Pi_{C_{\text{adm}}} = \mathbb{I}$)، $\alpha_{\text{eff}} \to \infty$، و عدم وجود رفتار جمعی مقید با ظرفیت گرمایی گاز ایده‌آل ($c_V = \frac{3}{2}k_B$).
* **مدل $M_1$ (Rigid/Static Metric Projection):**
  پروجکشن بدون جفت‌شدگی دینامیکی ($\alpha_{\text{eff}} = 0$) و عدم وجود تبادل انرژی ($\Gamma_{\text{coupling}} = 0$).
* **مدل $M_2$ (Standard Newtonian Viscous Fluid):**
  سیال هیدرودینامیکی پیوسته ناویر-استوکس بدون گاف برشی ($\omega_F = 0$) با طیف پیوسته مدهای تراکمی و برشی استاندارد.
* **مدل $M_3$ (Standard Cosmological Benchmark - $\Lambda\text{CDM}$):**
  مدل استاندارد کیهان‌شناسی با ثابت کیهانی صلب ($w = -1$)، عدم حضور فازهای ماده چگال، و $\Gamma_{\text{coupling}} = 0$.

### فرضیه رقیب اصلی ($H_1$ - SDF Framework)
چارچوب کامل SDF شامل گاف فونونی فعال ($\omega_F > 0$) و رابطه پاشش مقید $\omega(k) = \sqrt{c_t^2 k^2 - \omega_F^2}$ که جفت‌شدگی غیرخطی با انبساط کیهانی را نتیجه می‌دهد.

## 2. Falsification Decision Rule
معیار ابطال‌پذیری و برتری مدل بر اساس شاخص آکائیکه و بیزین (BIC) به صورت زیر فرمول‌بندی می‌شود:
$$\Delta\mathrm{BIC}(H_1, M_k) = \mathrm{BIC}(M_k) - \mathrm{BIC}(H_1)$$

1. **ابطال جفت‌شدگی ساختاری:** اگر $\Delta\mathrm{BIC}(H_1, M_0) < 10$ باشد، ادعای وجود جفت‌شدگی برآمده ($\Gamma_{\text{coupling}}$) از نظر آماری فاقد شواهد کافی بوده و رد می‌شود.
2. **ابطال الاستیسیته برشی موضعی:** اگر $\Delta\mathrm{BIC}(H_1, M_2) < 2$ باشد، وجود گاف برشی $\omega_F$ و ترم الاستیک بولماتوف رد شده و رفتار سامانه به هیدرودینامیک استاندارد نیوتنی تقلیل می‌یابد.
3. **ابطال نسبت به مدل استاندارد:** اگر $\Delta\mathrm{BIC}(H_1, M_3) \le 0$ باشد، مزیت چارچوب برآمده بر $\Lambda\text{CDM}$ رد می‌شود.
