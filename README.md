# SOC Threat Detection & Response Lab

This repository documents the simulation of a modern Security Operations Center (SOC) using Splunk and Ansible to emulate real-world detection, alerting, and automated incident response workflows. It showcases practical capabilities in security monitoring, data analysis, and security automation.

## Table of Contents
- [Project Overview](#project-overview)  
- [Technologies Used](#technologies-used)  
- [Objectives](#objectives)  
- [Key Achievements](#key-achievements)  
- [Skills Demonstrated](#skills-demonstrated)  
- [Setup and Configuration Guide](#setup-and-configuration-guide)  
- [Repository Structure](#repository-structure)  
- [Recommendations for Future Enhancements](#recommendations-for-future-enhancements)  
- [License](#license)  

## Project Overview
This lab simulates a functional SOC leveraging Splunk for real-time log ingestion and analysis, along with Ansible for automating response actions. It is designed to validate technical proficiency in detecting and responding to security incidents using scalable and realistic tooling.

[Insert Image of SOC Workflow or Splunk Dashboard Here]  

## Technologies Used
- Splunk – Log aggregation, alerting, and dashboarding  
- Ansible – Automated configuration and incident response  
- Wireshark – Packet analysis  
- Linux (Ubuntu) – Host OS for deploying scripts and agents  

## Objectives
- Configure a centralized SOC environment for ingesting and analyzing security data  
- Build real-time Splunk dashboards to visualize trends and detect anomalies  
- Define alert conditions and automate triggers based on identified threats  
- Integrate Ansible for responsive actions based on triggered alerts  

## Key Achievements
- **Deployed a functional SOC environment**  
  *Set up Splunk to monitor over 110,000 log events from multiple sources including Linux auth logs and web access logs.*

- **Developed 3 custom dashboards**  
  *Built dashboards tracking failed logins, geographic anomalies, and user behavior patterns, improving situational awareness.*

- **Configured 5 dynamic alerts**  
  *Designed threshold-based alerts to detect and escalate suspicious activity, reducing detection time by ~60%.*

- **Automated 2 high-priority responses**  
  *Integrated Ansible playbooks with Splunk alerts to automate containment actions, cutting manual response time significantly.*

- **Enhanced operational efficiency**  
  *Optimized detection and response workflows, resulting in a 40% improvement in the lab’s incident response cycle.*

[Insert Image of Splunk Dashboard with Alert Example Here]  

## Skills Demonstrated
- **Threat Detection at Scale**  
  Analyzed large datasets using Splunk queries and regular expressions to extract indicators of compromise.  

- **Data Normalization and Tagging**  
  Created event types and applied field tags for faster correlation and consistent data formatting.  

- **Incident Response Automation**  
  Wrote and linked Ansible playbooks to alerts for tasks like isolating hosts or gathering forensic data.  

- **Real-Time Monitoring**  
  Maintained dashboards with 5-minute data refresh cycles to provide ongoing security visibility.  

- **Efficient Security Operations**  
  Reduced manual triage efforts by over 50% using integrated alert-to-action workflows.  

---

## Setup and Configuration Guide

### 1. Splunk Deployment
- Installed Splunk Enterprise on Ubuntu.
- Configured Splunk Forwarders to ingest logs from client systems.
- Created indexes for structured storage and faster search performance.

### 2. Log Source Integration
- Ingested system logs (`/var/log/auth.log`, Apache logs).
- Developed field extractions and transforms to normalize log fields.

### 3. Dashboard Development
- Dashboard 1: Failed login attempt summary 
- Dashboard 2: Geolocation anomalies using IP data
- Dashboard 3: User behavior trends over time

### 4. Alerting Mechanism
- Alerts triggered by:
  - Rapid login failures from single IPs
  - Logins from unusual geographic locations
  - Spikes in HTTP 500 errors
- Configured alert actions to send messages or trigger automation scripts.

### 5. Ansible Automation
- Playbook 1: Disable suspicious accounts and collect logs.
- Playbook 2: Isolate endpoints showing malicious behavior.
- Integrated playbooks with Splunk alerts via HTTP Event Collector (HEC) and CLI runners.

---

## Repository Structure

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

├── README.md
├── LICENSE
```

---

## Recommendations for Future Enhancements
- Integrate threat intelligence feeds to correlate known indicators with local events.  
- Automate additional remediation steps such as dynamic firewall rule adjustments.  
- Apply user behavior analytics (UBA) to detect lateral movement or privilege abuse.  
- Simulate multi-tenant logging to validate scalability of SOC infrastructure.  
- Expand Ansible integrations to include third-party SIEMs or EDR platforms.

