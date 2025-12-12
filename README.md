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

> A hands-on SOC simulation lab implementing Splunk and Ansible to detect, analyze, and automate responses to security incidents. This lab demonstrates real-world SOC capabilities, including log ingestion, dashboarding, alerting, threat detection, incident analysis, and automated response workflows.

---

## Table of Contents
- [Threat Detection Overview](#threat-detection-overview)
- [Why This SOC Lab Matters](#why-this-soc-lab-matters)
- [SOC Technologies Used](#soc-technologies-used)
- [Objectives](#objectives)
- [Key Problem-Solving Experiences](#key-problem-solving-experiences)
- [SOC Architecture & Data Flow](#soc-architecture--data-flow)
- [Detection & Response Workflow](#detection--response-workflow)
- [Repository Structure](#repository-structure)
- [Recommendations for Future Enhancements](#recommendations-for-future-enhancements)

---

## <span style="color:#2b6cb0">Threat Detection Overview</span>

This SOC lab simulates a production-ready security monitoring environment using **Splunk** for log analysis and real-time alerting, paired with **Ansible** for automated incident response.  
It demonstrates a full detection-to-response lifecycle, including enrichment, normalization, threat hunting, dashboarding, and automated containment actions.

> [!TIP]
> This lab simulates a **real-world SOC environment**, providing practical skills in both **detection engineering** and **incident response automation**.

---

## <span style="color:#2b6cb0">Why This SOC Lab Matters</span>

Building a **Security Operations Center** from scratch provides valuable insights into what a **real SOC** looks like. Here’s why it matters:

- **Hands-on experience**: Working with 100k+ log events mirrors the type of data SOC analysts handle daily.
- **Real-world relevance**: Designed to simulate live, real-time incident detection, it goes beyond theory into **practical application**.
- **Automation in SOC**: Using Ansible to automate response actions frees up analysts for more critical tasks.

Rather than simply watching a tutorial, this lab provides a **learning-by-doing** approach.

---

## <span style="color:#2b6cb0">SOC Technologies Used</span>

This lab integrates multiple technologies to simulate a functioning SOC environment:

- **Splunk** for ingesting logs, building dashboards, and triggering alerts.  
- **Ansible** for automating playbooks and handling incident responses.  
- **Wireshark** for network traffic analysis and packet-level event correlation.  
- **Ubuntu Linux** for system configuration, forwarders, and script execution.

These technologies allow for a **comprehensive** SOC simulation experience.

---

## <span style="color:#2b6cb0">Key Problem-Solving Experiences</span>

<details>
<summary><strong>Problem 1: Handling a Flood of Log Data</strong></summary>

**Challenge:**  
The lab’s early stages revealed how overwhelming **log ingestion** can become with **large volumes** of data — especially when it’s unstructured or lacks critical context.

**Solution:**  
- Configured **custom Splunk queries** to focus on key indicators (failed logins, unusual geo-locations).
- Integrated **Wireshark** to supplement Splunk data and gain deeper visibility into network activity.
</details>

<details>
<summary><strong>Problem 2: Improving Incident Response Efficiency</strong></summary>

**Challenge:**  
Manual response to detected threats was time-consuming and inconsistent. The goal was to improve **response times** and reduce **human error**.

**Solution:**  
- Implemented **Ansible playbooks** to automate critical tasks, such as isolating compromised machines and disabling accounts.
</details>

<details>
<summary><strong>Problem 3: Building Real-Time Dashboards</strong></summary>

**Challenge:**  
Before dashboarding, it was hard to get a comprehensive view of SOC activity, and critical threats would sometimes be missed.

**Solution:**  
- Developed **three dynamic dashboards** to provide real-time visibility into failed login attempts, geolocation anomalies, and user access patterns.
</details>

---

## <span style="color:#2b6cb0">SOC Architecture & Data Flow</span>

<details>
<summary><strong>View Data Flow Breakdown</strong></summary>

- **Log Forwarders → Splunk Indexers:** Normalizes and indexes system and application logs.
- **Dashboards Render Real-Time Metrics:** Visualizes metrics like failed login attempts, geolocation anomalies, and other threshold-based metrics.
- **Correlation Searches Trigger Alerts:** Threshold-based and anomaly-based detections identify suspicious behavior.
- **Splunk → Ansible Bridge:** Alerts trigger automated response playbooks to isolate compromised machines or disable accounts.
- **Automated Response Actions:** Depending on alert severity, tasks like isolation or account disabling are automated, improving containment speed.

</details>

---

## <span style="color:#2b6cb0">Detection & Response Workflow</span>

<img width="1700" height="965" alt="image" src="https://github.com/user-attachments/assets/e13d1799-5a5f-4235-8a26-14bc3cefb149" />

---

## <span style="color:#2b6cb0">Repository Structure</span>

```
SOC-Threat-Detection-Response/

├── Ansible-Playbooks/
│ ├── playbook1.yml.txt
│ └── playbook2.yml.txt

├── Configurations/
│ ├── Ansible-Configs/
│ │ ├── ansible-hosts.txt
│ │ └── ansible-vars-yml.txt
│ └── Splunk-Alert-Configs/
│ ├── alert1.conf.txt
│ └── alert2.conf.txt

├── Documentation/
│ ├── Ansible-Playbook-Usage.md
│ ├── Dashboard-Descriptions.md
│ ├── Login-Attempts-Analysis-Report.md
│ └── Splunk-Alert-Configuration.md

├── Logs-Samples/
│ ├── sample-log1.log.txt
│ └── sample-log2.log.txt

├── Splunk-Dashboards/
│ ├── Dashboard1.json.txt
│ ├── Dashboard2.json.txt
│ ├── Dashboard3.json.txt
│ └── soc-threat-overview-2025-01-11.pdf

└── README.md
```

---

## <span style="color:#2b6cb0">Recommendations for Future Enhancements</span>

- Integrate external threat intelligence feeds (e.g., AbuseIPDB, MISP)  
- Automate firewall adjustments through Ansible or API calls  
- Add user behavior analytics (UBA) for lateral movement detection  
- Test multi-tenant architectures to validate SIEM scalability  
- Expand automation playbooks to support EDR or SOAR tooling  

---

