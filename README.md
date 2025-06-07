# Detecting and Preventing Phishing Attacks on Health Workers through Network Traffic Monitoring and Detection

This project aims to protect healthcare workers, especially in underserved populations, from phishing attacks through a custom-built detection tool and secure network infrastructure. It combines technical countermeasures with staff training to prevent incidents like ransomware.

## Problem Statement
Phishing attacks on healthcare workers are on the rise, especially during crises like pandemics. Attackers exploit urgency to steal credentials or deploy ransomware. Many health systems lack phishing protection at the network level, and staff are often untrained in identifying phishing attempts.

## Scope and Objectives

### Scope
- Build an email-based phishing detection system (CLI and web).
- Focus on underserved healthcare environments.

### Objectives
- Detect phishing in .txt/.eml/.html emails.
- Use signature + heuristic detection.
- Secure inbox scanning with OAuth.
- Real-time alerts and reporting.
- Network hardening (VLAN, firewalls).
- Deliver staff phishing awareness training.

## Research and Case Study

### Rhysida Ransomware Attack

In August 2023, Rhysida ransomware hit a healthcare provider with 16 hospitals and 165+ clinics. The attack used a phishing email as entry, leading to encrypted systems and healthcare disruption.

### Indicators of Compromise (IoCs)
- File Hashes (VirusTotal checked)
![Data Professional Breakdown](https://github.com/Kelvinchuks/Phishing-Detection-for-Health-Workers/blob/Kelvinchuks/IOC_VirusTotal.PNG)
- File extensions changed to `.rhysida`
- Use of ChaCha20 and 4096-bit RSA encryption

### Data Sources
- HC3
- CISA
- VirusTotal
- Socradar.io
- OWASP
- MITRE CVE Database

## Solution Design

- **Phishing Detection Engine**: CLI and web app using signature + heuristic scanning.
- **Live Inbox Scanning**: IMAP with OAuth authentication.
- **Alerting System**: Real-time notifications for phishing detections.
- **Secure Storage**: Auth-protected JSON/CSV reports saved in a database.
- **User Interface**: Flask web app for non-technical users.

## Implementation Timeline

| Phase          | Description                                               | Duration     |
|----------------|-----------------------------------------------------------|--------------|
| Planning       | Requirements, case studies                                | 2–3 weeks    |
| Development    | CLI + Flask app, detection logic                          | 6–8 weeks    |
| Network Setup  | VLANs, firewalls, VPNs, server hardening                  | 3–4 weeks    |
| Integration    | Link inbox, alerts, database                              | 3–4 weeks    |
| Training       | Phishing awareness per NIST PR.AT-1                       | 2–3 weeks    |
| Testing        | Simulations and failover tests                            | 1–2 weeks    |
| Go-Live        | Deploy, monitor, handover                                 | 1–2 weeks    |

## References

- [HC3 - Rhysida Ransomware Report](https://www.hhs.gov/sites/default/files/rhysida-ransomware-hc3-analyst-note.pdf)
- [CISA Advisory on Rhysida](https://www.cisa.gov/news-events/cybersecurity-advisories/aa23-319a)
- [VirusTotal Report](https://www.virustotal.com/)
- [OWASP Phishing Detection Guide](https://owasp.org/www-community/Phishing)
- [NIST Cybersecurity Framework](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.04162018.pdf)
