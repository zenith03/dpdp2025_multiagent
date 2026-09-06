# DPDP 2025 Privacy Policy Compliance Auditor

## Overview
This project is a multi-agent AI framework designed to automatically audit privacy policies for readiness against India's **Digital Personal Data Protection Act (DPDPA), 2023** and the **DPDP Rules, 2025**. 

Built on the Neuro SAN Studio framework, this system utilizes a 5-agent pipeline powered by `gemini-1.5-flash` to ingest policy URLs, extract exact verbatim evidence, evaluate statutory compliance, and synthesize an auditable remediation report.

## Note to Evaluators
My core architectural work, multi-agent orchestration, and legal prompt engineering for this capstone can be found exclusively in:
👉 `registries/basic/dpdp2025_agent.hocon`

## System Architecture
The auditing network consists of 5 specialized agents:
1. **DPDPAuditor:** The lead orchestrator that manages the workflow.
2. **WebIngestionAgent:** Navigates to the supplied URL, scrapes the webpage, and normalizes the raw text.
3. **LegalEvidenceAgent:** Maps text to DPDP rules (Notice, Consent, Breach, Security, etc.) and extracts exact evidence clauses.
4. **ComplianceEvaluator:** Grades the extracted clauses against strict statutory thresholds (Compliant, Needs Improvement, Action Required).
5. **ReportSynthesizer:** Calculates the final deterministic score and generates a highly structured Markdown report.

## How to Run the Project Locally

**1. Clone the repository and navigate into it:**
```bash
git clone [https://github.com/YourUsername/dpdp-2025-compliance-auditor.git](https://github.com/YourUsername/dpdp-2025-compliance-auditor.git)
cd dpdp-2025-compliance-auditor