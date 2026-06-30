## 3. local.rules
CodeAlpha Task 4 — Snort NIDS Rules
**Author: Nilanjan Chowdhury**
Date: June 30, 2026
Rule 1: Detect ICMP Ping
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)

Rule 2: Detect SSH Connection
alert tcp any any -> any 22 (msg:"SSH Connection Detected"; sid:1000002; rev:1;)

Rule 3: Detect Port Scan (Multiple Ports)
alert tcp any any -> any 1:1024 (msg:"Port Scan Detected"; sid:1000003; rev:1;)
