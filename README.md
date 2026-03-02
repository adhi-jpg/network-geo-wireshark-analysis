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

Architecture diagram available at:
