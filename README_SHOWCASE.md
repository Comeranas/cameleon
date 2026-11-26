<div align="center">

  <img src="cameleon-marca.png" alt="Cameleon Logo" width="360" />

  # Cameleon

  ### Next-Gen Resilient Cryptographic Steganography Engine
  **Engineered in Rust & WebAssembly — 100% Local-First & Zero-Knowledge**

  <p align="center">
    <a href="https://alejandrobriz.es/cameleon">
      <img src="https://img.shields.io/badge/Launch%20App-alejandrobriz.es%2Fcameleon-bafd00?style=for-the-badge&logoColor=0d0f14&labelColor=0d0f14" alt="Launch Cameleon" />
    </a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
    <img src="https://img.shields.io/badge/WebAssembly-654FF0?style=flat-square&logo=webassembly&logoColor=white" alt="WebAssembly" />
    <img src="https://img.shields.io/badge/Architecture-Zero--Knowledge-bafd00?style=flat-square&logoColor=000" alt="Zero Knowledge" />
    <img src="https://img.shields.io/badge/Security-AEAD%20Encrypted-blue?style=flat-square" alt="AEAD Encrypted" />
    <img src="https://img.shields.io/badge/Offline-PWA%20Ready-emerald?style=flat-square" alt="PWA Ready" />
    <img src="https://img.shields.io/badge/Author-Alejandro%20Briz-e7dbc6?style=flat-square" alt="Author" />
  </p>

  <p align="center">
    <strong>Hide authenticated encrypted messages within ordinary images that survive WhatsApp/Telegram compression and AirDrop direct transfers.</strong>
  </p>

  <p align="center">
    👉 <strong><a href="https://alejandrobriz.es/cameleon">Experience Cameleon Online Now</a></strong> 👈
  </p>

</div>

---

## 🌟 Overview

Conventional cryptography hides the **content** of your message, but flags the conversation as suspicious. **Cameleon** takes privacy to the ultimate level through **cryptographic steganography**: it conceals the very **existence** of the communication inside innocent-looking photographs.

Unlike naive steganography tools (such as plain spatial LSB) that instantly break when an image is compressed or re-encoded, Cameleon features a proprietary **Discrete Cosine Transform (2D-DCT) frequency-domain modulation** paired with **Reed-Solomon Error Correction Codes (ECC)**. 

The result? Your encrypted payload reliably survives heavy lossy JPEG compression (~75% quality) applied by instant messaging networks like **WhatsApp and Telegram**.

<div align="center">
  <img src="imagen/cameleon-color.png" alt="Cameleon Palette & Identity" width="420" />
</div>

---

## ⚡ Key Highlights

* 🔒 **100% Local-First & Zero-Knowledge**: The compiled Rust/WASM core runs exclusively on your device’s browser CPU. No image, password, or secret ever leaves your device or touches any remote server.
* 🛡️ **WhatsApp & Telegram Resilient**: Frequency-band coefficient manipulation coupled with parity correction overcomes destructive re-quantization.
* 📡 **Direct "Over-the-Air" Transfer**: Native support for instantaneous AirDrop (Apple) and Quick Share (Android/Windows) transfers with zero compression and zero network footprint.
* 📊 **Real-Time Entropy & Texture Diagnostic**: Embedded Shannon entropy ($H$) and spatial gradient density analyzer alerts you if an image has enough visual noise to ensure imperceptible camouflage.
* ✈️ **Fully Offline PWA**: Installable as a standalone app on iOS, Android, and Desktop. Works entirely without an internet connection in Airplane Mode.

---

## 🎯 Use Cases

1. **Crypto Seed Phrases & Key Backups**: Safely store 12/24-word recovery seeds hidden inside ordinary vacation photos in Google Photos, iCloud, or external drives.
2. **Investigative Journalism & Source Protection**: Transmit sensitive briefings across monitored national firewalls where Tor or PGP raise immediate red flags.
3. **Plausible Deniability**: Border or checkpoint inspections reveal only mundane family snapshots; without the pre-agreed passphrase, no forensic tool can distinguish the payload from natural camera noise.
4. **Air-Gapped In-Person Exchanges**: Share encrypted files device-to-device over WiFi Direct/Bluetooth without leaving IP logs or telecom server timestamps.

---

## 🚦 Dual Transmission Channels

| Mode | Core Algorithm | Resistance to Compression | Payload Capacity | Optimal Use Case |
| :--- | :--- | :--- | :--- | :--- |
| **WhatsApp / Telegram** | 2D-DCT Mid-Frequency + Reed-Solomon | **High** (Resists ~75% lossy JPEG) | Moderate | Sent as standard chat photos in messaging apps. |
| **Lossless / Document** | RGB Spatial LSB Modulation | **Zero Loss Required** | **Maximum** | Sent via AirDrop, Quick Share, or as document attachments. |

---

## 🚀 Live Web Application

The live application is freely accessible and runs completely in client-side WebAssembly:

### 🔗 [https://alejandrobriz.es/cameleon](https://alejandrobriz.es/cameleon)

---

## 👤 Author & Contact

**Alejandro Briz**
* Website: [alejandrobriz.es](https://alejandrobriz.es)
* GitHub: [@Comeranas](https://github.com/Comeranas)

---

<div align="center">
  <sub>Cameleon © 2026. Designed and built with privacy, aesthetics, and mathematical rigor.</sub>
</div>
