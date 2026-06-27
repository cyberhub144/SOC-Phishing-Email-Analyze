# 🛡️ SOC Phishing Email Analyzer — Project 4

<div align="center">

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-00ff41?style=for-the-badge&logo=shield&logoColor=white)
![SOC](https://img.shields.io/badge/Role-SOC_Analyst-0a0a0a?style=for-the-badge&logo=datadog&logoColor=00ff41)
![HTML](https://img.shields.io/badge/Built_With-HTML%20%7C%20CSS%20%7C%20JS-00aaff?style=for-the-badge&logo=html5&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-00ff41?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**A real-world SOC analyst tool for detecting and analyzing phishing emails using threat intelligence platforms.**

[🔍 Live Demo](#live-demo) · [📖 How It Works](#how-it-works) · [🚀 Features](#features) · [🛠️ Tools Used](#tools-used) · [📋 Resume Point](#resume-point)

</div>

---

## 📌 Project Overview

This project simulates how a **Security Operations Center (SOC) Analyst** investigates suspicious emails. Built as **Project 4** of my cybersecurity portfolio, it covers the full phishing investigation workflow — from raw email header parsing to IOC extraction and threat intelligence lookup.

The tool features a **cyber-terminal dark UI** with matrix rain effects, real-time threat scoring, and direct integration links to industry-standard threat intel platforms like VirusTotal, URLScan, and MXToolbox.

---

## 🎯 Objective

> Analyze suspicious emails like a SOC analyst — extracting indicators of compromise (IOCs), checking sender reputation, validating authentication headers, and producing a structured findings report.

---

## ✨ Features

### 🔬 Analysis Engine
- **Email header parser** — extracts From, Reply-To, Received, X-Originating-IP, Authentication-Results and more
- **SPF / DKIM / DMARC detection** — flags authentication failures instantly
- **IOC extractor** — pulls IPs, URLs, and domains from raw email content
- **Threat scorer** — 0–100 risk score based on weighted detection rules
- **Typosquatting detection** — catches lookalike domains (`paypa1`, `microsofft`, `g00gle`)
- **BEC pattern recognition** — detects wire transfer / bank account fraud language
- **Urgency language detection** — identifies social engineering pressure tactics
- **Bulk mailer fingerprinting** — spots PHPMailer, SendGrid-bulk signatures

### 📊 Findings Report
- Verdict: **Phishing / Suspicious / Clean**
- Threat score bar with color-coded severity
- IOC table with one-click **VirusTotal** and **URLScan.io** lookups
- Red flag breakdown with severity levels (Critical / Warning)
- Parsed header analysis table
- One-click **export to `.txt` report**
- AI-powered full **Incident Response report generation**

### 🧪 Sample Email Library
- PayPal credential harvest (confirmed phishing)
- Microsoft 365 MFA lure (token theft)
- BEC invoice fraud (suspicious)
- GitHub notification (legitimate / clean)

### 🛠️ SOC Toolkit Tab
Direct launch links to all major threat intel platforms with a built-in **quick IOC lookup** field.

---

## 🚀 Live Demo

> **Paste any raw email headers + body → get instant SOC analysis**

```
Clone the repo and open index.html in any browser — no server required.
```

```bash
git clone https://github.com/YOUR-USERNAME/soc-phishing-analyzer.git
cd soc-phishing-analyzer
open index.html
```

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **MXToolbox** | Email header analysis, SPF/DKIM/DMARC validation, IP blacklist check |
| **VirusTotal** | URL, IP, and domain multi-engine reputation scanning |
| **URLScan.io** | Safe URL detonation, screenshot, DOM analysis |
| **AbuseIPDB** | Sender IP reputation and community abuse reports |
| **PhishTank** | Crowdsourced phishing URL database verification |
| **Google Safe Browsing** | Malware and phishing URL check |
| **ICANN Whois** | Domain registration date, registrant, and registrar lookup |

---

## 🔍 How It Works

### Detection Rules & Scoring

| Rule | Score Weight | Severity |
|------|-------------|---------|
| SPF authentication fail | +25 | Critical |
| DKIM missing or failed | +20 | Critical |
| DMARC policy rejected | +15 | Critical |
| Reply-To mismatch from From address | +20 | Critical |
| Typosquatted / lookalike domain | +30 | Critical |
| Credential-harvest URL detected | +25 | Critical |
| Known malicious IP range | +20 | Critical |
| Financial fraud / BEC pattern | +25 | Critical |
| Urgency / fear language | +15 | Warning |
| Bulk mailer signature | +10 | Warning |
| High-risk TLD (.ru/.xyz/.top/.tk) | +15 | Warning |

**Verdict thresholds:**
- 🔴 **60–100** → Phishing detected
- 🟡 **25–59** → Suspicious — further review required
- 🟢 **0–24** → Likely clean

---

## 📁 Project Structure

```
soc-phishing-analyzer/
│
├── index.html          # Full tool — single-file, zero dependencies
├── README.md           # This file
├── samples/
│   ├── phishing-paypal.txt       # Sample phishing email headers + body
│   ├── phishing-microsoft.txt    # MFA lure sample
│   ├── suspicious-bec.txt        # BEC invoice fraud sample
│   └── clean-github.txt          # Legitimate email sample
└── reports/
    └── sample-report.txt         # Example exported SOC findings report
```

---

## 📋 Skills Demonstrated

| Skill | Details |
|-------|---------|
| **Email Security** | Header analysis, SPF/DKIM/DMARC validation, sender verification |
| **IOC Analysis** | Extraction and classification of IPs, URLs, and domains |
| **Threat Intelligence** | Integration with VirusTotal, URLScan, MXToolbox, AbuseIPDB |
| **OSINT** | Domain reputation, WHOIS lookups, IP geolocation analysis |
| **SOC Workflow** | Triage → Analysis → IOC extraction → Report generation |
| **Report Writing** | Structured findings reports with severity classification |

---

## 📄 Resume Point

> **Performed phishing email investigations by analyzing email headers, URLs, sender reputation, and Indicators of Compromise (IOCs) using threat intelligence platforms such as VirusTotal, URLScan.io, MXToolbox, and AbuseIPDB. Identified SPF/DKIM/DMARC failures, typosquatted domains, credential-harvest URLs, and BEC patterns. Documented findings in structured SOC reports.**

---

## 🎓 What I Learned

- How email authentication protocols (SPF, DKIM, DMARC) work and how attackers bypass them
- Identifying typosquatting and lookalike domain techniques used in phishing campaigns
- IOC extraction and enrichment using threat intelligence platforms
- Business Email Compromise (BEC) attack patterns and financial fraud indicators
- Structuring a SOC incident findings report with severity classification
- MITRE ATT&CK techniques: **T1566** (Phishing), **T1078** (Valid Accounts), **T1071** (Application Layer Protocol)

---

## 🔧 How to Use

1. **Open `index.html`** in any modern browser
2. Go to the **Analyze** tab
3. Paste raw email headers into the first field
4. Paste email body into the second field
5. Click **Run SOC scan**
6. Review findings in the **Findings** tab
7. Click **Export report** to save results as `.txt`
8. Use **Full IR report ↗** to generate a complete Incident Response document

> **Tip:** Use the **Samples** tab to load pre-built phishing, suspicious, and clean email examples instantly.

---

## 🧪 Sample Test Case

Paste these headers to test a phishing detection:

```
From: paypal-security@paypa1.com
Reply-To: harvest@collect-data.ru
Received: from mail.paypa1.com (185.220.101.12)
To: john.doe@company.com
Subject: Urgent: Your PayPal account has been limited!
X-Mailer: PHPMailer 5.2.27
X-Originating-IP: 185.220.101.12
Authentication-Results: spf=fail; dkim=fail; dmarc=fail
```

**Expected result:** 🔴 Phishing detected — Score: 95/100 — 6+ red flags

---

## 🌐 Related Projects

- [Project 1 — Network Traffic Analysis](#)
- [Project 2 — Vulnerability Assessment](#)
- [Project 3 — SIEM Log Investigation](#)
- **Project 4 — Phishing Email Analysis ← You are here**
- [Project 5 — Incident Response Simulation](#)

---

## 📬 Connect

**[Your Name]** — Aspiring SOC Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077b5?style=flat-square&logo=linkedin)](https://linkedin.com/in/YOUR-PROFILE)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-212c42?style=flat-square&logo=tryhackme)](https://tryhackme.com/p/YOUR-PROFILE)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/YOUR-USERNAME)

---

## 📜 License

This project is licensed under the **MIT License** — free to use, share, and build upon with attribution.

---

<div align="center">

⭐ **Star this repo if it helped you — it helps others find it too!** ⭐

*Built as part of a hands-on SOC analyst portfolio. All sample emails are fictional and created for educational purposes only.*

</div>
