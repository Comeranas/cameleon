# Security & Privacy Policy — Cameleon

## Zero-Knowledge Guarantee

Cameleon operates under a strict **Zero-Knowledge, Client-Side Only** architecture:

1. **No External Network Calls**: The cryptographic engine runs exclusively on your local machine using compiled WebAssembly.
2. **Zero Storage of Secrets**: Neither images, passphrases, nor deciphered messages are ever transmitted, cached on external servers, or logged in telemetry.
3. **Cryptographic Primitives**: Payload protection utilizes modern authenticated encryption with associated data (AEAD) with cryptographically secure key derivation.

## Reporting Security Issues

If you discover any potential vulnerability or security concern regarding Cameleon's cryptographic implementation, please report it privately:

* **Contact**: [Alejandro Briz](https://alejandrobriz.es)
* **GitHub**: [@Comeranas](https://github.com/Comeranas)
