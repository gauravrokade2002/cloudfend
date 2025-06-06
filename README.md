# 🌩️ Cloud Security Management & Threat Mitigation System in GCP

## Overview

**Cloud Security Management & Threat Mitigation System in GCP** is a comprehensive solution designed to monitor, secure, and defend cloud infrastructure hosted on **Google Cloud Platform (GCP)**. It integrates native GCP security services with custom monitoring, threat detection, and automated response mechanisms to protect cloud resources from evolving cyber threats.

---

## 🔐 Key Features

* **Security Monitoring & Logging**

  * Stackdriver (Cloud Monitoring, Logging, Error Reporting)
  * VPC Flow Logs, Audit Logs, Cloud Armor logs

* **Threat Detection**

  * Integration with **Google Cloud Security Command Center (SCC)**
  * Detection of misconfigurations, vulnerabilities, and suspicious activity

* **Incident Response & Mitigation**

  * Automated policy-based responses using Cloud Functions and Pub/Sub
  * Threat remediation workflows integrated with Security Command Center

* **IAM & Policy Management**

  * Automated least-privilege IAM policy enforcement
  * Policy violations alerts using Cloud Asset Inventory and Forseti Security

* **Network & Application Security**

  * Cloud Armor for DDoS protection
  * Firewall policy enforcement
  * HTTPS Load Balancing and SSL management

---

## 🛠️ Architecture

The system architecture includes:

* **GCP Security Tools**: Security Command Center, Cloud Armor, IAM, VPC Service Controls
* **Monitoring & Alerting**: Cloud Monitoring, Cloud Logging, Pub/Sub
* **Automation**: Cloud Functions, Cloud Scheduler
* **Optional**: Integration with third-party SIEMs or ticketing systems

---

## 🚀 Getting Started

### Prerequisites

* GCP Project with billing enabled
* Access to Security Command Center (Standard or Premium tier)
* Enable required APIs:

  * `securitycenter.googleapis.com`
  * `logging.googleapis.com`
  * `monitoring.googleapis.com`
  * `cloudfunctions.googleapis.com`



## 📊 Dashboard & Reporting

* Security dashboards available in GCP Console → Security Command Center
* Custom dashboards in **Looker Studio** or **Grafana** (optional)
* Scheduled email reports via Cloud Scheduler & Pub/Sub

---

## 🧪 Testing & Validation

* Simulate threats using [GCP Security Scenarios](https://cloud.google.com/security-command-center/docs/how-to-simulate-findings)
* Validate mitigation via audit logs and automatic function execution


## ✅ Best Practices Followed

* Principle of Least Privilege (PoLP)
* Defense in Depth
* Secure defaults
* Continuous monitoring and logging
* Automated remediation

---

## 🧩 Future Improvements

* ML-based anomaly detection
* Integration with Chronicle or third-party SIEMs
* Support for multi-cloud environments (e.g., AWS, Azure)

---

## 🧑‍💻 Contributors

* Gaurav Rokade rokadegaurav03@gmail.com


---

## 📄 License

This project is licensed under the gujaratuniversity.ac.in. 


