---
id: sdf-audit-identifiability-001
type: Audit_Node
layer: 99_Audit
version: 3.4.1
status: canonical
role: Parameter_Identifiability_and_Fisher_Analysis
depends_on:
  - Null_Models_M0
  - Residual_Floor_and_Observational_Convergence
  - Coupling_Functional_Forms
downstream:
  - Closure_Stability_Criteria
---

# گره ممیزی: تحلیل شناسایی‌پذیری پارامترها (Identifiability Analysis)

این سند رتبه، استقلال دیفرانسیلی، و میزان هم‌پوشانی (Degeneracy) پارامترهای برآمده مدل SDF را در مقایسه با مدل خنثی $\Lambda\text{CDM}$ مورد ارزیابی ریاضی قرار می‌دهد.

---

## ۱. بردار پارامتر و بردار پیش‌بینی مشاهداتی

بردار پارامترهای کانونیکال مدل SDF به‌صورت زیر تعریف می‌گردد:

$$\boldsymbol{\theta} = \Big( \alpha_0,\, \beta,\, \gamma_0,\, \xi,\, \omega_F,\, \Omega_{m,0},\, H_0 \Big)^{\mathsf{T}} \in \mathbb{R}^7$$

بردار مشاهدات فیزیکی تجمعی شامل داده‌های انبساطی، گاف، و رشد ساختار است:

$$\mathbf{Y}(\boldsymbol{\theta}) = \Big( H(z_k),\, D_A(z_k),\, f\sigma_8(z_k),\, \omega(k_j),\, w_{\text{eff}}(z_k) \Big)^{\mathsf{T}}$$

---

## ۲. ماتریس ژاکوبین حساسیت و ماتریس اطلاعات فیشر (FIM)

ماتریس حساسیت موضعی $\mathbf{J}$ با ابعاد $N_{\text{obs}} \times 7$ تعریف می‌شود:

$$J_{kp} = \frac{\partial Y_k(\boldsymbol{\theta})}{\partial \theta_p}$$

ماتریس اطلاعات فیشر (Fisher Information Matrix) بر اساس ماتریس کوواریانس خطا $\mathbf{C}$ به‌صورت زیر محاسبه می‌گردد:

$$\mathbf{F} = \mathbf{J}^{\mathsf{T}} \mathbf{C}^{-1} \mathbf{J}$$

### ۲.۱. معیار شناسایی‌پذیری محلی (Local Identifiability Criterion)
برای اینکه تمامی پارامترها به‌صورت یکتا قابل استخراج باشند، باید شرط رتبه کامل بر قرار باشد:

$$\operatorname{rank}(\mathbf{F}) = \dim(\boldsymbol{\theta}) = 7 \iff \det(\mathbf{F}) > 0$$

در صورتی که $\lambda_{\min}(\mathbf{F}) < \epsilon_{\text{mach}}$ باشد، یک جهت تخت (Flat Direction) در فضای پارامتر وجود دارد که نمایانگر تداخل نامطلوب دو یا چند پارامتر است.

---

## ۳. تفکیک تداخل گاف فرنکل ($\omega_F$)

بر اساس رابطه پراکندگی در [[Null_Models_M0]] و پدیدارشناسی در [[Emergent_Law_L]]:

$$\omega_F = \frac{2\pi G_\infty}{\eta}$$

از آنجا که مشاهدات کیهان‌شناختی استاندارد فقط به مقدار ترکیب‌شده گاف $\omega_F$ حساس هستند:

$$\frac{\partial \mathbf{Y}}{\partial G_\infty} \propto \frac{\partial \mathbf{Y}}{\partial \omega_F} \left(\frac{2\pi}{\eta}\right), \qquad \frac{\partial \mathbf{Y}}{\partial \eta} \propto \frac{\partial \mathbf{Y}}{\partial \omega_F} \left(-\frac{2\pi G_\infty}{\eta^2}\right)$$

این امر منجر به همبستگی خطی کامل ستون‌های فیشر برای $(G_\infty, \eta)$ می‌شود. 
**دستورالعمل بستار:** پارامتر بنیادین قابل برازش در سطح تحلیل کیهانی اکیداً کمیت منفرد $\omega_F$ است، مگر آنکه داده‌های پراکندگی الکترون (EMS) مندرج در جدول [[Residual_Floor_and_Observational_Convergence]] جهت قیدگذاری مستقل $\eta$ اضافه گردند.

---

## ۴. جداسازی تحول جفت‌شدگی ($\alpha_0$ در برابر $\beta$)

تابع جفت‌شدگی $\alpha_{\text{eff}}(z) = \alpha_0 (1+z)^\beta$ در صورتی تفکیک‌پذیر است که داده‌های توموگرافی سرخ‌گرایی در حداقل دو زون مجزا ($z_1 \ll 1$ و $z_2 > 1$) موجود باشند:

$$\det \begin{pmatrix} 1 & \ln(1+z_1) \\ 1 & \ln(1+z_2) \end{pmatrix} = \ln\left(\frac{1+z_2}{1+z_1}\right) \neq 0$$

این شرط تجربی استقلال مشتقات جزئی $\frac{\partial w_{\text{eff}}}{\partial \alpha_0}$ و $\frac{\partial w_{\text{eff}}}{\partial \beta}$ را تضمین می‌کند.
`
