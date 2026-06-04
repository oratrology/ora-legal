# POLÍTICA DE PRIVACIDAD — ORA Plataforma de IA Esotérica
## Versión 2.3 | 4 de junio de 2026
## Responsable de datos: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## PRINCIPIOS CLAVE
- Recopilamos solo lo necesario
- Nunca vendemos tus datos
- Datos biométricos (fotos de mano/iris) eliminados inmediatamente tras la lectura
- Datos de análisis emocional nunca almacenados — solo en tiempo real
- Datos de ubicación (ciudad de nacimiento) transmitidos a Google únicamente durante el autocompletado del onboarding
- Tú controlas tus datos — derechos completos abajo
- Componentes de código abierto solo para cálculos — tus datos nunca son procesados por ellos de forma identificable

---

## 1. DATOS RECOPILADOS

### Datos Estándar
- Identidad: nombre, correo electrónico
- Datos de nacimiento: fecha, hora, lugar (para lecturas)
- Datos de ubicación: ciudad o lugar de nacimiento introducido durante el onboarding (ver Sección 6 — API de Google Places)
- Visuales: fotos de mano (quiromancia), fotos de iris (iridología), fotos de café (tasseografía)
- Narrativos: descripciones de sueños, preguntas personales
- Pago: procesado por Apple/Google/Stripe/PayPal (no almacenado por ORA)
- Recopilados automáticamente: info del dispositivo, uso, IP, ubicación general, analítica (anonimizada)

### 1.1 DATOS BIOMÉTRICOS — PROTECCIÓN MÁXIMA

Fotografías de mano e iris = datos biométricos bajo RGPD Art.9, LOPDP Art.26, LGPD Art.11, BIPA (Illinois).

| Regla | Detalle |
|-------|---------|
| Doble consentimiento | Consentimiento explícito separado — distinto del consentimiento general de cuenta |
| Siempre opcional | Descripción textual siempre disponible como alternativa |
| Limitación de propósito | Usados SOLO para generar tu lectura |
| Eliminación inmediata | Eliminados permanentemente tras generar la lectura |
| Cifrado | TLS 1.3 en tránsito + AES-256 en reposo |
| Sin compartir con terceros | Solo a Anthropic Claude API para generación de lecturas, bajo DPA |
| Sin entrenamiento de IA | Expresamente prohibido |
| Eliminación en 24h a petición | privacy@oratrology.com |

### 1.2 ANÁLISIS EMOCIONAL — DATOS DE CÁMARA PASIVA

Durante sesiones de lectura activa, ORA puede usar la cámara frontal para análisis emocional en tiempo real, exclusivamente para personalizar tu lectura.

| Regla | Detalle |
|-------|---------|
| Sin grabación | No se captura, almacena ni transmite ningún video o imagen |
| Solo tiempo real | No se retiene tras finalizar la sesión |
| Solo uso interno | Nunca mostrado como resultado |
| Nunca compartido | Nunca enviado a terceros |
| Sin entrenamiento de IA | Nunca usado para entrenar modelos |
| Opcional | Deniega el permiso en Configuración → ORA → Cámara |

**Base legal:** RGPD Art. 9(2)(a) + Art. 6(1)(f) | Ecuador LOPDP Art. 26 | Brasil LGPD Art. 11(I)

---

## 2. COMPONENTES DE CÓDIGO ABIERTO Y TRATAMIENTO DE DATOS

ORA usa software de código abierto (incluido Swiss Ephemeris bajo AGPLv3) exclusivamente para cálculos astronómicos y de calendarios. Tus datos personales NUNCA son procesados por estos componentes de forma identificable — solo reciben entradas numéricas anónimas (fecha, hora, coordenadas).

---

## 3. BASE LEGAL (RGPD)

| Actividad | Base |
|-----------|------|
| Cuenta/lecturas/pagos | Contrato Art. 6(1)(b) |
| Datos biométricos (mano/iris) | Consentimiento explícito Art. 9(2)(a) |
| Datos de nacimiento | Consentimiento explícito Art. 9(2)(a) |
| Análisis emocional (cámara) | Consentimiento explícito Art. 9(2)(a) + Interés legítimo Art. 6(1)(f) |
| Autocompletado de ubicación (onboarding) | Interés legítimo Art. 6(1)(f) |
| Analítica | Interés legítimo Art. 6(1)(f) |
| Marketing | Consentimiento Art. 6(1)(a) |
| Cumplimiento legal | Obligación legal Art. 6(1)(c) |

Ecuador: LOPDP consentimiento/legitimidad/proporcionalidad | Brasil: LGPD Arts. 7 y 11

---

## 4. USO DE DATOS

- Lecturas: datos de nacimiento + fotos SOLO para generar tu lectura
- Análisis emocional: personalización en tiempo real — no almacenado
- Datos de ubicación: ciudad de nacimiento almacenada en perfil solo para cálculos astrológicos
- Cuenta: nombre/email para gestión y recibos
- Personalización: historial de lecturas y preferencias
- Recompensas Astrales: datos de actividad para saldo

**NUNCA:** vender datos, compartir con anunciantes, usar fotos o datos emocionales para entrenamiento de IA.

---

## 5. RETENCIÓN DE DATOS

| Dato | Período |
|------|---------|
| Datos de cuenta | Duración de cuenta + 3 años |
| Historial de lecturas | Cuenta + 1 año |
| Fotos biométricas (mano/iris) | ELIMINACIÓN INMEDIATA tras la lectura |
| Datos de análisis emocional | NO SE RETIENEN — solo sesión en tiempo real |
| Otras fotos (café) | 90 días tras la lectura |
| Ubicación de nacimiento (nombre de ciudad) | Duración de la cuenta |
| Registros de pago | 7 años (ley fiscal Ecuador) |
| Analítica (anon) | 3 años |

Eliminación de cuenta: datos personales eliminados en 30 días, fotos en 7 días.

---

## 6. COMPARTICIÓN DE DATOS

| Proveedor | Rol | Datos compartidos | Ubicación |
|-----------|-----|-------------------|-----------|
| Supabase | BD / auth / almacenamiento | Cuenta + datos de lecturas | EE.UU. (AWS) |
| Anthropic Claude | Generación de lecturas IA | Datos de nacimiento, contexto de lectura | EE.UU. |
| Apple (App Store / IAP) | Distribución de app, pagos | Solo tokens de compra | EE.UU. |
| Google (Firebase / Auth) | Autenticación, notificaciones push | Token de dispositivo, credenciales de auth | EE.UU. |
| **Google (API de Places)** | **Autocompletado de ubicación de nacimiento — solo onboarding** | **Texto parcial del lugar escrito por el usuario** | **EE.UU.** |
| Stripe / PayPal | Pagos | Datos de pago tokenizados | EE.UU. |
| OneSignal | Notificaciones push | Token de dispositivo | EE.UU. |

**Transferencias UE:** Cláusulas Contractuales Estándar (CCE) con todos los proveedores en EE.UU.
**Sin venta de datos. Sin actividad de intermediario de datos.**
**Datos de análisis emocional:** procesados en el dispositivo o en sesión únicamente — nunca transmitidos a terceros.

### 6.1 API de Google Places — Divulgación Específica

ORA integra la API de Google Places Autocomplete exclusivamente durante el onboarding para ayudar al usuario a introducir su ciudad de nacimiento:

- **Lo que se envía a Google:** solo el texto parcial escrito en el campo de lugar de nacimiento
- **Lo que Google NO recibe:** nombre, email, fecha/hora de nacimiento, fotos, lecturas ni ningún otro dato personal
- **Lo que ORA almacena:** solo el nombre del lugar seleccionado, como parte de tu perfil para cálculos astrológicos
- **Tratamiento por Google:** regido por los Términos de Servicio de Google (https://developers.google.com/maps/terms) y la Política de Privacidad de Google (https://policies.google.com/privacy)
- **Tu alternativa:** puedes escribir tu ciudad de nacimiento manualmente — el autocompletado no es obligatorio

ORA no es responsable de las prácticas de tratamiento de datos de Google más allá de esta divulgación.

---

## 7. TUS DERECHOS (TODOS LOS USUARIOS)

Acceso, Rectificación, Supresión, Portabilidad, Retirar consentimiento, Reclamación.

**UE/RGPD adicional:** Limitación, Oposición, Sin decisiones automatizadas.
**Ecuador LOPDP:** Reclamación ante Superintendencia de Protección de Datos Personales.
**Brasil LGPD:** Reclamación ante ANPD (gov.br/anpd).
**California CCPA:** Derecho a saber, eliminar, optar por no venta (no vendemos).

Contacto: privacy@oratrology.com — Respuesta: 30 días.

---

## 8. SEGURIDAD

- TLS 1.2+ en tránsito | AES-256 en reposo (Supabase)
- Auth Supabase con soporte MFA
- Controles de acceso, revisiones de seguridad periódicas
- Notificación de brechas RGPD: 72 horas a autoridades

---

## 9. DIVULGACIÓN DE IA

ORA usa la API Claude de Anthropic. Las solicitudes de lectura son procesadas por Anthropic bajo DPA. Minimización de datos aplicada. Sin uso de datos para entrenamiento de IA sin consentimiento.

---

## 10. CONTACTO

- Privacidad: privacy@oratrology.com
- DPD (UE/BR): dpo@oratrology.com
- Legal: legal@oratrology.com
- Hub Legal: https://oratrology.com/legal/

---

## CHANGELOG

| Versión | Fecha | Cambios |
|---------|-------|---------|
| v2.3 | 4 jun 2026 | Sección 1: "Datos de Ubicación" añadidos a datos recopilados. Sección 3: base legal para autocompletado de ubicación añadida. Sección 6: tabla de compartición expandida — Google separado en dos entradas (Firebase/Auth y API de Places). Sección 6.1 añadida: divulgación específica de API de Google Places. |
| v2.2 | 3 jun 2026 | Sección 2 añadida: Componentes de código abierto AGPLv3 y aislamiento de datos. |
| v2.1 | 14 may 2026 | Secciones 1.1–1.2 añadidas: Protección máxima datos biométricos y Análisis emocional. |
| v2.0 | 11 may 2026 | Versión inicial publicada. |

*ORA Política de Privacidad v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
