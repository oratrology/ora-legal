# ORA — REGLAS DEL SISTEMA DE REGALOS
## Gift System Rules v1.0
**Fecha:** 18 Mayo 2026 | **Estado:** APROBADO
**Compartir con:** ORA 05.1, ORA 05.2, ORA 06, ORA 00 Command Center

---

## 1. ELEGIBILIDAD

- **1 regalo por email registrado** — personal e intransferible
- Requiere aceptar **T&C + Disclaimer** via checkbox obligatorio antes de ver opciones
- **Edad mínima:** 18 años. Entre 16-17 años: requiere checkbox de consentimiento parental/tutor
- **Menores de 16 años:** acceso bloqueado completamente
- El email debe estar **validado** antes de acceder a la selección de regalo

---

## 2. LOS 5 REGALOS DISPONIBLES

| # | Regalo | Personaje | Datos mínimos requeridos | Upgrade disponible |
|---|--------|-----------|--------------------------|-------------------|
| 1 | Carta Natal Resumida | Kael | Nombre + fecha + hora + lugar de nacimiento | ✅ Carta Natal Extendida |
| 2 | Eneagrama Resumido | Kael | Nombre + fecha de nacimiento | ✅ Eneagrama Extendido |
| 3 | I Ching Resumido | Kael | Nombre + pregunta del usuario | ✅ I Ching Extendido |
| 4 | Calendario Lunar + Rituales | Luna | Nombre + signo solar | ✅ Versión Extendida |
| 5 | Ovoscopia (Limpieza de Huevo) | Yaru | Nombre + fecha de nacimiento + foto desde dispositivo | ✅ Lectura Extendida |

> ⚠️ **Ovoscopia excluida para usuarios de 16-17 años**
> ⚠️ **Ovoscopia requiere dispositivo con cámara** — se informa al usuario en el paso a paso
> ⚠️ **Ovoscopia se sube desde dispositivo** — no cámara en tiempo real

---

## 3. PLAZO Y EXPIRACIÓN

- El regalo está disponible por **15 días** desde el registro
- Si no se reclama en 15 días → **expira**, pero el usuario puede comprarlo después a precio normal
- **Con ORA nadie pierde para siempre** — todo producto está disponible para compra posterior
- Emails de recordatorio automáticos:
  - **10 días antes** de expiración (con preview FOMO del regalo)
  - **5 días antes** de expiración (con preview FOMO + urgencia)

---

## 4. CAMBIO DE REGALO

- El usuario **puede cambiar su selección** dentro de los 15 días, antes de reclamarlo
- Una vez **reclamado** (generado y mostrado en pantalla) → definitivo, no cambia
- El personaje vinculado cambia según el regalo escogido

---

## 5. ENTREGA DEL REGALO

- **Versión resumida:** se muestra **en pantalla** inmediatamente
- Generada por IA **una sola vez** → guardada en Supabase (costo controlado)
- El texto es **seductor, impactante y personalizado** — no genérico
- El usuario **no recibe PDF** con el regalo gratuito
- Para envío al email y versión extendida → **requiere upgrade**

---

## 6. DESCARGA PDF

- Solo disponible con **upgrade pagado**
- El PDF queda disponible **indefinidamente** en el perfil del usuario
- Cuando llegue **ORA App** → disponible directamente en la app
- El usuario puede descargarlo **todas las veces que quiera** mientras tenga suscripción activa

---

## 7. SISTEMA DE UPGRADES

- Cada regalo tiene su **propio precio de upgrade** (ver ORA 03 — investigación de precios de mercado)
- Al recibir el regalo gratuito, el usuario recibe automáticamente un **bono de descuento de $10** para el upgrade de ese mismo producto
  - Ejemplo: Carta Natal Resumida → descuento en Carta Natal Extendida
  - Precio estándar: $29.99 → **con descuento: $19.99**
- El descuento **vence junto con el regalo** (15 días)
- Dentro de los 15 días se puede hacer upgrade de múltiples productos (extensión promocional)

---

## 8. MONEDAS Y PAGOS

- Monedas aceptadas directamente: **USD ($) · EUR (€) · GBP (£)**
- Otras monedas: conversión via **API de PayPal** (o la que recomiende ORA 06)
- El precio base se mantiene en número igual por moneda: $19.99 = €19.99 = £19.99
- Para monedas fuera de las 3 principales → conversión en tiempo real al momento del pago

---

## 9. PERSONAJE VINCULADO

- El personaje queda vinculado al **tipo de regalo/producto**, no al usuario
- Cuando el usuario llega a ORA App → el personaje de su regalo es su **guía principal**
- El personaje puede cambiarse después dentro de la app
- Asignación por especialidad:
  - **Kael** → Carta Natal, Eneagrama, I Ching, Numerología
  - **Luna** → Calendario Lunar, Rituales, Tarot, Sueños
  - **Yaru** → Ovoscopia, Shamanismo, Animales de Poder
  - **Krista** → Onboarding, Quiromancia, Lenormand

---

## 10. SUPABASE — FICHA DE USUARIO

La ficha se crea en Supabase **SOLO cuando el usuario acepta y reclama su regalo**.
Si dice "no quiero regalo" → solo queda email en waitlist.

**Campos registrados:**
```
- email
- nombre
- fecha_nacimiento
- hora_nacimiento (si aplica)
- lugar_nacimiento (si aplica)
- signo_solar
- regalo_escogido
- personaje_asignado
- idioma_preferido
- fecha_registro
- fecha_expiracion_regalo (registro + 15 días)
- regalo_reclamado (boolean)
- fecha_reclamo
- texto_regalo_generado (guardado fijo — no se regenera)
- upgrade_comprado (boolean)
- descuento_usado (boolean)
- puntos_lunas_acumulados
- fuente_registro (web / google_oauth)
- pais
- moneda_local
- menor_edad (boolean)
- consentimiento_parental (boolean, si aplica)
```

---

## 11. ASTRAL REWARDS — LUNAS 🌙

- Al registrarse y reclamar regalo → usuario recibe **Lunas** (puntos)
- Al comprar upgrade o producto → acumula más **Lunas**
- Al referir un usuario que se registra → acumula **Lunas**
- Las Lunas se canjean por productos y servicios ORA
- Sistema fortalece **fidelización y membership**
- Detalle de puntos por acción → definir en ORA 06

---

## 12. IDIOMA

- Default: **idioma con el que navegó** la web
- El usuario debe **confirmar el idioma** antes de recibir su regalo
- El regalo se genera y guarda en el idioma confirmado

---

## 13. TECNOLOGÍA

- **Cálculos astrológicos:** Swiss Ephemeris (open source)
- **IA principal:** Claude (Anthropic)
- **IA backup:** ChatGPT → DeepSeek → Perplexity (arquitectura resiliente)
- **Base de datos:** Supabase
- **Pagos:** PayPal principal · Stripe fase posterior
- **Email:** Resend + Edge Functions
- **Hosting:** SiteGround

---

## 14. FLUJO COMPLETO RESUMIDO

```
Registro (email o Google OAuth)
    ↓
Validar email → Success Page
    ↓
Email con link a página de regalos
    ↓
Acepta T&C + Disclaimer ✅ (checkbox obligatorio)
    ↓
Confirma idioma
    ↓
┌─────────────────────────────────┐
│ Escoge 1 de 5 regalos           │
│ O elige "No quiero regalo"      │
└─────────────────────────────────┘
    ↓ (solo si acepta regalo)
Completa datos mínimos según regalo
    ↓
IA genera texto personalizado → se guarda en Supabase
    ↓
Regalo mostrado en pantalla ✨
    ↓
Aparece bono descuento $10 para upgrade (válido 15 días)
    ↓
Acumula Lunas 🌙
    ↓
[Si no reclama] → Recordatorio día 5 y día 10
    ↓
[ORA App lista] → Email con clave temporal → confirma data → entra
```

---

*ORA Gift System Rules v1.0 — Aprobado 18 Mayo 2026*
*Santiago Sáiz / Fundación Hostelling del Ecuador*
