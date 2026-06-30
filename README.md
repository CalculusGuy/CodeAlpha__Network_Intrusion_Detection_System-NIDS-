# 🔐 CodeAlpha Task 4: Network Intrusion Detection System (Snort)

**Author:** Nilanjan Chowdhury  
**Date:** June 30, 2026  
**Internship:** CodeAlpha Cyber Security Internship  

---

## 📌 Overview

This project demonstrates the installation and configuration of **Snort** as a Network Intrusion Detection System (NIDS) on Kali Linux. Snort was set up to monitor live network traffic on the `eth0` interface, detect suspicious activity, and generate alerts.

---

## 🛠️ Tools Used

- **Snort++ 3.12.2.0**
- **Kali Linux**
- **eth0 Network Interface**

---

## 🚀 Installation & Setup

### Step 1: Install Snort
```bash
sudo apt update
sudo apt install snort -y
```
Step 2: Verify Installation
```bash
snort -V
```
Step 3: Run Snort in Packet Capture Mode
```bash
sudo snort -d -e -X -i eth0
```
📊 Results
Metric	Value
Interface	eth0
Packets Received	18
Packets Analyzed	17
Protocols Detected	IPv4, IPv6, ICMP, UDP, IGMP
Status	✅ Operational
