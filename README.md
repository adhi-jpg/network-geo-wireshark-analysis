# Network Geo Location Analysis Using Wireshark Packet Capture

## 📌 Project Overview

This project demonstrates the detection and analysis of a TCP SYN Flood attack using Wireshark packet capture and IP geolocation mapping.

The objective was to:

- Simulate a TCP SYN Flood attack using hping3
- Capture and filter suspicious packets using Wireshark
- Analyze TCP flags and packet structure
- Extract attacker IP information
- Perform IP geolocation mapping using the GeoLite2 database

The experiment was conducted in a controlled lab environment for academic cybersecurity study purposes.

---

## 🎯 Objectives

- Simulate SYN flood attack traffic
- Apply Wireshark display filters
- Inspect TCP headers and flags
- Identify suspicious endpoints
- Map IP addresses geographically
- Document findings with screenshots and logs

---

## 🛠 Tools & Software Versions

| Tool | Version | Purpose |
|------|----------|----------|
| Kali Linux | 2023.4 (64-bit) | Attacker Machine |
| hping3 | 3.0.0-alpha-2 | SYN Flood Simulation |
| Windows 10 Pro | 64-bit | Victim Machine |
| Wireshark | 4.0.x | Packet Capture & Analysis |
| GeoLite2 City DB | 2026 Release | IP Geolocation |

---

## 🏗 Architecture

The system architecture consists of:

- Attacker Machine (Kali Linux)
- Victim Machine (Windows 10)
- Packet Capture using Wireshark
- IP Extraction
- GeoLite2 Database Mapping

Architecture diagram available at: diagrams/architecture.png

---

## 📂 Repository Structure
network-geo-wireshark-analysis/
├── README.md
├── report/
│ └── Network_Geo_Location_Analysis_Report_AdithyanH.pdf
├── diagrams/
│ └── architecture.png
├── evidence/
│ ├── 01-attack-execution.png
│ ├── 02-wireshark-filter.png
│ ├── 03-packet-inspection.png
│ ├── 04-endpoints-analysis.png
│ ├── 05-geolocation-map.png
│ └── INDEX.md
├── logs/
│ ├── hping3-attack.txt
│ ├── wireshark-filter.txt
│ ├── packet-analysis.txt
│ ├── endpoints-analysis.txt
│ ├── geolocation-results.txt
│ └── system-info.txt
└── LICENSE

---

## 🔍 Methodology

### 1️⃣ Attack Simulation

The SYN Flood attack was generated using:
sudo hping3 -S --flood -p 80 <target-ip>

Flood mode continuously sends TCP SYN packets without waiting for replies.

---

### 2️⃣ Packet Capture

Wireshark was used on the victim machine to capture live network traffic.

---

### 3️⃣ SYN Packet Filtering

Display filter applied:
tcp.flags.syn == 1 && tcp.flags.ack == 0

This isolates TCP SYN packets where ACK flag is not set.

---

### 4️⃣ Packet Inspection

The following fields were analyzed:

- Source and Destination IP  
- TCP Flags  
- Sequence Numbers  
- Window Size  
- MSS and TCP Options  

Repeated SYN packets without handshake completion confirmed flood behavior.

---

### 5️⃣ Endpoint Analysis

Wireshark → Statistics → Endpoints was used to:

- Identify IPs with high packet counts  
- Analyze transmission statistics  
- View country and city mapping  
- Inspect ASN and ISP details  

---

### 6️⃣ Geolocation Mapping

GeoLite2 database was integrated in Wireshark.

Mapped IP details included:

- Country  
- City  
- Latitude and Longitude  
- AS Organization  

Note: Geolocation is ISP-based and approximate.

---

## 🧪 Testing & Verification

Verification was performed using:

- SYN packet frequency analysis  
- TCP flag inspection  
- Endpoint statistics  
- Wireshark IP Location Map  
- Screenshot evidence in `/evidence`  
- Command logs in `/logs`  

The complete implementation is documented in the project report.

---

## 📍 Key Findings

- Repeated SYN packets detected from attacker IP  
- High packet transmission rate confirmed flood behavior  
- TCP handshake remained incomplete  
- Multiple endpoints observed during analysis  
- Geolocation mapping provided approximate ISP-level location  

---

## 🚀 Future Work

- Integrate real-time intrusion detection system (IDS)  
- Automate SYN flood detection scripts  
- Implement firewall mitigation rules  
- Integrate with Snort or Suricata  
- Develop traffic monitoring dashboard  

---

## ⚠ Limitations

- IP geolocation is ISP-based and approximate  
- NAT and VPN may mask real source  
- Private IP addresses cannot be publicly mapped  
- Conducted in controlled lab environment only  

---

## 🤖 AI Usage Disclosure

AI-assisted tools were used for:

- Report formatting and documentation structuring  
- LaTeX formatting improvements  
- README preparation and refinement  

All attack simulation, packet capture, analysis, and experimentation were performed independently in a controlled lab environment.

---

## 📄 Project Report

The full academic report is available in:
report/Network_Geo_Location_Analysis_Report_AdithyanH.pdf

---

## 👨‍💻 Author

Adithyan H  
Bachelor of Computer Applications  
Marian College Kuttikkanam Autonomous  
March 2026  

---

## 📜 License

This project is licensed under the MIT License.
