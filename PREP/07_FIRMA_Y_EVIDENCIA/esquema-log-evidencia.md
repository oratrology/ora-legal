# Esquema de Log de Evidencia — ORA PREP

## Objetivo

Definir la estructura mínima de evidencia técnica y trazabilidad generada durante procesos de:

* aceptación legal;
* firma electrónica;
* validación biométrica;
* simulacros supervisados;
* monitoreo de integridad;
* autenticación de usuario.

---

# Campos mínimos recomendados

## 1. Identificación de usuario

* user_id
* nombre_usuario
* email
* identificador interno
* estado de cuenta

---

## 2. Información de sesión

* session_id
* fecha_hora_inicio
* fecha_hora_fin
* timezone
* duración de sesión

---

## 3. Información técnica

* dirección_ip
* user_agent
* navegador
* sistema_operativo
* dispositivo
* resolución_pantalla
* idioma_sistema

---

## 4. Evidencia biométrica

* validación_facial
* prueba_de_vida
* score_confianza
* captura_referencia
* estado_validación

---

## 5. Evidencia de consentimiento

* aceptación_términos
* aceptación_privacidad
* aceptación_firma_electrónica
* aceptación_biometría
* timestamp_aceptación

---

## 6. Eventos de integridad

* cambios_de_pestaña
* pérdida_de_foco
* múltiples_dispositivos
* desconexiones
* actividad_sospechosa
* alertas_automáticas

---

## 7. Evidencia de simulacro

* simulacro_id
* inicio_simulacro
* fin_simulacro
* resultado
* porcentaje
* estado_validación

---

## 8. Seguridad y retención

Los logs y evidencias deberán almacenarse bajo medidas razonables de:

* seguridad;
* confidencialidad;
* integridad;
* control de acceso;
* trazabilidad.

La retención dependerá de:

* políticas internas;
* cumplimiento normativo;
* prevención de fraude;
* resolución de disputas;
* auditoría.

---

## 9. Observaciones

El presente esquema constituye una referencia técnica inicial y podrá evolucionar según necesidades operativas, regulatorias o tecnológicas de ORA PREP.
