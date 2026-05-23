# Unauthenticated API Token Exposure

<p align="center">
  <img src="https://img.shields.io/badge/Bug_Report-Cybersecurity-0078D4?style=for-the-badge" alt="Bug Report">
  <img src="https://img.shields.io/badge/CTF_Lab-Playable-22C55E?style=for-the-badge" alt="CTF Lab">
  <img src="https://img.shields.io/badge/Category-Sensitive_Data_Exposure_%2F_Missing_Authentication-F97316?style=for-the-badge" alt="Sensitive Data Exposure / Missing Authentication">
  <img src="https://img.shields.io/badge/Severity-Critical-DC2626?style=for-the-badge" alt="Critical">
</p>

---

## Overview

An API endpoint returns credential-like access and refresh tokens without authentication.

This repository is a **sanitized educational case study**. It does not target a real company or live system. The included lab uses mock data so students can safely understand the bug class.

## Quick Facts

| Field | Value |
|---|---|
| Category | Sensitive Data Exposure / Missing Authentication |
| Severity | Critical |
| Related CWE | CWE-200: Exposure of Sensitive Information to an Unauthorized Actor |
| Lab | Browser-based CTF |
| Flag Style | `FLAG{...}` |

## Play the CTF Lab

Run locally:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

Goal: solve the three missions and reveal the flag.

## Report

Read the full report:

```text
report/BUG-REPORT.md
```

## Impact Summary

- Attackers may gain access to protected services depending on token scope.
- Refresh tokens may allow continued access.
- Internal user or app metadata can leak.

## Repository Structure

```text
unauthenticated-api-token-exposure/
|-- README.md
|-- report/
|   `-- BUG-REPORT.md
|-- docs/
|   `-- remediation.md
|-- labs/
|   `-- ctf-game/
|       |-- index.html
|       |-- styles.css
|       |-- app.js
|       |-- manifest.webmanifest
|       |-- service-worker.js
|       `-- assets/
|           `-- ctf-icon.svg
`-- resources/
    `-- references.md
```

## Safety

Use this project only for learning, local labs, and responsible disclosure practice. Do not test destructive actions, IDORs, token exposure, or business-logic abuse against systems you do not own or have permission to test.
