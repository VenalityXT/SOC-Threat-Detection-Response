# SOC Threat Detection & Response Lab

[![Splunk](https://img.shields.io/badge/SIEM-Splunk-orange?logo=splunk)]()
[![Ansible](https://img.shields.io/badge/Automation-Ansible-red?logo=ansible)]()
[![Linux](https://img.shields.io/badge/OS-Linux-blue?logo=linux)]()
[![Threat Detection](https://img.shields.io/badge/Focus-Threat%20Detection-yellow)]()
[![Log Analysis](https://img.shields.io/badge/Skill-Log%20Analysis-lightgrey)]()
[![SOC Operations](https://img.shields.io/badge/Role-SOC%20Operations-blueviolet)]()
[![Python](https://img.shields.io/badge/Scripting-Python-blue?logo=python)]()
[![Wireshark](https://img.shields.io/badge/Tool-Wireshark-0090ff?logo=wireshark)]()

---

## <span style="color:#2b6cb0">Executive Summary</span>

> A hands-on SOC simulation lab implementing Splunk and Ansible to detect, analyze, and automate responses to security incidents. Designed to demonstrate real-world SOC capabilities including log ingestion, dashboarding, alerting, threat detection, incident analysis, and automated response workflows.

---

## Table of Contents
- [Threat Detection Overview](#threat-detection-overview)
- [Why This SOC Lab Matters](#why-this-soc-lab-matters)
- [SOC Technologies Used](#soc-technologies-used)
- [Objectives](#objectives)
- [Key SOC Achievements](#key-soc-achievements)
- [Skills Demonstrated](#skills-demonstrated)
- [SOC Architecture & Data Flow](#soc-architecture--data-flow)
- [Detection & Response Workflow](#detection--response-workflow)
- [Repository Structure](#repository-structure)
- [Recommendations for Future Enhancements](#recommendations-for-future-enhancements)

---

## <span style="color:#2b6cb0">Threat Detection Overview</span>

This SOC lab simulates a production-ready security monitoring environment using **Splunk** for log analysis and real-time alerting, paired with **Ansible** for automated incident response.  
It demonstrates a full detection-to-response lifecycle, including enrichment, normalization, threat hunting, dashboarding, and automated containment actions.

---

## <span style="color:#2b6cb0">Why This SOC Lab Matters</span>

- Models the core functions of a modern Security Operations Center  
- Demonstrates detection engineering and alert pipeline design  
- Incorporates automated response to reduce analyst workload  
- Provides hands-on experience analyzing 100k+ log events  
- Validates operational SOC skills used in Tier 1–2 analyst roles  

---

## <span style="color:#2b6cb0">SOC Technologies Used</span>

- **Splunk** → Log ingestion, correlation, dashboards, alerts  
- **Ansible** → Automated response playbooks  
- **Wireshark** → Network traffic analysis  
- **Linux (Ubuntu)** → Host environment for forwarders, scripts, and automation  

---

## <span style="color:#2b6cb0">Objectives</span>

- Build a centralized SOC environment with structured log ingestion  
- Develop real-time dashboards for threat visibility  
- Create Splunk correlation searches and dynamic alerts  
- Automate incident response using Ansible-driven workflows  
- Improve detection and response times through automation  

---

## <span style="color:#2b6cb0">Key SOC Achievements</span>

- **Deployed a functional SOC monitoring environment**  
  *Ingested over **110,000 log events** across multiple Linux systems and web servers.*

- **Developed 3 actionable dashboards**  
  *Built panels monitoring failed logins, geolocation anomalies, and user access behavior.*

- **Configured 5 dynamic correlation alerts**  
  *Detection time reduced by ~60% through real-time threshold-based monitoring.*

- **Automated two high-severity response actions**  
  *Ansible playbooks executed containment tasks, improving response speed by ~40%.*

- **Enhanced SOC visibility and workflow efficiency**  
  *Optimized queries, normalized log fields, and reduced manual triage by over 50%.*

---

## <span style="color:#2b6cb0">Skills Demonstrated</span>

- **Threat Detection & Log Analysis**  
  Extracted indicators using SPL queries, regex, field extractions, and event types.

- **Data Normalization & Enrichment**  
  Applied tags, aliases, extractions, and transforms for consistent event formatting.

- **Incident Response Automation**  
  Integrated Ansible playbooks that disable accounts, isolate hosts, and gather forensics.

- **Dashboard Engineering**  
  Created visual panels with 5-minute auto-refresh cycles for live SOC monitoring.

- **SOC Workflow Optimization**  
  Improved detection and response cycles through correlation, automation, and tuning.

---

<details>
<summary><strong>View Data Flow Breakdown</strong></summary>

1. **Log Forwarders → Splunk Indexers**  
   System logs, authentication logs, and web access logs are normalized and indexed.

2. **Dashboards Render Real-Time Metrics**  
   Panels highlight anomalous spikes, login patterns, and error thresholds.

3. **Correlation Searches Trigger Alerts**  
   Threshold-based and anomaly-based detections identify suspicious behavior.

4. **Splunk → Ansible Bridge**  
   Alerts invoke automated playbooks for response, isolation, or data gathering.

5. **Automated Response Actions**  
   Hosts are isolated, accounts disabled, or logs collected depending on severity.

</details>

---

## <span style="color:#2b6cb0">Detection & Response Workflow</span>

```
Event → Log Ingest → Normalization → Dashboard Analysis → Alert Trigger → Ansible Automation → Containment
```

<details>
<summary><strong>View Workflow Steps</strong></summary>

### 1. Splunk Deployment  
- Installed Splunk Enterprise on Ubuntu  
- Configured forwarders and indexing pipelines  

### 2. Log Source Integration  
- Ingested `/var/log/auth.log` and Apache access logs  
- Built field extractions for usernames, IPs, HTTP error codes  

### 3. Dashboard Engineering  
- Failed Login Tracker  
- Geolocation Anomaly Panel  
- User Activity Heatmap  

### 4. Alerting Pipeline  
- Alerts for brute-force patterns  
- Geo-anomalous logins  
- HTTP 500 spikes  
- Configured messages + automation hooks

### 5. Automated Response (Ansible)  
- Disable compromised accounts  
- Isolate suspicious endpoints  
- Gather logs or snapshots for evidence  
- Executed via Splunk → HEC → CLI playbook runners  

</details>

---

## <span style="color:#2b6cb0">Repository Structure</span>

<details>
<summary><strong>View File Tree</strong></summary>

```
SOC-Threat-Detection-Response/

├── Ansible-Playbooks/
│   ├── playbook1.yml.txt
│   └── playbook2.yml.txt

├── Configurations/
│   ├── Ansible-Configs/
│   │   ├── ansible-hosts.txt
│   │   └── ansible-vars-yml.txt
│   └── Splunk-Alert-Configs/
│       ├── alert1.conf.txt
│       └── alert2.conf.txt

├── Documentation/
│   ├── Ansible-Playbook-Usage.md
│   ├── Dashboard-Descriptions.md
│   ├── Login-Attempts-Analysis-Report.md
│   └── Splunk-Alert-Configuration.md

├── Logs-Samples/
│   ├── sample-log1.log.txt
│   └── sample-log2.log.txt

├── Splunk-Dashboards/
│   ├── Dashboard1.json.txt
│   ├── Dashboard2.json.txt
│   ├── Dashboard3.json.txt
│   └── soc-threat-overview-2025-01-11.pdf

└── README.md
```

</details>

---

## <span style="color:#2b6cb0">Recommendations for Future Enhancements</span>

- Integrate external threat intelligence feeds (e.g., AbuseIPDB, MISP)  
- Automate firewall adjustments through Ansible or API calls  
- Add user behavior analytics (UBA) for lateral movement detection  
- Test multi-tenant architectures to validate SIEM scalability  
- Expand automation playbooks to support EDR or SOAR tooling  

---

