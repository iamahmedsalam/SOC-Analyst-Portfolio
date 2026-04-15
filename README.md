# SOC Analyst Portfolio — Ahmed Salam

**Aspiring AI-Augmented SOC Analyst** building real detection capabilities through hands-on labs, custom SIEM rules, and documented incident response.

> CompTIA Security+ Certified | TryHackMe Top 2% (132 rooms, 30 badges) | SOC Level 1 Certified

🌐 **Portfolio:** [iamahmedsalam.com](https://iamahmedsalam.com)

---

## Projects

### 🛡️ [Home SOC Lab v2.0](https://github.com/iamahmedsalam/home-soc-lab)

A production-grade SOC home lab — 4-VM environment with custom detection engineering, real attack simulation, and professional incident response documentation.

**What I built:**
- Multi-platform Wazuh SIEM (v4.14.4) monitoring Windows 11 + Ubuntu endpoints
- 10 custom detection rules mapped to MITRE ATT&CK techniques
- Atomic Red Team adversary simulation — 8/10 techniques detected
- 3 professional incident reports with full forensic evidence from real alerts

**Key technical details:**
- Sysmon v15.15 with Olaf Hartong modular config for endpoint telemetry
- PCRE2 regex with case-insensitive flags for evasion-resistant detection
- Host-Only networking (192.168.56.0/24) for stable lab communication
- Discovered Wazuh 4.14.4 uses `sysmon_eid1_detections` group naming (not older `sysmon_event1` format)

**Detection coverage:** T1059.001, T1003.001, T1547.001, T1136.001, T1070.001, T1055, T1105, T1021.001, T1083

| | |
|---|---|
| **Repo** | [github.com/iamahmedsalam/home-soc-lab](https://github.com/iamahmedsalam/home-soc-lab) |
| **Detection Rules** | [local_rules.xml](https://github.com/iamahmedsalam/home-soc-lab/blob/main/detection-rules/local_rules.xml) |
| **Incident Reports** | [IR-001](https://github.com/iamahmedsalam/home-soc-lab/blob/main/incident-reports/IR-001-powershell-encoded-command.md) · [IR-002](https://github.com/iamahmedsalam/home-soc-lab/blob/main/incident-reports/IR-002-registry-run-key-persistence.md) · [IR-003](https://github.com/iamahmedsalam/home-soc-lab/blob/main/incident-reports/IR-003-windows-event-log-cleared.md) |
| **Simulation Results** | [Full detection matrix](https://github.com/iamahmedsalam/home-soc-lab/blob/main/attack-simulations/simulation-results.md) |

---

### 🔰 [Incident Response Playbooks + Live Drills](https://github.com/iamahmedsalam/incident-response-playbooks)

5 professional IR playbooks validated through live attack drills — proving the full SOC L1 workflow from alert triage through investigation, containment, and documentation.

**What I built:**
- 5 reusable playbooks covering Execution, Credential Access, Persistence, Defence Evasion, and Command & Control
- 5 live drill reports with real Wazuh alert artifacts, timestamps, and forensic evidence
- 1 new detection rule (Rule 100011 — SSH Brute Force) expanding coverage to Linux
- 12 detection improvement recommendations discovered through hands-on investigation

**Key findings:**
- MTTD consistently < 3 seconds across all 5 drills
- Identified 2 LOLBINs (reg.exe, certutil.exe) used in attack simulations
- Recovered full multi-stage attack timeline from SIEM after local log destruction
- Caught malware dropper before execution — quarantined with hash preserved

| | |
|---|---|
| **Repo** | [github.com/iamahmedsalam/incident-response-playbooks](https://github.com/iamahmedsalam/incident-response-playbooks) |
| **Playbooks** | [PB-001](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/playbooks/PB-001-powershell-execution.md) · [PB-002](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/playbooks/PB-002-ssh-brute-force.md) · [PB-003](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/playbooks/PB-003-registry-persistence.md) · [PB-004](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/playbooks/PB-004-event-log-cleared.md) · [PB-005](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/playbooks/PB-005-malware-dropper-temp.md) |
| **Live Drills** | [Drill 001](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/live-drills/drill-001-powershell.md) · [Drill 002](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/live-drills/drill-002-ssh-bruteforce.md) · [Drill 003](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/live-drills/drill-003-registry-persistence.md) · [Drill 004](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/live-drills/drill-004-event-log-cleared.md) · [Drill 005](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/live-drills/drill-005-malware-dropper.md) |
| **Detection Improvements** | [Rule tuning log](https://github.com/iamahmedsalam/incident-response-playbooks/blob/main/detection-improvements/rule-tuning-log.md) |

---

### 🔬 Home SOC Lab v1.0 (Foundation)

The original 2-VM lab that started it all — Wazuh Manager + Windows 11 endpoint with Sysmon. Deployed from scratch, troubleshot real issues (config validation, port binding, SSL fallback, agent enrollment), and documented everything. This became the foundation for the v2.0 upgrade.

**Architecture:**

![Home SOC Lab v1.0 Architecture](Soc-Lab-Architecture.png)

**Technologies:** Wazuh, Sysmon (SwiftOnSecurity config), VirtualBox, Ubuntu 24.04 LTS, Windows 11

---

## Certifications

| Certification | Platform | Status |
|---|---|---|
| CompTIA Security+ | CompTIA | ✅ Certified (Active) |
| SOC Level 1 | TryHackMe | ✅ Completed (April 2026) |

---

## TryHackMe Progress

| Metric | Value |
|---|---|
| Global Ranking | **Top 2%** |
| Rooms Completed | 132 |
| Badges Earned | 30 |
| Learning Path | SOC Level 1 (completed) |

---

## Skills Demonstrated

**Detection Engineering:** Custom Wazuh rule authoring (11 rules), PCRE2 regex, MITRE ATT&CK mapping, Sysmon event ID analysis, `if_sid` vs `if_group` chaining, XML validation workflow

**Incident Response:** 5 professional IR playbooks, live drill execution, alert triage decision trees, forensic artifact extraction, attack chain correlation, evidence-preserving containment (quarantine vs delete)

**Attack Simulation:** Atomic Red Team execution, Hydra brute force, purple team methodology, detection gap analysis, OS hardening assessment (Credential Guard, LSA Protection), LOLBIN identification (reg.exe, certutil.exe)

**SIEM Operations:** Wazuh deployment and configuration, multi-platform agent enrollment, custom dashboard creation, centralised log forwarding architecture, SIEM evidence recovery after local log destruction

**Endpoint Monitoring:** Sysmon configuration and tuning, Windows Event Log analysis, Linux auth.log analysis, process creation / registry / file creation / process access event correlation

---

## What's Next

- AI-Augmented Alert Triage — LLM integration with Wazuh pipeline
- Threat Intel Integration — MISP/OTX feed enrichment
- HackTheBox CJCA certification
- Splunk specialization (Core Power User + CDA)

---

## Connect

- 🌐 Portfolio: [iamahmedsalam.com](https://iamahmedsalam.com)
- 💼 LinkedIn: [Ahmed Salam](https://www.linkedin.com/in/ahmedsalamnyc)
- 🐙 GitHub: [iamahmedsalam](https://github.com/iamahmedsalam)
- ✉️ Email: [contact@iamahmedsalam.com](mailto:contact@iamahmedsalam.com)
