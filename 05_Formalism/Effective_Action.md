---
id: sdf-form-action-001
type: Formalism_Node
layer: 05_Formalism
version: 3.4.1
status: canonical
role: Effective_Action_Foundation
depends_on:
  - Formalism_F
  - Identity_Constraint_Cid
  - Geometric_Boundary_Conditions
downstream:
  - Canonical_Equations
  - Modified_FRW_Dynamics
  - Closure_Stability_Criteria
---

# گره فرمالیسم: کنش مؤثر ($S_{\text{eff}}$)

این سند چارچوب وردشی کانونیکال سامانه برآمده SDF را تعریف کرده و ارتباط میان عملگرهای تحول باز ($\mathcal{D}_t$) و معادلات هیدرودینامیکی پیوستگی کیهان‌شناختی را برقرار می‌سازد.

---

## ۱. تعریف تابعک کنش کل

کنش مؤثر کلی سامانه در منیفلد فضازمان $\mathcal{M}$ به همراه مرز $\partial\mathcal{M}$ به‌صورت تابعی از متریک $g_{\mu\nu}$، میدان مؤثر زیرلایه $\Phi_{\text{SDF}}$، و پارامتر جفت‌شدگی برآمده $\alpha_{\text{eff}}$ تعریف می‌شود:

$$S_{\text{eff}}[g_{\mu\nu}, \Phi_{\text{SDF}}, \alpha_{\text{eff}}] = \int_{\mathcal{M}} d^4x\,\sqrt{-g} \left[ \frac{M_{\text{Pl}}^2}{2} R + \mathcal{L}_{\text{SDF}}(\Phi_{\text{SDF}}, \nabla_\mu \Phi_{\text{SDF}}) + \mathcal{L}_{\text{cpl}}(\Phi_{\text{SDF}}, \alpha_{\text{eff}}) + \mathcal{L}_{\text{con}} \right] + S_{\partial\mathcal{M}}$$

که در آن:
- $M_{\text{Pl}} = (8\pi G)^{-1/2}$ جرم کاهیده‌ی پلانک است.
- $R$ اسکالر ریچی منیفلد فضا-زمان است.
- $S_{\partial\mathcal{M}}$ جمله مرزی سازگارکننده وردش (هماهنگ با [[Geometric_Boundary_Conditions]]) است.

---

## ۲. چگالی لاگرانژی زیرلایه و برهم‌کنش

چگالی لاگرانژی بخش برآمده SDF شامل بخش جنبشی اصلاح‌شده با توپولوژی و پتانسیل مؤثر است:

$$\mathcal{L}_{\text{SDF}} = -\frac{1}{2} P^{ab}(\alpha_{\text{eff}}) \nabla_a \Phi_{\text{SDF}} \nabla_b \Phi_{\text{SDF}} - V_{\text{eff}}(\Phi_{\text{SDF}})$$

جمله جفت‌شدگی غیرکمینه‌ای با مقیاس خمش و برهم‌کنش ماده به‌صورت زیر تعیین می‌شود:

$$\mathcal{L}_{\text{cpl}} = -\frac{1}{2} \xi R \alpha_{\text{eff}}^2 - \Gamma_{\text{coupling}} \mathcal{K}_{\text{int}}(\Phi_{\text{SDF}})$$

که با روابط داده‌شده در [[Coupling_Functional_Forms]] و نگاشت [[Projection_Map_DO_C_to_rho_p_H]] تطابق دارد.

---

## ۳. جملات قید و پروجکشن مجاز ($\Pi_{C_{\text{adm}}}$)

قیود ناوردایی گره [[Identity_Constraint_Cid]] از طریق متغیرهای کمکی لاگرانژ $\lambda_A$ در چگالی قید اعمال می‌شوند:

$$\mathcal{L}_{\text{con}} = \sum_A \lambda_A \cdot \left[ (\mathbb{I} - \Pi_{C_{\text{adm}}}) \Phi_A \right]$$

اصل تغییرات مقید ایجاب می‌کند که فضای وردش‌ها اکیداً محدود به زیرفضای مجاز باشد:

$$\delta S_{\text{eff}} \Big|_{\Phi \in \mathcal{S}_{\text{adm}}} = 0 \iff \Pi_{C_{\text{adm}}} \left( \frac{\delta S_{\text{eff}}}{\delta \Phi} \right) = 0$$

---

## ۴. ارتباط با فرمالیسم لیندبلاد و بستار اتلافی

به دلیل حضور ترم‌های اتلافی و ویسکوزیته ساختاری ($\zeta(\omega_F)$) مشتق‌شده در [[Formalism_F]]، تحول وردشی از طریق تصویر دوگانه شوینگر-کلدیش به مولد تحول زمانی مربوط می‌شود:

$$\frac{d}{dt}\langle \hat{\mathcal{O}} \rangle = \mathrm{Tr}\left( \mathcal{D}_t(\hat{\rho}) \hat{\mathcal{O}} \right) \quad \longleftrightarrow \quad \nabla_\mu T^{\mu\nu}_{\text{eff}} = \mathcal{Q}^\nu_{\text{diss}}$$

هسین دوم تابعک انرژی پیرامون نقطه تعادل اکسترمم کنش:

$$K_{ij} = \frac{\partial^2 S_{\text{eff}}}{\partial X_i \partial X_j}$$

به‌طور مستقیم شرط ماتریسی لیاپانوف در [[Closure_Stability_Criteria]] را بازتولید می‌کند.
`
