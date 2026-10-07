# PLAN DE AUDITORÍA DE TECNOLOGÍAS DE LA INFORMACIÓN

## CARÁTULA DE LA UNIVERSIDAD
Universidad Privada de Tacna - Curso de Auditoría de Sistemas

## CARÁTULA DEL PLAN DE AUDITORÍA

### AUDITORÍA DE SEGURIDAD WEB EXTERNA A INTERBANK  
### TACNA, PERÚ  
(Tacna, Tacna, Tacna)  

### "Evaluación de Seguridad Web Externa basada en OWASP Top 10 al portal interbank.pe"  

### TACNA, 07 DE OCTUBRE DE 2026  

### “DECENIO DE LA IGUALDAD DE OPORTUNIDADES PARA MUJERES Y HOMBRES”  
### “AÑO DEL BICENTENARIO, DE LA CONSOLIDACIÓN DE NUESTRA INDEPENDENCIA, Y DE LA CONMEMORACIÓN DE LAS HEROICAS BATALLAS DE JUNÍN Y AYACUCHO”  

---

## ÍNDICE

| DENOMINACIÓN                                          | N° Pág. |
|-------------------------------------------------------|---------|
| I. ORIGEN                                             |         |
| II. INFORMACIÓN DE LA ENTIDAD O DEPENDENCIA          |         |
| III. DENOMINACIÓN DE LA MATERIA DE CONTROL           |         |
| IV. ALCANCE                                           |         |
| V. OBJETIVOS                                          |         |
| VI. PROCEDIMIENTOS DE AUDITORÍA                       |         |
| VII. PLAZO DE LA AUDITORÍA Y CRONOGRAMA               |         |
| VIII. CRITERIOS DE AUDITORÍA                         |         |
| IX. INFORMACIÓN ADMINISTRATIVA                       |         |
| IX.1 Comisión Auditora                               |         |
| IX.2 Costos Directos Estimados                       |         |
| X. DOCUMENTO A EMITIR                                |         |
| ANEXOS                                                |         |

---

## I. ORIGEN

La Auditoría de Tecnologías de la Información (TI) se origina a partir de la necesidad detectada de realizar una **Auditoría de Seguridad Web Externa**, centrada en evaluar la exposición del sitio web público de Interbank (https://interbank.pe) ante amenazas externas, sin acceso a sistemas internos ni credenciales. Esta auditoría está alineada con las mejores prácticas del estándar **OWASP Top 10**, con el fin de detectar proactivamente vulnerabilidades explotables desde Internet y prevenir posibles brechas que podrían afectar la integridad, disponibilidad o confidencialidad de los datos y servicios financieros.

---

## II. INFORMACIÓN DE LA ENTIDAD O DEPENDENCIA

- **Entidad/Dependencia**: Banco Internacional del Perú - Interbank  
- **Sector**: Banca y Finanzas  
- **Nivel de Gobierno**: No Aplica (Sector Privado)  

---

## III. DENOMINACIÓN DE LA MATERIA DE CONTROL

Evaluación de Seguridad Web Externa (basada en el marco OWASP Top 10) aplicada a la infraestructura pública, portal institucional y canales de interacción en línea alojados en el dominio https://interbank.pe.

---

## IV. ALCANCE

La auditoría de seguridad cubrirá exclusivamente los servicios digitales públicos accesibles desde el exterior a través del dominio https://interbank.pe. El alcance comprende:
- El portal web institucional.
- Interfaces de inicio de sesión de la banca por internet (solo desde la perspectiva no autenticada).
- Simuladores de préstamos y productos financieros.
- Formularios de contacto y recopilación de datos personales.
- Enlaces y accesos a subdominios institucionales.

La evaluación se realizará estrictamente bajo el enfoque de **Caja Negra** (sin credenciales ni conocimiento interno del código fuente) en el periodo comprendido entre el **12 de octubre de 2026** y el **06 de noviembre de 2026**.

---

## V. OBJETIVOS

### Objetivo General:
Detectar vulnerabilidades técnicas explotables desde Internet y verificar el cumplimiento de prácticas de desarrollo seguro en el portal web de Interbank, fortaleciendo así su postura de ciberseguridad mediante la aplicación de las directrices del marco OWASP Top 10.

### Objetivos Específicos:
1. Evaluar la configuración de los **Encabezados de Seguridad HTTP** (como CSP, HSTS, X-Frame-Options) para prevenir ataques del lado del cliente como Cross-Site Scripting (XSS) o Clickjacking.
2. Verificar la gestión segura de **Cookies de sesión e interacción** comprobando la implementación de los atributos Secure, HttpOnly y SameSite.
3. Analizar la **exposición tecnológica** del portal para identificar bibliotecas JavaScript de terceros o componentes de software con vulnerabilidades conocidas (CVE).
4. Comprobar la existencia y efectividad de la **validación de datos de entrada y mecanismos anti-automatización** (ej. CAPTCHA) en los formularios públicos expuestos.
5. Inspeccionar los **mecanismos de redirección** presentes en el sitio web para mitigar riesgos asociados a redirecciones abiertas (Open Redirects) y phishing.

---

## VI. PROCEDIMIENTOS DE AUDITORÍA

Los procedimientos que se aplicarán durante la auditoría son los siguientes:

**Cuadro n.º 1 – Procedimientos**

| Objetivos Específicos | Procedimientos                                                                                      | Responsable |
|-----------------------|----------------------------------------------------------------------------------------------------|-------------|
| 1                     | 1. Inspección y análisis pasivo/activo de las respuestas HTTP del servidor para verificar encabezados de seguridad. | GH |
| 2                     | 1. Intercepción del tráfico web (proxy HTTP) para auditar la creación y atributos de las cookies emitidas por el portal. | AC |
| 3                     | 1. Análisis de tecnologías web (fingerprinting) y escaneo automatizado para detectar versiones de software desactualizadas. | CC |
| 4                     | 1. Pruebas de inyección y fuzzing manual en campos de formularios. Verificación visual y técnica de controles anti-spam. | GH |
| 5                     | 1. Análisis de parámetros de URL (ej. ?url=, ?redirect=) en enlaces para probar vulnerabilidades de redirección no validada. | AC |

*(CC = Cesar Camac, AC = Andy Calizaya, GH = Gregory Huanca)*

---

## VII. PLAZO DE LA AUDITORÍA Y CRONOGRAMA

El desarrollo de la Auditoría se llevará a cabo dentro del siguiente plazo y cronograma estimado:

| Etapa                 | Fecha de Inicio | Fecha de Finalización |
|-----------------------|-----------------|------------------------|
| Planificación         | 12/10/2026      | 16/10/2026             |
| Ejecución (Pruebas)   | 19/10/2026      | 30/10/2026             |
| Elaboración del Informe | 02/11/2026      | 06/11/2026             |

---

## VIII. CRITERIOS DE AUDITORÍA

La auditoría se llevará a cabo con base en los siguientes criterios:
- Marco de referencia internacional **OWASP Top 10** (Open Web Application Security Project).
- Guía de Pruebas de Seguridad Web de OWASP (OWASP Web Security Testing Guide - WSTG).
- Mejores prácticas de la industria para configuraciones seguras TLS/SSL.
- Políticas internas de seguridad de la información de Interbank (de ser aplicables o públicas).

---

## IX. INFORMACIÓN ADMINISTRATIVA

### IX.1 Comisión Auditora

El equipo encargado de realizar la auditoría estará compuesto por profesionales con experiencia en ciberseguridad ofensiva, pruebas de penetración (pentesting) y análisis de vulnerabilidades web.

**Cuadro n.º 2 – Comisión Auditora**

| Cargo         | Nombres y Apellidos             | Profesión                | Planificación (días) | Ejecución (días) | Informe (días) | Total (días) |
|---------------|---------------------------------|--------------------------|----------------------|------------------|----------------|--------------|
| Supervisor    | Cesar Nikolas Camac Melendez    | Ing. Sistemas / Ciberseg.| 5                    | 10               | 5              | 20           |
| Jefe Comisión | Andy Michael Calizaya Ladera    | Ing. Sistemas / Ciberseg.| 5                    | 10               | 5              | 20           |
| Integrante 1  | Gregory Brandon Huanca Merma    | Ing. Sistemas / Ciberseg.| 5                    | 10               | 5              | 20           |

*(Los costos y asignaciones se evaluarán de forma académica y no requieren presupuesto real).*

---

## X. DOCUMENTO A EMITIR

Como resultado de la auditoría, se emitirá un **Informe de Auditoría de Seguridad Web Externa (Penetration Test Report)**. Este documento incluirá:
- Un resumen ejecutivo de la postura de seguridad del portal web.
- El detalle técnico de los hallazgos (vulnerabilidades) categorizados por su nivel de criticidad (Crítico, Alto, Medio, Bajo, Informativo).
- Evidencias de las pruebas realizadas (Pruebas de Concepto - PoC).
- Recomendaciones técnicas y planes de acción concretos para el equipo de desarrollo de Interbank orientados a remediar cada hallazgo detectado.

---

**Tacna**, **07 de octubre de 2026**

**Cesar Nikolas Camac Melendez**  
Supervisor de Auditoría de Ciberseguridad

**Andy Michael Calizaya Ladera**  
Jefe de Comisión / Pentester Líder 

**Gregory Brandon Huanca Merma**  
Auditor / Especialista en Seguridad Web

---

## ANEXOS

### Anexo 1: Matriz de Riesgos en TI (Relacionados a la Seguridad Web)

| ID | Riesgo Identificado | Causa Potencial | Impacto | Nivel de Riesgo | Controles a Evaluar / Propuestos |
|---|---|---|---|---|---|
| R1 | Secuestro de Sesiones (Session Hijacking) | Cookies configuradas sin los atributos `Secure` y `HttpOnly`. | Robo de credenciales y acceso no autorizado a la banca por internet. | **Alto** | Verificar configuración de cookies. Implementar atributos de seguridad estrictos. |
| R2 | Ataques de Clickjacking | Ausencia del encabezado HTTP `X-Frame-Options` o CSP equivalente. | Engaño a usuarios para realizar acciones no deseadas en el portal bancario. | **Medio** | Auditar cabeceras HTTP de respuesta y recomendar la implementación de políticas de seguridad. |
| R3 | Automatización y Ataques de Fuerza Bruta | Falta de controles anti-spam o CAPTCHA en los formularios web. | Saturación del servicio, creación de cuentas falsas o envíos masivos. | **Medio** | Probar la resiliencia de los formularios e implementar validación tipo CAPTCHA. |
| R4 | Redireccionamientos Maliciosos (Phishing) | Validaciones insuficientes en parámetros de URL que redirigen a subdominios. | Pérdida de confianza del cliente, fraudes y estafas dirigidas. | **Alto** | Analizar el comportamiento de los enlaces y restringir redirecciones a dominios confiables. |
| R5 | Explotación de Vulnerabilidades Conocidas (CVEs) | Uso de bibliotecas de terceros (JavaScript) desactualizadas. | Compromiso del frontend de la aplicación web y ataques XSS. | **Crítico** | Escanear dependencias y recomendar la actualización a versiones seguras. |

---

### Anexo 3: Lista de Normativa y Estándares Aplicables

Durante la ejecución de la auditoría se tomarán como referencia las siguientes normativas, leyes y estándares de la industria:

**Estándares Internacionales y Mejores Prácticas:**
1. **OWASP Top 10 (2021):** Estándar principal para la identificación de los riesgos de seguridad más críticos en aplicaciones web.
2. **OWASP Web Security Testing Guide (WSTG):** Guía metodológica para la ejecución técnica de pruebas de ciberseguridad en aplicaciones web.
3. **ISO/IEC 27001:** En los controles específicos correspondientes al desarrollo y mantenimiento seguro de sistemas de información.

**Normativa Legal Nacional (Perú):**
4. **Ley N° 29733 - Ley de Protección de Datos Personales:** Aplicable debido a que el portal web recopila, procesa y almacena datos personales de clientes.
5. **Resolución SBS N° 504-2021:** Reglamento para la Gestión de la Seguridad de la Información y la Ciberseguridad aplicable a empresas del sistema financiero peruano (como Interbank).
