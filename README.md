# 🦉 OKeepaliveX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OKeepaliveX** — keepalived (VRRP / LVS) Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OKeepaliveX is an offline, read-only auditor for keepalived (VRRP / LVS) configuration. It parses nested `keepalived.conf` blocks (including recursive includes) and reviews VRRP authentication, unicast/multicast exposure, script security, LVS health checks, global_defs, and systemd options. Secrets are masked; reports export to TXT, Markdown, JSON, CSV, or SARIF.

---

## ✨ Features

- Stdlib keepalived.conf parser with nested blocks, quoted strings, comments, and recursive include globs
- VRRP authentication checks (PASS plaintext, AH, missing/weak/reused `auth_pass`)
- Unicast vs multicast exposure, VRID collisions, priority/preempt, and advert_int sanity
- Script security: `script_user`, `enable_script_security`, notify/MISC_CHECK paths, world-writable scripts
- LVS virtual_server health-check review and global_defs / SNMP / DBus / systemd unit analysis
- Secret masking, offline `--root` audits, multi-format export, `--demo` and CI severity gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OKeepaliveX -c /etc/keepalived/keepalived.conf --scan
./OKeepaliveX --root ./collected -f sarif -o keepalive.sarif
./OKeepaliveX --demo --fail-on high
./OKeepaliveX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*
