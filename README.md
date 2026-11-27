# 🦎 Cameleon — Resilient Cryptographic Steganography / Esteganografía Criptográfica Resiliente

<p align="center">
  <strong>[ <a href="#english">English</a> | <a href="#español">Español</a> ]</strong>
</p>

---

<a name="english"></a>
## 🇬🇧 English

**Cameleon** is a resilient, local-first (*Zero-Knowledge*) cryptographic steganography platform powered by **Rust compiled to WebAssembly (WASM)**.

Unlike standard encryption—which outputs conspicuous ciphertexts that raise immediate red flags with firewalls and automated filters—steganography conceals the very existence of the communication. Cameleon embeds encrypted data into ordinary carrier photographs, built to withstand the aggressive JPEG compression applied by messaging apps like **WhatsApp and Telegram**.

### ⚡ Live Application
Try the web app directly in your browser (no registration required):  
👉 **[https://alejandrobriz.es/cameleon/](https://alejandrobriz.es/cameleon/)**

* 100% Client-side execution (operates fully in Airplane Mode).
* Zero backend dependencies, zero cloud storage, zero telemetry.

### 🚀 Architecture & Technical Highlights

1. **Dual-Mode Transport:**
   * **WhatsApp / Telegram (2D DCT + Reed-Solomon ECC):**
     - Transforms luminance ($Y$) into frequency domains via **8×8 2D Discrete Cosine Transform (DCT)**.
     - Modulates mid-frequency coefficient pairs $(3,2)$ and $(2,3)$—the exact visual band preserved by standard JPEG compressors.
     - Incorporates **Reed-Solomon Error Correction Codes (ECC)** to restore 100% of the payload even after aggressive re-compression (~70%-75% quality).
   * **Lossless PNG / Document Mode:**
     - Spatial LSB embedding pseudorandomly scattered using **ChaCha20 PRNG**.
     - Maximum throughput for large files, source code, and long texts.

2. **Military-Grade Cryptography (AEAD):**
   * **ChaCha20-Poly1305** authenticated encryption: clean failure detection on tampered files or wrong keys.
   * Salted password key derivation resilient against offline GPU brute-force attacks.

3. **Real-Time Entropy & Texture Diagnostic:**
   * Client-side evaluator calculating **Shannon Entropy** and spatial edge gradient variance to warn users if an image has flat, telltale regions (< 42 score) or is optimal for camouflage (> 70 score).

### 🔍 Security & Privacy Audit (Zero-Knowledge)

Security in cryptographic software is verified through code inspection, not marketing promises:

1. **Zero Telemetry (Zero Network Calls):**
   - Open your browser's Developer Tools (`Network` tab): no `fetch`, `XHR`, or WebSocket requests are made during encoding or decoding.
   - Operates completely offline in **Airplane Mode** once cached as a PWA.
2. **Isolated WebAssembly Memory:**
   - The entire cryptographic and DCT pipeline runs inside the local `/crates/stego-core` engine compiled to WASM.
   - Passwords and payloads reside strictly in volatile memory and are cleared when the browser tab closes.

### 🛠️ Development & Build Commands

```bash
# Run mathematical and cryptographic unit tests
cargo test

# Compile release WebAssembly package
wasm-pack build crates/stego-wasm --target web --out-dir ../../web/pkg --release

# Start local test server
python3 -m http.server 3000 --directory web
```

### ⚖️ License & Intellectual Property
Distributed under a **Source-Available Software License (Non-Commercial Audit & Verification / All Rights Reserved)**. Anyone is permitted to inspect, compile, and audit the source code for security and personal educational purposes. Commercial exploitation, reproduction, or redistribution is strictly prohibited without prior written consent. See [LICENSE](LICENSE).

---

<a name="español"></a>
## 🇪🇸 Español

**Cameleon** es una plataforma de esteganografía criptográfica local-first (*Zero-Knowledge*) desarrollada en **Rust compilado a WebAssembly (WASM)**.

A diferencia del cifrado convencional —que genera cadenas ininteligibles que alertan a filtros y cortafuegos—, la esteganografía oculta la propia existencia del mensaje. Cameleon permite camuflar información confidencial dentro de imágenes cotidianas, resistiendo incluso la compresión destructiva JPEG aplicada por aplicaciones de mensajería como **WhatsApp y Telegram**.

### ⚡ Aplicación en Producción
Prueba la versión web en vivo y sin registro:  
👉 **[https://alejandrobriz.es/cameleon/](https://alejandrobriz.es/cameleon/)**

* 100% Procesamiento en el navegador (funciona en Modo Avión).
* Sin backend, sin almacenamiento en la nube y sin telemetría.

### 🚀 Arquitectura y Tecnologías Clave

1. **Dual-Mode Resiliente & Lossless:**
   * **Modo WhatsApp / Telegram (DCT 2D + Reed-Solomon):**
     - Transforma el canal de luminancia $Y$ a dominios de frecuencia mediante la **Transformada Discreta del Coseno (DCT 8×8)**.
     - Modula coeficientes en pares de frecuencias medias $(3,2)$ y $(2,3)$ para situar los bits en la zona que los compresores JPEG preservan.
     - Integra códigos de corrección de errores **Reed-Solomon (ECC)** con paridad para recuperar el 100% del mensaje frente a la compresión destructiva (~70%-75% calidad).
   * **Modo Lossless PNG / Documentos:**
     - Ocultación espacial LSB con dispersión pseudoaleatoria mediante **ChaCha20 PRNG**.
     - Máxima capacidad para documentos extensos, códigos y volcados sin compresión.

2. **Criptografía Grado Militar (AEAD):**
   * Cifrado autenticado **ChaCha20-Poly1305**: autenticación criptográfica que rechaza intentos fallidos o manipulaciones sin emitir basura.
   * Derivación de claves basada en contraseña con sal criptográfica resistente a ataques de fuerza bruta.

3. **Diagnóstico de Entropía & Textura en Tiempo Real:**
   * Analizador visual integrado en el cliente: calcula la **Entropía de Shannon** y la variación de bordes de la imagen portadora para alertar al usuario si una imagen tiene áreas lisas delatoras (puntuación < 42) o si es óptima para el camuflaje (> 70).

### 🔍 Auditoría de Seguridad & Privacidad (Zero-Knowledge)

La confianza en las herramientas criptográficas se basa en la verificabilidad matemática, no en promesas:

1. **Cero Telemetría (Zero Network Calls):**
   - Puedes abrir las Herramientas de Desarrollador del navegador (pestaña `Red / Network`) y verificar que la aplicación no realiza ni una sola llamada `fetch`, `XHR` o websocket a ningún servidor externo durante el cifrado o descifrado.
   - El motor funciona desconectado en **Modo Avión** una vez cargada la PWA.
2. **Memoria Aislada en WebAssembly:**
   - Todo el proceso de incrustación DCT, paridad Reed-Solomon y cifrado se ejecuta en el crate local `/crates/stego-core` y se compila a WebAssembly.
   - No hay almacenamiento persistente de contraseñas ni logs locales. Al cerrar la pestaña, la memoria volátil del módulo se destruye.

### 🛠️ Comandos de Desarrollo y Compilación

```bash
# Ejecutar tests de integración matemáticos y criptográficos
cargo test

# Compilar el paquete WebAssembly en modo release
wasm-pack build crates/stego-wasm --target web --out-dir ../../web/pkg --release

# Iniciar servidor local de desarrollo
python3 -m http.server 3000 --directory web
```

### ⚖️ Licencia y Propiedad Intelectual
Este proyecto se distribuye bajo una licencia **Source-Available (Código Fuente Auditable / Todos los derechos reservados)**. Se autoriza a cualquier persona o investigador a inspeccionar, compilar, auditar y verificar el código fuente con fines de seguridad y estudio personal. Queda expresamente prohibida la copia, venta, redistribución o explotación comercial de este software o de sus algoritmos derivados sin autorización previa por escrito del autor. Consulta [LICENSE](LICENSE).

---

**Author & Lead Engineer / Autor:**  
[Alejandro Briz](https://alejandrobriz.es) — Software Engineering & Cybersecurity Consulting / Consultoría tecnológica y desarrollo en Cantabria.
