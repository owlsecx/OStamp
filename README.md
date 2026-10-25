# 🦉 OStamp

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OStamp** — Advanced Service & Application Fingerprinting Suite

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OStamp is an advanced service and application fingerprinting suite for reconnaissance that combines port scanning, banner grabbing, TLS intelligence and OS fingerprinting. It uses an asynchronous engine with configurable concurrency, protocol-aware probes, and optional TLS certificate inspection via the cryptography library. Results can be exported for later analysis, and it is intended strictly for authorized assessment.

---

## ✨ Features


- Service detection and protocol-aware banner grabbing across a configurable port range
- TLS/SSL detection with X.509 certificate inspection when the cryptography library is present
- OS fingerprinting alongside TCP and optional UDP scanning
- High concurrency (default 150) with per-connection, UDP and probe timeouts
- Filtered-port reporting, probe-packet control and colour toggle for piped output
- Export results to file for downstream processing

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OStamp 10.0.0.5 -p 1-1024 --banner --ssl
./OStamp 192.168.1.10 -p 22,80,443 -u --udp-timeout 3
./OStamp example.com --ssl --filtered -o stamp.txt
./OStamp 10.0.0.5 --no-probe --threads 200
./OStamp --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
