# Security Policy / Política de Seguridad

---

## [ES] Política de Seguridad, Divulgación y Auditorías

### 1. Modelo de Custodia y Repositorio Privado
El motor criptográfico de alta resiliencia y el código fuente completo de **Cameleon** se encuentran bajo custodia en un repositorio de acceso restringido. Este repositorio público actúa exclusivamente como escaparate institucional, especificación técnica y canal oficial de contacto.

### 2. Auditorías Técnicas y Verificación de Código bajo Acuerdo (NDA)
Respaldamos la verificación independiente por parte de auditores de ciberseguridad, peritos informáticos, investigadores y entidades comerciales interesadas en certificar la ausencia de puertas traseras (*backdoors*), telemetría o canales ocultos de exfiltración.

* **Procedimiento:** El acceso al código fuente completo de Rust y pruebas unitarias se concede bajo la firma previa de un **Acuerdo de Confidencialidad y Evaluación Técnica (NDA)**.
* **Solicitud formal:** Para iniciar el proceso de acreditación de auditoría o debida diligencia técnica, contacte a:
  - **Email:** `contacto@alejandrobriz.es` / `comeranas@gmail.com`
  - **Asunto sugerido:** `[Auditoría Cameleon / NDA] Solicitud de acceso técnico - <Nombre de la entidad / Auditor>`

### 3. Reporte de Vulnerabilidades (Divulgación Coordinada)
Si descubre una vulnerabilidad potencial o un fallo de implementación criptográfica, le rogamos que nos lo comunique de forma confidencial y responsable:
- **No abra un Issue público en GitHub** para reportar vulnerabilidades críticas de seguridad.
- Envíe un informe detallado con los pasos de reproducción o vector de ataque por correo electrónico a `contacto@alejandrobriz.es`.
- Nos comprometemos a acusar recibo en un plazo inferior a **48 horas hábiles** y a coordinar la resolución de forma transparente.

### 4. Principios Fundamentales del Sistema
* **Zero-Knowledge (Conocimiento Cero):** La aplicación web funciona 100% en el procesador local del cliente mediante WebAssembly compilado. Las claves y los mensajes nunca se envían a ningún servidor.
* **Criptografía sin puertas traseras:** Cifrado simétrico AES-GCM-256 autenticado, derivación de clave con Argon2id / PBKDF2 y paridad de frecuencia DCT + Reed-Solomon.

---

## [EN] Security Policy, Responsible Disclosure & Audits

### 1. Custody Model & Private Repository
The resilient cryptographic engine and full source code of **Cameleon** are held under custody within a restricted-access private repository. This public repository serves solely as an institutional showcase, technical specification, and official contact point.

### 2. Technical Audits & Source Code Verification under NDA
We support independent verification by qualified cybersecurity auditors, forensic investigators, and enterprise partners seeking to certify the complete absence of backdoors, telemetry, or data exfiltration channels.

* **Procedure:** Access to the complete Rust source code and test suite is granted strictly under a prior **Non-Disclosure and Technical Evaluation Agreement (NDA)**.
* **Formal Inquiries:** To initiate the audit accreditation process or technical due diligence, please reach out to:
  - **Email:** `contacto@alejandrobriz.es` / `comeranas@gmail.com`
  - **Suggested Subject:** `[Cameleon Audit / NDA] Technical Access Request - <Entity / Auditor Name>`

### 3. Reporting a Vulnerability (Coordinated Disclosure)
If you identify a security vulnerability or cryptographic implementation flaw, please report it confidentially and responsibly:
- **Do not open a public GitHub Issue** to disclose sensitive security vulnerabilities.
- Send a detailed advisory outlining reproduction steps or attack vectors via email to `contacto@alejandrobriz.es`.
- We commit to acknowledging receipt within **48 business hours** and coordinating resolution transparently.

### 4. Core System Principles
* **Zero-Knowledge Architecture:** The web app executes 100% client-side via WebAssembly compiled from Rust. Encryption keys and payload messages are never transmitted over the network.
* **Backdoor-Free Cryptography:** Authenticated AES-GCM-256 encryption, robust key derivation (Argon2id / PBKDF2), and DCT + Reed-Solomon frequency-domain parity.

---
*© 2026 Cameleon — Alejandro Briz.*
