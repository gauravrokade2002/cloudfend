# 🛡️ Security Command Center – GCP Threat Detection and Mitigation
Skill Badge- https://www.credly.com/badges/179967b1-c0b9-4916-891e-72fe132a2c33

This repository outlines a practical implementation of Google Cloud's **Security Command Center (SCC)** for identifying and mitigating threats and vulnerabilities in a cloud environment. It is designed for cloud security engineers managing enterprise-grade environments with a focus on automation, compliance, and proactive security.

---

## ⚙️ Setup & Configuration

To begin, access the **Security Command Center (SCC)** via the Google Cloud Console and ensure the **time range is set to the last 180 days**. This configuration is crucial for visibility into both current and historical findings.

1. Navigate to `Security > Security Command Center > Findings`
2. In the time range dropdown, select **Last 180 days**
3. Review any active findings and logs

---

## 🔕 Muting Noisy or Non-actionable Findings

Not all findings require attention. To reduce noise and improve focus, SCC allows you to create **mute rules**. These can be used to suppress findings that are irrelevant or expected in your environment.

Examples include:

* Findings related to disabled **VPC Flow Logs**
* Findings for **disabled audit logs**
* Findings regarding **admin-level service accounts**

To mute these:

* Go to the **Mute Rules** section within SCC
* Use filters (e.g., `category = "FLOW_LOGS_DISABLED"`) to define matching findings
* Apply appropriate labels and descriptions for clarity

---

## 🔐 Addressing High-Risk Vulnerabilities

Critical issues such as open SSH (port 22) or RDP (port 3389) to the public internet should be remediated immediately.

Steps:

* Open **VPC > Firewall Rules**
* Identify rules allowing `0.0.0.0/0` access on these ports
* Edit the rules to restrict access using Google IAP IP ranges (`35.235.240.0/20`) or internal IP ranges as needed
* Save and verify the rule has taken effect via SCC findings

This action aligns with least-privilege and zero-trust network design.

---

## 🌐 Scanning Applications for Vulnerabilities

Use **Web Security Scanner** to test for vulnerabilities in web applications running in your environment.

Steps:

1. Locate the Compute Engine instance hosting the app
2. Edit the instance and reserve a **static external IP address**
3. Confirm the app is accessible via `http://<STATIC_IP>:8080`
4. Open **Web Security Scanner** and create a new scan targeting the app URL
5. Monitor the scan results for any security alerts or misconfigurations

This is especially useful for detecting XSS, outdated libraries, and open directories in real-time.

---

## 📤 Exporting Findings for Audit and Compliance

To retain a historical record of findings for auditing purposes:

1. Create a **Google Cloud Storage** bucket with a unique name like `scc-export-bucket-<unique-id>`
2. Use **SCC's export feature** to output findings to this bucket
3. Choose **JSONL** as the format for compatibility with analytics tools
4. Set time range to **All time** and filename to `findings.jsonl`

This provides a secure and durable record for future forensic analysis or compliance reporting.

---

## 📘 Best Practices

* Always **review and update mute rules** periodically to ensure they still align with security policies
* **Restrict public access** unless absolutely necessary
* Use **labels and annotations** to track ownership and context around findings
* Leverage **Cloud Logging** and **Monitoring** to create alerting pipelines
* Use **IAM roles** with least-privilege principle to control access to SCC

---

## 📎 Additional Tools

* **Cloud Functions** for auto-remediation of common findings
* **Pub/Sub** for real-time alert streaming
* **BigQuery** for advanced querying of exported SCC data
* **Looker Studio** or **Grafana** for dashboarding and visualization

---

## ✅ Summary

This project demonstrates the application of Google Cloud's native tools to secure a cloud environment through the Security Command Center. From identifying vulnerabilities to muting irrelevant noise and ensuring long-term auditability, SCC enables proactive, automated, and scalable cloud security operations.

---

Let me know if you'd like a CLI-based version, Terraform automation script, or architecture diagram added!


## 🧑‍💻 Contributors

* Gaurav Rokade rokadegaurav03@gmail.com
GCP- https://www.cloudskillsboost.google/public_profiles/d6300a7b-a248-49ca-a295-7c3388c94f0e


---

## 📄 License

This project is licensed under the gujaratuniversity.ac.in. 


