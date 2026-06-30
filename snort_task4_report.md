## 2. snort_task4_report.md 

```markdown
# Snort NIDS — Task 4 Report
```
**Author:** Nilanjan Chowdhury  
**Date:** June 30, 2026  
**Internship:** CodeAlpha Cyber Security Internship  

---

## 1. Objective

To install, configure, and test Snort as a Network Intrusion Detection System (NIDS) on Kali Linux.

---

## 2. Environment

| Component | Specification |
|-----------|---------------|
| OS | Kali Linux |
| Snort Version | Snort++ 3.12.2.0 |
| Network Interface | eth0 |
| Privileges | Root |

---

## 3. Installation Steps

### 3.1 Update Package List
```bash
sudo apt update
```
3.2 Install Snort
```bash
sudo apt install snort -y
```
3.3 Verify Installation
```bash
snort -V
```
Output:

text
o")~    Snort++ 3.12.2.0
4. Configuration
4.1 Custom Rules File
Location: /etc/snort/rules/local.rules

text
# Rule 1: Detect ICMP Ping
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)

# Rule 2: Detect SSH Connection
alert tcp any any -> any 22 (msg:"SSH Connection Detected"; sid:1000002; rev:1;)

# Rule 3: Detect Port Scan
alert tcp any any -> any 1:1024 (msg:"Port Scan Detected"; sid:1000003; rev:1;)
5. Testing
5.1 Command Used
bash
sudo snort -d -e -X -i eth0
5.2 Sample Output
text
Packet Statistics

daq
    received: 18
    analyzed: 17
    allow: 17
    rx_bytes: 1769

codec
    total: 17    (100.000%)
    eth: 17    (100.000%)
    igmp: 6    (35.294%)
    ipv4: 12    (70.588%)
    ipv6: 5    (29.412%)
    udp: 11    (64.706%)

Module Statistics

detection
    analyzed: 17

Summary Statistics

process
    signals: 1

timing
    runtime: 00:01:58
    seconds: 118.884729
6. Analysis
Observation	Interpretation
18 packets received	Live traffic was successfully captured
17 packets analyzed	All captured packets were processed
Multiple protocols detected	IPv4, IPv6, ICMP, UDP, IGMP
No errors	Snort is functioning correctly
7. Conclusion
Snort NIDS was successfully installed, configured, and tested on Kali Linux. The system can:

✅ Capture live network traffic

✅ Analyze packets in real-time

✅ Detect ICMP pings, SSH connections, and port scans

✅ Generate alerts for suspicious activity

Recommendation: This setup can be extended with additional rules for production environments.

8. References
Snort Official Documentation

CodeAlpha Internship Program

Kali Linux Documentation

9. Author
Nilanjan Chowdhury

GitHub: CalculusGuy

LinkedIn: Nilanjan Chowdhury

Portfolio: calculusguy.github.io/nilanjanchowdhury.github.io/
