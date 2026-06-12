<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=32&duration=2000&pause=1000&color=00FF88&center=true&vCenter=true&width=600&lines=%E2%9A%A1+Ayush+Sinha;%F0%9F%9B%A1%EF%B8%8F+Cybersecurity+Engineer;%F0%9F%94%A5+Building+Security+at+Scale" alt="Typing SVG" />
  </picture>
</p>

<p align="center">
  <a href="https://ayushsinha322.github.io"><img src="https://img.shields.io/badge/Portfolio-ayushsinha322.github.io-00ff88?style=flat-square&logo=safari" /></a>
  <a href="https://www.linkedin.com/in/ayush-sinha-aba246236"><img src="https://img.shields.io/badge/LinkedIn-ayush--sinha-0077B5?style=flat-square&logo=linkedin" /></a>
  <a href="mailto:sinhaayush2003@gmail.com"><img src="https://img.shields.io/badge/Email-sinhaayush2003-00e5ff?style=flat-square&logo=gmail" /></a>
  <a href="https://github.com/Ayushsinha322"><img src="https://img.shields.io/github/followers/Ayushsinha322?label=Follow&style=social" /></a>
</p>

---

```
$ whoami
Ayush Sinha — Security Engineer @ ESDS Software | NCIIPC Recognised | CEH v12 | CAP
$ uname -r
Building enterprise-grade security tools from scratch. Rust, Go, Python.
```

### 🎯 At a Glance

> **Security engineer** with production experience building **enterprise-grade security tools from scratch** — a multi-tenant SaaS DAST scanner and a next-generation Web Application Firewall. Recognised by **NCIIPC (Govt. of India)** for responsible vulnerability disclosure on critical national infrastructure.

| 🏆 Achievement | 🔢 Metric |
|:---|:---|
| NCIIPC Recognition | **Govt. of India** — among <50 researchers recognised annually |
| TechGig Code Gladiators | **National Rank 34** out of **1,000,000+** participants |
| Vulnerabilities Identified | **200+** across client applications |
| DAST Modules Built | **12** OWASP Top 10 modules, production-grade |
| WAF Benchmark | **5–125× faster** than every open-source & commercial WAF |
| Test Coverage | **87 tests**, all green, GitLab CI/CD pipeline |

---

### 📜 Certifications

<p align="left">
  <img src="https://img.shields.io/badge/CEH_v12-EC--Council-DA1010?style=for-the-badge&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/CAP-Certified_AppSec_Practitioner-0B5E2E?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Cybersecurity_Foundation-Palo_Alto_Networks-F04E23?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Google_Cybersecurity-Google-4285F4?style=for-the-badge&logo=google" />
  <img src="https://img.shields.io/badge/Networking_Basics-Cisco-1BA0D7?style=for-the-badge&logo=cisco" />
</p>

---

### ⚔️ Flagship Projects

#### 🕷️ WebScanner — Multi-Tenant SaaS DAST Platform
*Production-grade vulnerability scanner built solo at ESDS — identifying 200+ real vulnerabilities*

```
├── 12 DAST Modules        → SQLi, XSS, SSRF, SSTI, LFI, CMDi, Open Redirect...
├── AI Analyst             → LLM-powered false-positive triage, reduced manual work by ~60%
├── OAST Engine            → Out-of-band detection with external cascade + LocalOAST fallback
├── Multi-Tenant SaaS      → Full client isolation at API + DB layer, RBAC (admin/user/viewer)
├── Real-Time Dashboard    → WebSocket live-streaming, risk score KPIs, tenant comparison
├── MCP Server             → 6 AI-agent-callable tools via Model Context Protocol
├── CI/CD Pipeline         → 87 pytest tests, GitLab CI/CD, auto PDF/HTML report generation
└── Tech Stack             → Python 3.11 · FastAPI · PostgreSQL 16 · Docker · WebSocket · LLM API
```

<details>
<summary><b>🔍 All 16 Scanner Modules</b></summary>

| Module | Detection Strategy |
|:---|:---|
| Port Scanner | Service enumeration, banner grabbing |
| SSL/TLS | Cipher suite audit, certificate validation |
| Tech & CVE | Technology fingerprinting, CVE database correlation |
| Security Headers | CSP, HSTS, X-Frame-Options, Permissions-Policy |
| SQL Injection | Error-based, blind (boolean/time), OAST — 4-layer cascade |
| XSS | Reflected, stored, DOM-based — polyglot payloads |
| LFI | Path traversal, null-byte injection, wrapper abuse |
| Open Redirect | Parameter pollution, double-encoding bypass |
| Command Injection | OAST → Echo → Error → Time-based fallback chain |
| SSTI | Jinja2, Twig, Freemarker, ERB template injection |
| API Gateway | Endpoint discovery, rate limiting bypass, auth testing |
| Auth Endpoints | JWT analysis, session fixation, password reset flaws |
| SSRF | Internal service probing, cloud metadata exfiltration |
| OAST (OOB) | DNS/HTTP callbacks via oast.pro/live/fun + local fallback |
| Sensitive Files | .git, .env, backup files, config exposure |
| AI FP Filter | LLM-powered false-positive classification |

</details>

---

#### 🛡️ Next-Gen WAF — 5–125× Faster Than Every Competitor
*Rust data plane + Go control plane. Zero-GC. Benchmarked and verified.*

```
┌──────────────────────────────────────────────────┐
│  🏎️  PERFORMANCE                                    │
│  Rule Inspection (200 rules)        40 µs          │
│  Attacker Block Time               505 ns          │
│  Throughput per Core           25,000 req/s        │
│  Tail Latency (p99)         Flat — no GC spikes    │
│  Rule Scaling                     O(n) linear      │
└──────────────────────────────────────────────────┘
```

| WAF | Speed vs. Next-Gen | Rule Latency |
|:---|---:|:---|
| **Next-Gen WAF** | — | **40 µs** |
| Coraza (best open-source) | 5–12× slower | 200–500 µs |
| ModSecurity (legacy standard) | 25–125× slower | 1,000–5,000 µs |
| Cloudflare WAF | 5–50× slower | 200–2,000 µs + RTT |
| AWS WAF | 12–75× slower | 500–3,000 µs + RTT |
| eNlight WAF (ESDS cloud) | 12–75× slower | — |

**Architecture highlights:**
- **Rust data plane** — lock-free 7-phase pipeline, zero-GC, compile-time memory safety
- **Bytecode VM + Aho-Corasick** — single-pass multi-pattern matching, early-exit block at 505ns
- **2-Hop Fusion** — proxy + WAF fused in one process, no IPC, no serialization
- **eBPF/XDP pre-filter** — DDoS dropped at NIC before TCP stack, 30–70% traffic reduction
- **WASM plugin system** — write extensions in Rust, Go, JS; OCI registry; hot-swappable
- **AI/ML built-in** — Isolation Forest anomaly detection, transformer payload classifier, LLM rule copilot
- **Go control plane** — Raft-clustered admin API, RBAC, multi-tenant orchestration
- **Post-Quantum Ready** — HTTP/3 + QUIC, Kyber/Dilithium hybrid TLS, JA4 fingerprinting

---

#### 🔑 JWT Attack Suite
*Automated JWT security assessment — 6 attack vectors for token exploitation*

- **None Algorithm Bypass** (CRITICAL) — accept tokens with `"alg": "none"`
- **RS256→HS256 Algorithm Confusion** — re-sign with public key
- **Weak Secret Brute-Force** — rockyou.txt dictionary attack
- **JWK/JKU Header Injection** — embed attacker-controlled keys
- **Expired Token Reuse Detection** — privilege retention via stale tokens
- **Claim Tampering** — privilege escalation via payload manipulation

---

#### 📡 More Projects

| Project | Description | Stack | Link |
|:---|:---|---:|:---|
| **BunkerWeb WAF Engine** | Custom detection plugins + Heartbleed CVE-2014-0160 validation | BunkerWeb · Docker · C | [Repo](https://github.com/Ayushsinha322/bunkerweb-request-logger) |
| **ReconX Scanner** | Terminal-based vulnerability recon, ~40% time savings | Shell · Python · Nmap | [Repo](https://github.com/Ayushsinha322/reconx-scanner) |
| **Bug Management System** | Low-level C bug tracker — systems programming showcase | C | [Repo](https://github.com/Ayushsinha322/Bug-Management-System) |
| **Pentest Reports** | Professional penetration testing reports & methodology | Markdown · PDF | [Repo](https://github.com/Ayushsinha322/pentest-reports) |
| **IPv6/IPsec VPN Lab** | IPv6 IPsec VPN with IKEv2 — network security deep dive | StrongSwan · Linux | [Repo](https://github.com/Ayushsinha322/ipsec-vpn) |
| **MaterialKolor** | Compose Multiplatform Material3 colour library | Kotlin · Jetpack Compose | [Repo](https://github.com/Ayushsinha322/MaterialKolor) |
| **PaintApp** | Full-featured Android painting app, Canvas API | Kotlin · Android SDK | [Repo](https://github.com/Ayushsinha322/PaintApp) |
| **WiFi Speed Test** | Real-time network speed monitoring app | Kotlin · Networking | [Repo](https://github.com/Ayushsinha322/wifispeedtest) |

---

### 💼 Experience

<img width="100%" src="https://raw.githubusercontent.com/Ayushsinha322/Ayushsinha322/output/snake.svg" />

| Role | Company | Duration |
|:---|:---|---:|
| **Security Engineer — R&D** | ESDS Software Solution · Nashik, MH | Jun 2025 – Present |
| **Cybersecurity & Ethical Hacking Intern** | Brainwave Matrix Solutions · Remote | Jan – Feb 2025 |

---

### 🧰 Technical Arsenal

<table>
<tr>
  <td width="33%" valign="top">

#### 🎯 Core Security
![AppSec](https://img.shields.io/badge/Application_Security-✓-00ff88?style=flat-square)
![Pen Testing](https://img.shields.io/badge/Penetration_Testing-✓-00ff88?style=flat-square)
![DAST](https://img.shields.io/badge/DAST-✓-00ff88?style=flat-square)
![SAST](https://img.shields.io/badge/SAST-✓-00ff88?style=flat-square)
![API Security](https://img.shields.io/badge/API_Security-✓-00ff88?style=flat-square)
![WAF Engineering](https://img.shields.io/badge/WAF_Engineering-✓-00ff88?style=flat-square)
![Secure Code Review](https://img.shields.io/badge/Secure_Code_Review-✓-00ff88?style=flat-square)
![Vuln Research](https://img.shields.io/badge/Vulnerability_Research-✓-00ff88?style=flat-square)

#### 📐 Frameworks
![OWASP Top 10](https://img.shields.io/badge/OWASP_Top_10-✓-00e5ff?style=flat-square)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE_ATT&CK-✓-00e5ff?style=flat-square)
![NIST CSF](https://img.shields.io/badge/NIST_CSF-✓-00e5ff?style=flat-square)
![Cyber Kill Chain](https://img.shields.io/badge/Cyber_Kill_Chain-✓-00e5ff?style=flat-square)
![CIS Controls](https://img.shields.io/badge/CIS_Controls-✓-00e5ff?style=flat-square)
![PTES](https://img.shields.io/badge/PTES-✓-00e5ff?style=flat-square)

  </td>
  <td width="33%" valign="top">

#### ⚔️ Operations
![Red Team](https://img.shields.io/badge/Red_Team-✓-ff4444?style=flat-square)
![Blue Team](https://img.shields.io/badge/Blue_Team-✓-0077B5?style=flat-square)
![Purple Team](https://img.shields.io/badge/Purple_Teaming-✓-purple?style=flat-square)
![SOC](https://img.shields.io/badge/SOC_Operations-✓-ff9800?style=flat-square)
![DevSecOps](https://img.shields.io/badge/DevSecOps-✓-00ff88?style=flat-square)
![Incident Response](https://img.shields.io/badge/Incident_Response-✓-ff4444?style=flat-square)
![Malware Analysis](https://img.shields.io/badge/Malware_Analysis-✓-ff4444?style=flat-square)
![OSINT](https://img.shields.io/badge/OSINT-✓-00e5ff?style=flat-square)

#### 🚨 Detection & Response
![SIEM](https://img.shields.io/badge/SIEM-✓-ff9800?style=flat-square)
![EDR](https://img.shields.io/badge/EDR-✓-ff9800?style=flat-square)
![Log Correlation](https://img.shields.io/badge/Log_Correlation-✓-ff9800?style=flat-square)
![Threat Hunting](https://img.shields.io/badge/Threat_Hunting-✓-ff4444?style=flat-square)
![IOC Analysis](https://img.shields.io/badge/IOC_Analysis-✓-ff4444?style=flat-square)
![Threat Intel](https://img.shields.io/badge/Threat_Intelligence-✓-00e5ff?style=flat-square)

  </td>
  <td width="33%" valign="top">

#### 🔧 Languages & Infrastructure
![Python](https://img.shields.io/badge/Python-✓-3776AB?style=flat-square&logo=python)
![Rust](https://img.shields.io/badge/Rust-✓-000000?style=flat-square&logo=rust)
![Go](https://img.shields.io/badge/Go-✓-00ADD8?style=flat-square&logo=go)
![C](https://img.shields.io/badge/C-✓-A8B9CC?style=flat-square&logo=c)
![Bash](https://img.shields.io/badge/Bash-✓-4EAA25?style=flat-square&logo=gnubash)
![Kotlin](https://img.shields.io/badge/Kotlin-✓-7F52FF?style=flat-square&logo=kotlin)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-✓-4169E1?style=flat-square&logo=postgresql)
![Docker](https://img.shields.io/badge/Docker-✓-2496ED?style=flat-square&logo=docker)
![FastAPI](https://img.shields.io/badge/FastAPI-✓-009688?style=flat-square&logo=fastapi)
![Linux](https://img.shields.io/badge/Linux-✓-FCC624?style=flat-square&logo=linux)
![GitLab CI](https://img.shields.io/badge/GitLab_CI/CD-✓-FC6D26?style=flat-square&logo=gitlab)
![WebSocket](https://img.shields.io/badge/WebSocket-✓-010101?style=flat-square)

#### 🛠️ Security Tools
![Burp Suite](https://img.shields.io/badge/Burp_Suite-✓-FF6600?style=flat-square)
![OWASP ZAP](https://img.shields.io/badge/OWASP_ZAP-✓-00549E?style=flat-square)
![Nmap](https://img.shields.io/badge/Nmap-✓-004B87?style=flat-square)
![Metasploit](https://img.shields.io/badge/Metasploit-✓-1A1A1A?style=flat-square)
![Wireshark](https://img.shields.io/badge/Wireshark-✓-1679A7?style=flat-square)
![Semgrep](https://img.shields.io/badge/Semgrep-✓-0085FF?style=flat-square)
![Nessus](https://img.shields.io/badge/Nessus-✓-00B140?style=flat-square)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-✓-557C94?style=flat-square&logo=kalilinux)

  </td>
</tr>
</table>

---

### 🎓 Education

**B.Tech — Computer Science & Engineering (Cybersecurity)**  
*SRM Institute of Science and Technology, Chennai · 2021 – 2025*

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Ayushsinha322&show_icons=true&theme=dark&title_color=00ff88&icon_color=00e5ff&text_color=c8d8c0&bg_color=0a0e0a&hide_border=true&border_color=00ff8833&ring_color=00ff88" height="170" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ayushsinha322&layout=compact&theme=dark&title_color=00ff88&text_color=c8d8c0&bg_color=0a0e0a&hide_border=true&border_color=00ff8833" height="170" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Ayushsinha322&theme=dark&hide_border=true&background=0a0e0a&stroke=00ff8833&ring=00ff88&fire=00ff88&currStreakLabel=00ff88&sideNums=c8d8c0&currStreakNum=c8d8c0&sideLabels=7a9e80" />
</p>

---

### 🤝 Let's Connect

I'm open to roles across the full cybersecurity spectrum:

> **Red Team** · **Blue Team** · **Purple Team** · **AppSec** · **Security Engineering** · **Threat Intelligence** · **SOC / Detection Engineering**

<p align="center">
  <a href="mailto:sinhaayush2003@gmail.com"><img src="https://img.shields.io/badge/📧_Email-sinhaayush2003@gmail.com-00e5ff?style=for-the-badge" /></a>
  <a href="https://www.linkedin.com/in/ayush-sinha-aba246236"><img src="https://img.shields.io/badge/💼_LinkedIn-ayush--sinha-0077B5?style=for-the-badge&logo=linkedin" /></a>
  <a href="https://ayushsinha322.github.io"><img src="https://img.shields.io/badge/🌐_Portfolio-ayushsinha322.github.io-00ff88?style=for-the-badge" /></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Ayushsinha322&color=00ff88&style=flat-square&label=Profile+Views" />
</p>

---

<p align="center">
  <i>"Security is not a product, it's a process. And I build the tools that make that process faster."</i>
</p>