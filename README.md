# 🦉 OKeepaliveX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OKeepaliveX** — keepalived (VRRP / LVS) Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline keepalived VRRP / LVS configuration-hardening auditor

---

## ✨ Features

- Stdlib keepalived.conf parser — nested blocks, quoted strings, '#' / '!' comments, recursive include globs
- VRRP authentication — PASS plaintext, AH, missing auth, default / weak / truncated / reused auth_pass
- Unicast vs multicast exposure, unicast_src_ip, public peers, vrrp_version, VRID collisions, priority / preempt sanity, advert_int, gratuitous-ARP tuning
- Script security — script_user, enable_script_security, vrrp_script / notify / MISC_CHECK paths, /tmp scripts, world-writable files and directories, shell metachars
- LVS virtual_server — lb_kind, persistence, health checks (HTTP_GET vs SSL_GET, connect_timeout, digest, delay_loop)
- global_defs — router_id, SMTP alerts, SNMP / DBus, dynamic_interfaces, vrrp_strict, lvs_sync_daemon
- systemd unit / drop-in / sysconfig option review
- Secrets masked everywhere; --root offline tree audits
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OKeepaliveX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
