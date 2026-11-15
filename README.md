# Awesome-Endpoint-Data-Loss-Prevention-DLP

## Top Endpoint Data Loss Prevention (DLP) Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Sensitive Data Discovery, Exfiltration Prevention & Self-Hosted DLP Gates*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Endpoint Data Loss Prevention (DLP)**. These tools help organizations discover, classify, and protect sensitive data (PII, PHI, PCI, IP) across endpoints, networks, cloud apps, and AI tools—covering everything from enterprise suites with 1,800+ prebuilt classifiers to lightweight open-source gates that scrub data before it reaches the cloud.

**Examples** include Microsoft Purview, Forcepoint DLP, Symantec DLP, Netskope, Zscaler, Nightfall AI, and open-source alternatives like onprem-dlp and Zero-Leak-DLP (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted data loss prevention, open-source PII redaction, and community-driven exfiltration controls—ideal for organizations seeking data sovereignty and avoiding per-user pricing that scales across headcount. The open-source landscape is genuinely emerging: **onprem-dlp** provides a CPU-only gate that scrubs data before cloud egress , **Zero-Leak-DLP** targets AI agent secret exfiltration , and **Presidio** (referenced as an adapter) offers mature PII detection .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Microsoft Purview DLP](https://www.microsoft.com/en-us/security/business/microsoft-purview)** | Integrated DLP across Microsoft 365, endpoints, and cloud apps. **Purview Suite: €10.40/user/month** (annual) includes DLP, Information Protection, Insider Risk, and eDiscovery . **Content-blind outside M365**—relies on labels and patterns, does not inspect non-Microsoft destinations . | Suite: **€10.40/user/month** (annual) | No free tier; trial via Microsoft 365 E3/E5 licensing |
| **[Forcepoint DLP](https://www.forcepoint.com/)** | Unified DLP across endpoint, network, email, and cloud. **1,800+ prebuilt classifiers** covering 90+ countries' compliance requirements. **AI Policy Advisor** guides deployment; **Risk-Adaptive Protection** adjusts enforcement based on user risk. Extends to generative AI tools (ChatGPT, Copilot, Gemini) . | Quote-only (cloud or on-premises) | **30-day full-access trial** (no credit card, no feature gates) . |
| **[Symantec DLP](https://www.broadcom.com/)** | Enterprise DLP with broad channel coverage (USB, email, web) and **strong incident-to-user attribution** for fast response. Works on-premises or cloud with AWS/Azure/GCP integration. | **$1.99/user/year** (starting) | No free trial . Support quality and scanning speed are frequent complaints . |
| **[Netskope DLP](https://www.netskope.com/)** | Cloud-native DLP within Netskope One SASE platform. Covers SaaS, IaaS, web, and email with AI-powered data visibility and consistent policies. | Quote-only | No free tier; demo via sales |
| **[Zscaler Data Protection](https://www.zscaler.com/)** | Unified DLP across endpoints and cloud services. Discovers, classifies, and protects data in motion and at rest. AI-powered visibility with consistent DLP policies. | **$39.89/user/year** (GovCloud High, 1-year) | No free tier; demo via sales |
| **[Digital Guardian](https://www.digitalguardian.com/)** | Deep, customizable DLP for mixed environments (finance, healthcare, tech). Granular visibility, predefined templates for GDPR/HIPAA/PCI-DSS, and role-based policy shaping. CASB integration and ML threat detection. | Quote-only (**$1,000+ range** per SelectHub analysis) | No free tier; demo via sales |
| **[Proofpoint DLP](https://www.proofpoint.com/)** | Email-centric DLP with encryption and threat protection. Controls information leaving via email, social media, and file sharing. Automated discovery and remediation. | **$667.31/user/year** (Service Edition, 1-500 users) | No free tier; demo via sales |
| **[McAfee DLP](https://www.mcafee.com/)** | DLP suite covering Discover, Monitor, Prevent, and Endpoint modules. Centralized incident management with policy engine across networks, endpoints, and cloud. | Quote-only (custom plan) | **Free trial** available |
| **[Nightfall AI](https://www.nightfall.ai/)** | **AI-native DLP with 95% detection precision** using transformer-based detectors (not regex). Covers SaaS (12 apps), endpoints, browsers, and AI tools. **Claims ~50x lower TCO than legacy DLP** due to reduced false positives and bundled pricing . | Quote-only (per-user, includes 2 endpoint devices) | **7-day proof of value** (not self-serve) with free security assessment . |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[onprem-dlp](https://github.com/portable-genai/onprem-dlp)** | [![Stars](https://img.shields.io/github/stars/portable-genai/onprem-dlp?style=social&color=white)](https://github.com/portable-genai/onprem-dlp/stargazers) | **The most complete open-source DLP gate for pre-cloud egress.** Apache-2.0, CPU-only, runs **entirely on-prem**—no byte reaches the cloud unless the gate says so . **Unstructured**: detects PII in free text and images (OCR), redacts (tag/mask/hash/remove) or black-boxes pixel regions, issues **ALLOW/REDACT/BLOCK** decisions with human escalation for BLOCK. **Structured**: profiles CSV/SQLite/PostgreSQL/MySQL/BigQuery columns and classifies as PII_DIRECT/PII_QUASI/SENSITIVE/NON_PII using weighted signals. **Deterministic core** with checksum validators (Luhn, IBAN mod-97, SG NRIC, HK HKID) plus optional Gemma/Presidio adapters . **Best for organizations wanting to scrub data before sending to cloud LLMs or APIs** with a transparent, auditable gate. |
| **[Zero-Leak-DLP](https://github.com/AAH20/zero-leak-dlp)** | [![Stars](https://img.shields.io/github/stars/AAH20/zero-leak-dlp?style=social&color=white)](https://github.com/AAH20/zero-leak-dlp/stargazers) | **Purpose-built DLP for AI agent exfiltration.** 100% Python Standard Library—**zero external dependencies**. **Sub-millisecond execution (<0.02ms)**. Recursive protocol unpacker decodes Base64, Hex, URL-encoding, and nested JSON. **High-entropy credential scanner** (API keys, AWS tokens, private keys, JWTs) and **real-time PII redaction** (SSNs, emails, credit cards). **Cryptographic SHA-256 AuditLedger** for ISO 42001 and SOC 2 Type II compliance . **Best for teams deploying AI agents** that need to prevent secret and PII leakage in outbound payloads. |
| **[Presidio](https://github.com/microsoft/presidio)** | — | **Microsoft's open-source PII detection and anonymization framework.** Used as an optional NER adapter in onprem-dlp . Supports text and image anonymization with customizable recognizers for names, addresses, and custom entity types. **Best for teams building custom PII detection pipelines** that need mature, battle-tested detection logic . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[OpenDLP](https://github.com/ezra100/OpenDLP)** | — | **Open-source data loss prevention scanner** for identifying sensitive data (credit cards, SSNs, PII) across file shares and databases. Discovery-focused rather than real-time prevention. **Best for organizations wanting a self-hosted sensitive data discovery tool** to complement broader DLP strategies . |

**Frameworks for building custom systems**: Choose **onprem-dlp** for a deterministic, auditable gate that scrubs data before cloud egress with ALLOW/REDACT/BLOCK decisions , **Zero-Leak-DLP** for AI agent secret and PII protection with a cryptographic audit ledger , and **Presidio** for mature PII detection as a building block —all without per-user pricing that scales with headcount.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- DLP platforms handle sensitive data including PII, PHI, and credentials; enforce least-privilege access, audit logging, and compliance with applicable data protection regulations. **DLP policy errors can either block legitimate business or allow exfiltration.**
- **Pricing transparency varies dramatically and hidden costs compound.** **Symantec DLP starts at $1.99/user/year** but has no free trial and frequent support complaints . **Microsoft Purview is €10.40/user/month** but **content-blind outside the Microsoft 365 ecosystem**—it does not inspect non-Microsoft destinations . **Forcepoint offers a genuine 30-day full-access trial** with 1,800+ classifiers, but commercial pricing is quote-only . **Nightfall AI claims ~50x lower TCO than legacy DLP** by bundling SaaS, endpoint, and AI coverage into one per-user price with 95% precision—reducing analyst time on false positives . **Open-source DLP is genuinely emerging**: onprem-dlp provides a deterministic pre-cloud gate with ALLOW/REDACT/BLOCK decisions , and Zero-Leak-DLP targets AI agent exfiltration with a cryptographic audit ledger . **Validate detection precision on your own data, enforcement scope, and total cost of ownership** (including analyst time) before committing.

---

**Made for security engineers, data protection officers, and organizations building data-centric defense.**  
Let's make endpoint data loss prevention more open, precise, and cost-predictable.
