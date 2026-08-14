## Ayush Sinha

Security Engineer (R&D) at ESDS Software Solution, Nashik. I build offensive and
defensive tooling — a multi-tenant DAST platform and a WAF data plane in Rust —
and break things in between.

Recognised by **NCIIPC (Govt. of India)** for responsible disclosure on critical
national infrastructure. CEH v12, CAP. National rank 34 in TechGig Code Gladiators.

```
Languages   Rust · Go · Python · C · Bash · Kotlin
Infra       Linux · Docker · PostgreSQL · FastAPI · GitLab CI
Offensive   Burp · nmap · Metasploit · custom fuzzers/scanners
Focus       AppSec · WAF internals · DAST engineering · vuln research
```

---

### WebScanner — multi-tenant SaaS DAST platform

Built solo at ESDS. Found 200+ real vulnerabilities across client applications.
Python 3.11 · FastAPI · PostgreSQL 16 · Docker · WebSocket.

- **16 scanner modules** — SQLi (error/boolean/time/OAST cascade), XSS, SSRF, SSTI,
  LFI, command injection, open redirect, JWT, API gateway, TLS, headers, CVE
  fingerprinting, exposed `.git`/`.env`
- **OAST engine** — out-of-band detection with external providers plus a local
  DNS/HTTP callback fallback for air-gapped scans
- **LLM false-positive triage** — cut manual verification time by roughly 60%
- **Multi-tenant** — client isolation enforced at both API and DB layer, RBAC
- **MCP server** — 6 tools so an AI agent can drive scans directly
- 87 pytest tests in GitLab CI, automated PDF/HTML reporting

### Next-gen WAF — Rust data plane, Go control plane

Zero-GC request pipeline. Numbers below are from local benchmarks on identical
hardware and rulesets, not vendor marketing:

```
Rule inspection (200 rules)     ~40 µs
Attacker block (early exit)     ~505 ns
Throughput per core             ~25k req/s
p99 latency                     flat — no GC pauses
Rule scaling                    linear
```

For reference, Coraza measured 200–500 µs and ModSecurity 1–5 ms on the same set.

- 7-phase lock-free pipeline; bytecode VM over Aho-Corasick for single-pass
  multi-pattern matching
- Proxy and WAF fused in one process — no IPC, no serialisation hop
- eBPF/XDP pre-filter drops volumetric floods at the NIC before the TCP stack
- WASM plugins (Rust/Go/JS), hot-swappable, distributed via OCI registry
- Isolation Forest anomaly detection + transformer payload classifier
- Go control plane: Raft-clustered admin API, RBAC, multi-tenant orchestration
- HTTP/3 + QUIC, hybrid post-quantum TLS, JA4 fingerprinting

### JWT Attack Suite

Automated JWT assessment covering `alg: none` bypass, RS256→HS256 confusion,
weak-secret brute force, JWK/JKU header injection, expired-token reuse, and
claim tampering for privilege escalation.

### Other work

| Project | What it is | Stack |
|:---|:---|:---|
| [bunkerweb-request-logger](https://github.com/Ayushsinha322/bunkerweb-request-logger) | Custom WAF detection plugins; Heartbleed (CVE-2014-0160) validation | BunkerWeb · C · Docker |
| [reconx-scanner](https://github.com/Ayushsinha322/reconx-scanner) | Terminal recon pipeline, ~40% faster than doing it by hand | Shell · Python · nmap |
| [pentest-reports](https://github.com/Ayushsinha322/pentest-reports) | Penetration test reports and the methodology behind them | Markdown |
| [ipsec-vpn](https://github.com/Ayushsinha322/ipsec-vpn) | IPv6 IPsec VPN lab over IKEv2 | StrongSwan · Linux |
| [Bug-Management-System](https://github.com/Ayushsinha322/Bug-Management-System) | Bug tracker written in plain C | C |
| [MaterialKolor](https://github.com/Ayushsinha322/MaterialKolor) | Material3 colour library for Compose Multiplatform | Kotlin |
| [PaintApp](https://github.com/Ayushsinha322/PaintApp) | Android drawing app on the Canvas API | Kotlin |
| [wifispeedtest](https://github.com/Ayushsinha322/wifispeedtest) | Real-time network speed monitor | Kotlin |

---

### Background

- **Security Engineer, R&D** — ESDS Software Solution · Jun 2025 – present
- **Cybersecurity Intern** — Brainwave Matrix Solutions · Jan – Feb 2025
- **B.Tech CSE (Cybersecurity)** — SRM Institute of Science and Technology · 2021–2025

I write about what I'm building as I build it — daily engineering log at
[ayushsinha322.github.io](https://ayushsinha322.github.io).

Open to AppSec, security engineering, red/blue team, and detection engineering roles.
[Email](mailto:sinhaayush2003@gmail.com) · [LinkedIn](https://www.linkedin.com/in/ayush-sinha-aba246236)
