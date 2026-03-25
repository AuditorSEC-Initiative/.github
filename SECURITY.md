# Security Policy

## Supported Versions

| Component | Supported |
|-----------|----------|
| auditorsec-llm-bridge | main branch |
| bachmach-pqc-iot-sentinel | main branch |
| auditorsec-summaries-fuel-mvp | main branch |
| dabroiotexs-dao-decentralization | main branch |

## Reporting a Vulnerability

**Please do NOT open public GitHub issues for security vulnerabilities.**

We take security seriously. If you discover a vulnerability:

### Private Disclosure

1. Email: **romanchaa997@auditorsec.com**
   - Subject: `[SECURITY] Brief description`
   - Include: affected component, steps to reproduce, impact assessment
   - Attach: any PoC code (please do not publish)

2. We will acknowledge within **48 hours**.
3. We will provide a fix timeline within **7 days**.
4. We will credit you in the release notes (unless you prefer anonymity).

### What to Report

- Smart contract audit engine bypasses
- PQC implementation weaknesses (ML-KEM/ML-DSA)
- Authentication/authorization flaws in API endpoints
- Injection vulnerabilities (SQL, command, NATS message)
- Secrets or credentials exposed in code
- Supply chain / dependency vulnerabilities
- IoT firmware vulnerabilities (ESP32/RP2040 edge nodes)

### Responsible Disclosure Policy

- We ask for 90 days to patch before public disclosure.
- We will not take legal action against researchers acting in good faith.
- We follow coordinated vulnerability disclosure best practices.

## Security Contacts

- Email: romanchaa997@auditorsec.com
- Telegram: [@audityzerbot](https://t.me/audityzerbot)
- PGP key: available on request

## Security Design Principles

- Post-Quantum Cryptography: ML-KEM-768 + ML-DSA-65 (NIST FIPS 203/204)
- Policy-as-code: OPA/Rego for all authorization decisions
- Supply chain: Trivy scans in CI, SBOM generation planned
- Secrets: Never committed; use GitHub Actions secrets + Kubernetes secrets
- Dependencies: Renovate bot for automated dependency updates (planned)
