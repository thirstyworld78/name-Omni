# Omni – Autonomous Red Team Lead & Bug Bounty Hunter

> Powered by HexStrike MCP. Streaming pipeline, priority scoring, recursive recon, and advanced attack modules – all generating HackerOne‑ready reports with manual PoC, CVSS, and evidence capture.

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Tools](https://img.shields.io/badge/tools-150+-blue)
![Mode](https://img.shields.io/badge/mode-agentic-purple)
![Shell](https://img.shields.io/badge/shell-zsh%20%7C%20Kali-333)

---

## What is Omni?

**Omni** is an autonomous AI agent (prompt + toolset) designed to perform end‑to‑end bug bounty engagements. It uses the **HexStrike MCP server** (150+ offensive security tools) and an advanced streaming execution engine to:

- **Reconnaissance** – Passive & active subdomain enumeration, JavaScript analysis, recursive discovery.
- **Prioritization** – Criticality scoring of assets based on keywords, tech fingerprints, and role.
- **Vulnerability Scanning** – Automated scanning with adaptive templates and stack‑specific wordlists.
- **Advanced Attack Modules** – Protocol desync, race conditions, GraphQL abuse, SSO exploitation, prototype pollution, business logic testing, and more.
- **Professional Reporting** – Full HackerOne‑style reports with manual step‑by‑step PoC, CWE mapping, CVSS vectors, and auto‑screenshot evidence.

Omni never leaves you waiting: it streams results in real time, reports progress, and can pause/resume across sessions.

---

## Key Features

### 🧠 Intelligent Orchestration
- **Auto‑Tool Selection** – Chooses the best HexStrike tool for each step; no need to specify commands.
- **Chained Findings** – Passes outputs from one tool to the next automatically.
- **Parallel Execution** – Recon, scanning, and deep analysis run simultaneously in batches.

### 🚀 Streaming & Prioritized Pipeline
- **No Idle Waiting** – As soon as a batch of live hosts is discovered, scanning starts while recon continues.
- **Criticality Scoring** – Scores every endpoint (`admin`, `api`, `graphql`, `billing` vs `static`, `marketing`) and prioritizes high‑value targets.
- **Recursive Discovery** – New subdomains, API paths, and hidden parameters are automatically fed back into the recon queue.

### 🔥 Advanced Attack Modules (Auto‑Triggered)
| Module | Trigger | Capabilities |
|--------|---------|--------------|
| **JavaScript Intelligence** | .js files found | API key extraction, endpoint mapping, sourcemap recovery |
| **Authorization Matrix** | Multiple roles / login forms | Vertical/Horizontal privilege escalation via token replay |
| **Protocol Desync & Cache Poisoning** | Cloudflare, Fastly, Akamai | CL.TE / TE.CL smuggling, unkeyed input poisoning |
| **Race Conditions** | State‑changing endpoints (`/redeem`, `/transfer`) | Turbo‑intruder style 50× parallel requests |
| **GraphQL Abuse** | GraphQL endpoint | Introspection brute‑force, deep nesting, batching attacks |
| **SSO Exploitation** | OAuth / SAML redirects | Redirect‑uri manipulation, XML signature wrapping |
| **Prototype Pollution** | Node.js / heavy JS apps | `__proto__` injection, client/server‑side impact |
| **Business Logic Abuse** | Multi‑step forms / checkouts | State skipping, workflow inversion |
| **Secret Lifecycle Validation** | Any discovered key/token | Validity check, scoping (Read/Admin), historical audit |

### 🛡️ Built‑in Safety & Self‑Management
- **Ethical Guardrails** – Scope enforcement, rate limiting, non‑destructive default.
- **Safety‑First Aggression** – Even in Aggressive Mode, high‑risk tools warn before running.
- **Health Checks** – Alerts you if a tool hangs for >10 minutes.
- **Session Memory** – Maintains todo/done lists; supports pause/resume.
- **Log Overflow Prevention** – Summarises large outputs, saves raw logs to `./logs/`.

### 📝 Professional Reporting
- **HackerOne Format** – Title, Summary, Severity (CVSS + CWE), vulnerable endpoint.
- **Manual PoC** – Step‑by‑step reproduction for a human triager, not just raw tool output.
- **Evidence** – Full HTTP traffic, auto‑screenshots, deduplication.
- **Export** – Output to chat or save as `hackerone_report_target_YYYY‑MM‑DD.md`.

---

## Setup
   **Prerequisites**
   - A running **HexStrike MCP server** (provides the 150+ tools).
   - VSCode with the **GitHub Copilot** agent mode enabled.
   - A workspace configured to use the included `.github/agents/omni.agent.md` as the system prompt.
     
# name-Omni
Autonomous Red Team Lead &amp; Bug Bounty Hunter powered by HexStrike MCP. Streaming pipeline, priority scoring, recursive recon, protocol desync, race conditions, GraphQL abuse, SSO exploits, and auto HackerOne reporting with manual PoC, CVSS, and evidence capture. 150+ tools, AI attack suites, business logic abuse, auto screenshots, CVSS.
