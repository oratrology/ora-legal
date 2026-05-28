# MAPA LEGAL — ORA PREP

## Objetivo

El presente documento organiza la arquitectura legal base de ORA PREP y define la función de cada documento jurídico, técnico y operativo dentro del sistema.

---

# Estructura general

```text
PREP/
```

Contiene toda la documentación legal inicial relacionada con:

* términos de uso;
* privacidad;
* biometría;
* firma electrónica;
* simulacros supervisados;
* integridad;
* propiedad intelectual;
* resolución de conflictos;
* evidencia digital;
* políticas comerciales.

---

# 01_TERMINOS_Y_CONDICIONES

## Archivo principal

```text
terminos-prep-es.md
```

## Función

Define:

* condiciones generales de uso;
* aceptación contractual;
* limitaciones de responsabilidad;
* acceso al sistema;
* reglas generales de operación.

## Dependencias técnicas

Debe conectarse con:

* checkboxes frontend;
* timestamps;
* logs de aceptación;
* session_id;
* validación de usuario.

---

# 02_PRIVACIDAD_Y_DATOS

## Archivos principales

```text
privacidad-prep-es.md
consentimiento-biometrico-camara-es.md
politica-retencion-datos-es.md
```

## Función

Regula:

* tratamiento de datos;
* privacidad;
* biometría;
* uso de cámara;
* prueba de vida;
* retención de evidencia;
* seguridad de información.

## Dependencias técnicas

Debe conectarse con:

* cámara;
* biometría;
* backend de autenticación;
* almacenamiento seguro;
* logs técnicos;
* evidencia digital.

## Revisión recomendada

* protección de datos;
* GDPR;
* normativa biométrica;
* comercio electrónico;
* ciberseguridad.

---

# 03_PAGOS_REEMBOLSOS_FACTURACION

## Archivos principales

```text
politica-no-reembolso-es.md
politica-facturacion-es.md
politica-transferencia-paypal-es.md
```

## Función

Regula:

* pagos;
* facturación;
* transferencias;
* reembolsos;
* contracargos;
* condiciones comerciales.

## Dependencias técnicas

Debe conectarse con:

* Stripe;
* PayPal;
* pasarelas;
* logs de pago;
* sistema contable;
* facturación electrónica.

---

# 04_SIMULACROS_E_INTEGRIDAD

## Archivos principales

```text
reglas-simulacro-supervisado-es.md
aviso-camara-integridad-es.md
politica-anti-trampa-es.md
descargo-puntaje-90plus-es.md
```

## Función

Regula:

* simulacros supervisados;
* integridad académica;
* monitoreo;
* validación de identidad;
* restricciones de uso;
* disclaimers de resultados.

## Dependencias técnicas

Debe conectarse con:

* cámara;
* biometría;
* detección de anomalías;
* monitoreo de sesión;
* validación facial;
* logs de actividad.

---

# 05_PROPIEDAD_INTELECTUAL

## Archivos principales

```text
licencia-contenido-es.md
usos-prohibidos-es.md
proteccion-banco-preguntas-es.md
```

## Función

Protege:

* banco de preguntas;
* simulacros;
* metodología;
* diseños;
* marca;
* contenido;
* estructura visual;
* lógica de evaluación.

## Dependencias técnicas

Debe conectarse con:

* anti-scraping;
* watermarking;
* monitoreo de actividad;
* rate limits;
* detección de bots.

---

# 06_RESOLUCION_DE_CONFLICTOS

## Archivos principales

```text
mediacion-cac-ccg-es.md
resolucion-conflictos-es.md
```

## Función

Regula:

* mediación;
* arbitraje;
* jurisdicción;
* evidencia digital;
* resolución de disputas.

## Revisión recomendada

* abogados civiles;
* comercio electrónico;
* contratación digital;
* arbitraje.

---

# 07_FIRMA_Y_EVIDENCIA

## Archivos principales

```text
consentimiento-firma-electronica-es.md
consentimiento-registro-facial-es.md
esquema-log-evidencia.md
```

## Función

Regula:

* firma electrónica;
* consentimiento digital;
* trazabilidad;
* evidencia biométrica;
* logs jurídicos;
* validación de aceptación.

## Dependencias técnicas

Debe conectarse con:

* Fírmalo;
* biometría;
* backend legal;
* timestamps;
* auditoría;
* almacenamiento de evidencia.

---

# 99_HISTORIAL_DE_CAMBIOS

## Archivo principal

```text
historial-cambios-legales.md
```

## Función

Mantener trazabilidad de:

* versiones;
* modificaciones;
* cambios regulatorios;
* actualizaciones legales;
* revisiones técnicas.

---

# Componentes frontend obligatorios

ORA PREP deberá incorporar:

* checkboxes legales;
* consentimiento explícito;
* timestamps;
* registro de aceptación;
* modal legal inicial;
* validación de usuario;
* políticas visibles antes de pago.

---

# Componentes backend recomendados

## Logs mínimos

* session_id
* user_id
* timestamp
* ip
* navegador
* dispositivo
* biometría
* actividad de sesión
* validación facial
* aceptación legal

---

# Integraciones futuras recomendadas

## Jurídicas

* Fírmalo
* Firma electrónica avanzada
* Evidencia biométrica
* Certificados digitales

## Técnicas

* Stripe
* PayPal
* Firebase
* AWS
* Cloudflare
* Supabase

---

# Estado actual

## Fase

```text
Beta legal-operativa inicial
```

## Pendientes críticos

* revisión jurídica profesional;
* revisión tributaria;
* revisión protección de datos;
* validación biométrica legal;
* integración frontend/backend;
* auditoría de seguridad;
* definición societaria.

---

# Nota importante

La presente estructura constituye una base operativa inicial y deberá evolucionar conforme:

* crecimiento de ORA PREP;
* regulaciones aplicables;
* expansión internacional;
* integración tecnológica;
* nuevos servicios;
* revisión profesional especializada.
