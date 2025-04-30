# Lumma Stealer - DLL Side-Loading via Click Fix Phishing  
**Event ID:** 316  
**Platform:** LetsDefend.io  
**Date:** April 30, 2025  
**Category:** Email Phishing (Data Leakage)  
**Severity:** Critical  
**Status:** ✅ Closed (True Positive)

---

## Overview
This alert involved a phishing email sent from a spoofed Microsoft domain (`update@windows-update.site`) with the subject line:  
**"Upgrade your system to Windows 11 Pro for FREE."**

The email redirected to a site containing a malicious script associated with the **Lumma Stealer** malware. The connection was allowed by the endpoint.

---

## Key Findings

- **SMTP Address:** `132.232.40.201`  
- **Source Address:** `update@windows-update.site`  
- **Destination:** `dylan@letsdefend.io`  
- **Malicious URL:** `windows-update.site`  
- **Threat Type:** DLL Side-Loading / Data Leakage  
- **Threat Score:** Community ranked the domain 11/97  
- **Malware:** Confirmed via rule SOC338 as Lumma Stealer

---

## Investigation Steps

1. Parsed email header for sender/recipient, subject, and SMTP details.
2. Used threat intel tools to validate domain reputation.
3. Identified IOC match for Lumma Stealer.
4. Tagged alert as **True Positive**.
5. Submitted playbook steps and artifacts (email sender, domain, URL).
6. Documented findings in analyst note.

---

## Closing Note
Confirmed **True Positive**. Domain `windows-update.site` is known for Lumma Stealer distribution. Alert closed after validating all IOCs and referencing reputation databases.

---

## Skills Demonstrated
- Phishing Email Analysis  
- Threat Intelligence Validation  
- IOC Extraction & Correlation  
- SIEM Alert Investigation  
- MITRE ATT&CK Mapping (T1566 - Phishing, T1055.001 - DLL Side-Loading)
