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
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Data Loss Prevention (DLP) market is estimated at **$3.4B–$4.2B in 2025–2026** (expanding past $30B+ when including broader integrated SSE/SASE platforms), with the endpoint DLP segment experiencing rapid ~23% CAGR driven by hybrid work, BYOD risks, and shadow AI usage. The sector exhibits **moderate-to-high market concentration**, dominated by tier-1 hyperscalers and cybersecurity conglomerates (where Microsoft Purview alone captures over 20% share alongside Broadcom, Proofpoint, and Trellix accounting for nearly 60% of the market), while agile innovators (e.g., Nightfall AI) and open-source DLP engines (e.g., onprem-dlp, Zero-Leak-DLP) contest specialized AI egress and self-hosted niches.

## SaaS/Hosted Platforms

| Product | Company Scale (Valuation / Revenue) | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------------------------------|-------------|-------------------|--------------------------|
| **[Microsoft Purview DLP](https://www.microsoft.com/en-us/security/business/microsoft-purview)** | **~$3.89T** Market Cap (Microsoft) | Integrated DLP across Microsoft 365, endpoints, and cloud apps. Native Windows kernel/OS-level telemetry with prebuilt regulatory templates. Content-blind outside M365 without additional connectors. | **$12.00/user/month** (annual, add-on to M365 E3; or bundled in M365 E5 at $60.00/user/month) | **90-day free trial** (up to 25 Purview Suite trial licenses for M365 E3 tenants; one 30-day extension allowed) |
| **[Symantec DLP](https://www.broadcom.com/)** | **~$1.65T** Market Cap (Broadcom) | Enterprise DLP with comprehensive endpoint agent coverage (USB, print, network, clipboard) and mature incident attribution. Highly customizable for complex regulatory environments. | **$1.99/user/year** (starting per seat, volume-dependent) | **90-day proof of concept (POC)** available via Broadcom partner/support request; no permanent free tier |
| **[Zscaler Data Protection](https://www.zscaler.com/)** | **~$31.5B** Market Cap | Unified DLP across endpoints, web, and cloud apps integrated within the Zscaler Zero Trust Exchange. Automated classification and inline TLS/SSL inspection. | **$39.89/user/year** (starting baseline for GovCloud/Enterprise per seat) | **30-day proof of concept (POC)** available via enterprise evaluation agreement; no permanent free tier |
| **[Proofpoint DLP](https://www.proofpoint.com/)** | **$12.3B** Valuation (Acquired by Thoma Bravo; ~$2.45B ARR) | People-centric DLP and insider threat management. Correlates user behavior, sensitive data movement, and email exfiltration with automated remediation workflows. | **$667.31/user/year** (Enterprise Service Edition tier, 1–500 users) | **30-day free trial** (or structured 14-day rapid evaluation POC with threat assessment report); no permanent free tier |
| **[Netskope DLP](https://www.netskope.com/)** | **~$9.1B** Market Cap (NASDAQ: NTSK) | Cloud-native endpoint and SASE DLP powered by Netskope One. Inspects data in motion and at rest across SaaS, IaaS, web, and private apps with 3,000+ data identifiers. | **$50.00/user/year** (~$4.17/user/month for entry Standard DLP bundles) | **30-day proof of concept (POC)** (or 14-day self-paced test drive for select modules); no permanent free tier |
| **[McAfee DLP](https://www.mcafee.com/)** | **~$5.2B** Merged Value (~$1.1B Revenue; STG / Trellix) | Now Trellix DLP. Endpoint and network monitoring suite featuring centralized incident management, device rule enforcement, and unified policies via ePO. | **$45.00/user/year** (starting baseline quote per seat) | **90-day free trial** (for McAfee/Trellix Endpoint DLP evaluation via ePO console); no permanent free tier |
| **[Forcepoint DLP](https://www.forcepoint.com/)** | **~$2.45B** Valuation (Francisco Partners; G2CI unit spun to TPG) | Unified DLP across endpoint, network, email, and cloud. Includes 1,800+ prebuilt regional compliance classifiers, Risk-Adaptive Protection, and Generative AI monitoring. | **$50.00/user/year** (~$4.17/user/month entry-tier compliance bundle) | **30-day full-access trial** (evaluation portal with full policy features enabled); no permanent free tier |
| **[Digital Guardian](https://www.digitalguardian.com/)** | **~$800M** Revenue (Fortra) | Deep endpoint visibility agent for Windows, macOS, and Linux. Kernel-level event monitoring, automated tag-based classification, and insider risk detection. | **$15.00/user/year** (approx. $1.25/user/month, minimum 1,000-seat threshold) | **30-day proof of concept (POC)** (guided 2–4 week evaluation arranged with sales); no permanent free tier |
| **[Nightfall AI](https://www.nightfall.ai/)** | **~$60.3M** Funding Raised | AI-native DLP utilizing transformer-based detectors (over 95% precision) to discover and prevent PII/secret exfiltration across endpoints, SaaS apps, and GenAI prompts. | **$58.00/user/year** (~$4.83/user/month for SaaS/Cloud baseline; endpoints at $140.00/user/year) | **7-day proof of value trial** (with complimentary security risk assessment) plus **Free developer API tier** (scans up to 3 GB/month free) |

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
