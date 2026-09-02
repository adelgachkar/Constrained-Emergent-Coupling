---
id: sdf-fnd-geo-bc-001
type: Foundation_Node
layer: 01_Foundation
version: 3.4.1
status: canonical
role: Geometric_Boundary_Formulation
depends_on:
  - Admissibility_Principle_AA
  - Identity_Constraint_Cid
downstream:
  - Effective_Action
  - Canonical_Equations
  - Projection_Map_DO_C_to_rho_p_H
---

# گره پایه: شرایط مرزی هندسی (Geometric Boundary Conditions)

این سند مکمل ساختار عملگری فیلتر $\Pi_{C_{\text{adm}}}$ در [[Admissibility_Principle_AA]] است و شروط مرزی تحلیلی و دیفرانسیلی را روی رویه مرز منیفلد فضازمان $\partial\mathcal{M}$ تثبیت می‌کند.

---

## ۱. مشخصات هندسی مرز

منیفلد جهت‌پذیر $\mathcal{M}$ دارای مرز ریمانی/لورنتسی $\partial\mathcal{M}$ با بردار یکه نرمال $n^\mu$ ($n^\mu n_\mu = \epsilon = \pm 1$) و متریک القایی زیر است:

$$h_{\mu\nu} = g_{\mu\nu} - \epsilon\, n_\mu n_\nu$$

تنسور خمش خارجی رویه مرز به‌صورت زیر تعریف می‌شود:

$$K_{\mu\nu} = h_\mu^{\ \alpha} h_\nu^{\ \beta} \nabla_\alpha n_\beta, \qquad K = h^{\mu\nu} K_{\mu\nu}$$

---

## ۲. رژیم‌های سه‌گانه شرایط مرزی برای میدان‌های SDF

برای متغیرهای حالت $\Phi^A \in (\rho_{\text{SDF}}, H_{\text{eff}}, \alpha_{\text{eff}})$، سه دسته شرط مرزی کانونیکال تعیین می‌شود:

### ۲.۱. شرط دیریکله (مرز نامتغیر / صلب)
میدان در مرز اولیه افق یا فاز کیهان‌شناختی مقید است:

$$\left. \Phi^A(x) \right|_{\partial\mathcal{M}} = \Phi^A_{\text{adm}}(\xi^i)$$

### ۲.۲. شرط نیومن (شار جفت‌شدگی برآمده صفر)
عدم نشت تکانه یا آنتروپی به فراتر از زیرلایه مجاز:

$$\left. n^\mu \nabla_\mu \Phi^A \right|_{\partial\mathcal{M}} = \mathcal{J}^A_{\text{boundary}}$$

در حالت مرز منزوی آدیاباتیک، $\mathcal{J}^A = 0$ است.

### ۲.۳. شرط رابین (مرز تطبیقی رابطه‌ای)
در رژیم‌های گذار توپولوژیک برآمده:

$$\left. \left( n^\mu \nabla_\mu \Phi^A + \Lambda^A_{\ B} \Phi^B \right) \right|_{\partial\mathcal{M}} = 0$$

که $\Lambda^A_{\ B}$ ماتریس پاسخ سختی خلأ در بسامد گاف فرنکل $\omega_F$ است.

---

## ۳. جمله مرزی یورک-گیبونز-هاوکینگ تعمیم‌یافته

جهت رفع جملات مشتق دوم در وردش اکشن [[Effective_Action]] و خوش‌تعریف بودن معادلات، جمله مرزی زیر الزامی است:

$$S_{\partial\mathcal{M}} = M_{\text{Pl}}^2 \oint_{\partial\mathcal{M}} d^3x\,\sqrt{|h|}\, (K - K_0) + \oint_{\partial\mathcal{M}} d^3x\,\sqrt{|h|}\, \mathcal{L}_{\text{surf}}(\Phi^A, \hat{C}_{\text{top}})$$

که در آن $\hat{C}_{\text{top}}$ عملگر مرزی مشتق‌شده از [[Identity_Constraint_Cid]] است که بر پایداری توپولوژیک منیفلد نظارت دارد.
`
