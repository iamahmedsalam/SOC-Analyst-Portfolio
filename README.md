# SOC Analyst Portfolio - Ahmed Salam

Building hands-on cybersecurity skills with CompTIA Security+ as my foundation — this portfolio features a multi-agent Wazuh SOC lab and projects demonstrating real-world SOC Analyst capabilities.

## Overview

This repository documents my journey from an unemployed beginner in IT and cybersecurity to developing practical skills for a SOC Analyst role. Starting with foundational certifications like Security+, I'm focusing on hands-on projects to showcase my ability to perform real job tasks, such as threat detection, incident response, and endpoint monitoring. The goal is to solve problems, achieve results, and stand out by demonstrating I can handle SOC duties better both independantly and collaboratively beyond the entry-level expectations.

## Phase 1-3: Home SOC Lab with Wazuh

![SOC Lab Architecture](soc-lab-architecture.png)

- **Goal**: Built a complete SOC simulation environment from scratch using VirtualBox to monitor threats and generate alerts.
- **Tech Stack**: Ubuntu Server 24.04 LTS for Wazuh SIEM (all-in-one: manager, indexer, dashboard), Windows 11 Enterprise Evaluation endpoint with Sysmon for enhanced logging, multi-agent enrollment.
- **Outcomes**: 
  - Wazuh dashboard live on HTTP port 5601 (HTTP fallback for lab simplicity; HTTPS configurable).
  - Internal manager agent (ID 000) self-monitoring Ubuntu server, visible via filter `agent.id:000`.
  - Windows endpoint agent enrolled (ID 001 or similar), active and sending logs.
  - Events flowing from Sysmon (process creation, file changes, network connections) and generated activities (e.g., brute-force simulations, PowerShell execution).
- **Challenges Solved**: 
  - Config validation errors and deprecated keys in opensearch_dashboards.yml.
  - Port binding issues (e.g., setcap for Node.js on low ports).
  - SSL to HTTP fallback for reliable VM access.
  - Agent enrollment hiccups (port reachability, service restarts).
- **Screenshots**: See the `/screenshots` folder, organized by phase (Phase01, Phase02, Phase03). Key highlights include VM creation, Wazuh installation output, Sysmon events, multi-agent dashboard views.
- **Video Walkthrough**: [Loom link here] (coming soon — quick tour of lab setup, agent enrollment, and live events).

## Next Steps

- Phase 4: Core SOC skill showcases (e.g., brute-force detection & response, phishing investigation, network traffic analysis, custom detection rules, incident response playbook).
- Phase 5: Full portfolio polish, personal website launch, and job applications.

Feedback and suggestions welcome — let's connect!

## Connect with Me :

- **LinkedIn**: [Ahmed Salam](https://linkedin.com/in/ahmedsalamnyc) – For professional networking and cybersecurity discussions.
- **X (Twitter)**: [@imahmedsalam](https://x.com/imahmedsalam) – Follow for real-time updates on my SOC journey and tips.
- **GitHub**: [imahmedsalam](https://github.com/imahmedsalam) – Star or fork this repo for more projects.
- **Personal Website** (coming soon): [ahmedsalam.com](https://ahmedsalam.com) – Detailed write-ups and portfolio expansions.
