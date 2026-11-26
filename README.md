# Cameleon

<p align="center">
  <img src="./cameleon-icon.png" alt="Cameleon Logo" width="380" />
</p>

<h3 align="center">🦎 Military-Grade Steganography That Survives WhatsApp Compression</h3>
<p align="center"><strong>Engineered in Rust &amp; WebAssembly • 100% Client-Side • Zero-Knowledge</strong></p>

<p align="center">
  <a href="https://alejandrobriz.es/cameleon">
    <img src="https://img.shields.io/badge/LAUNCH_APP-alejandrobriz.es%2Fcameleon-bafd00?style=for-the-badge&labelColor=0d0f14" alt="Launch Cameleon Live" />
  </a>
</p>

<p align="center">
  <em>No installation required. No sign-up. 100% processed locally in your browser's RAM.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-Core-black?style=flat-square&logo=rust" alt="Rust Core" />
  <img src="https://img.shields.io/badge/WebAssembly-WASM-654FF0?style=flat-square&logo=webassembly&logoColor=white" alt="WebAssembly" />
  <img src="https://img.shields.io/badge/WhatsApp-Resilient_DCT-25D366?style=flat-square&logo=whatsapp&logoColor=white" alt="WhatsApp Resilient" />
  <img src="https://img.shields.io/badge/Zero_Knowledge-Local_First-bafd00?style=flat-square&labelColor=111317" alt="Zero-Knowledge" />
  <img src="https://img.shields.io/badge/AirDrop-Quick_Share-38bdf8?style=flat-square" alt="AirDrop Support" />
</p>

---

## 🧪 Take the 30-Second WhatsApp Challenge

Most steganography tools break the moment you send the image through a chat app. **Cameleon was built specifically to survive it.**

Don't take our word for it — test it right now in **4 simple steps**:

1. **Open the App**: Go to 👉 **[alejandrobriz.es/cameleon](https://alejandrobriz.es/cameleon)**
2. **Hide a Secret**: Pick any photo, type a password, and write a confidential note. The live **Entropy Meter** will evaluate whether your picture has optimal visual texture.
3. **Send via WhatsApp**: Click **"Enviar por WhatsApp"** (or AirDrop) and send the picture to a friend — or to your own chat.
4. **Reveal the Message**: Save the received compressed picture, switch to the **"Revelar Mensaje"** tab, type the password, and watch the authenticated secret reappear flawlessly.

> **💡 Even in Airplane Mode**: You can load the page, turn off WiFi/Mobile Data, and run the entire encryption/decryption offline. Nothing ever leaves your machine.

---

<p align="center">
  <img src="./cameleon-icon.png" alt="Cameleon App Icon" width="160" />
</p>

---

## ⚡ Why Cameleon is Different

When you encrypt a message with PGP or standard ciphers, an interceptor sees garbled gibberish and immediately knows you are hiding something. **Steganography conceals the very fact that a conversation exists.**

| Traditional Web Steganography | 🦎 Cameleon (Rust + WASM) |
| :--- | :--- |
| ❌ **Breaks on WhatsApp**: Naive LSB bit-flipping is erased by lossy JPEG compression. | ✅ **WhatsApp & Telegram Proof**: Uses mid-frequency 2D-DCT coefficients paired with Reed-Solomon parity recovery. |
| ❌ **Sends data to a backend server**: You must trust someone else's cloud. | ✅ **Zero-Knowledge**: 100% executed locally inside your browser CPU via WebAssembly. |
| ❌ **Vulnerable on flat backgrounds**: Alters pixels blindly, creating visible banding. | ✅ **Real-Time Entropy Analyzer**: Shannon entropy ($H$) checks ensure mathematical imperceptibility before embedding. |
| ❌ **No direct sharing**: Tedious manual download and file attachment. | ✅ **AirDrop & WhatsApp Native Integration**: 1-click native system share sheets. |

---

## 🎛️ Dual Operating Modes

* **📱 WhatsApp & Telegram (Resilient DCT + ECC)**:  
  Mathematical modulation in frequency space. Endures destructive ~75% JPEG compression and quantization matrices.
* **📄 Lossless Document & AirDrop (RGB Spatial LSB)**:  
  Maximum payload capacity for long texts, cryptographic keys, or code snippets transferred over AirDrop, Quick Share, or email attachments.

---

## 🎯 Real-World Applications

* **🔑 Crypto Seed Phrase Backup**: Hide your 12 or 24 recovery words inside an ordinary vacation photo stored safely in your camera roll or Google Photos.
* **🕵️ Investigative Journalism**: Send leak reports across censored network firewalls where encryption keywords trigger automated interception.
* **🛂 Plausible Deniability**: Border inspection? Your device contains only normal vacation snapshots. Without the secret key, no forensic tool can distinguish the hidden data from natural camera sensor noise.
* **📡 Zero-Trace AirDrop**: Share sensitive data peer-to-peer across a room with zero IP logs, zero telecom metadata, and zero cloud footprint.

---

## 🚀 Ready to Try?

No signup, no tracking cookies, no server dependencies.

<p align="center">
  <br />
  <a href="https://alejandrobriz.es/cameleon">
    <img src="https://img.shields.io/badge/TEST_CAMELEON_ONLINE-alejandrobriz.es%2Fcameleon-bafd00?style=for-the-badge&labelColor=0d0f14" alt="Test Cameleon" />
  </a>
  <br /><br />
  <strong>👉 <a href="https://alejandrobriz.es/cameleon">https://alejandrobriz.es/cameleon</a> 👈</strong>
</p>

---

## 👤 Author & Credits

Designed and engineered by **Alejandro Briz**
* Website: [alejandrobriz.es](https://alejandrobriz.es)
* GitHub: [@Comeranas](https://github.com/Comeranas)

---

<p align="center">
  <sub>Cameleon © 2026 • Privacy by Math, Not by Policy.</sub>
</p>
