# Task 1: Local Network Port Scanning & Reconnaissance

## Objective
To discover open ports and active devices on a local subnet using Nmap to evaluate network exposure and service visibility.

## Environment Details
- **Attacking Host Operating System:** Windows 10/11 (Command Prompt)
- **Target Subnet Range:** 192.168.1.0/24
- **Scan Method:** TCP SYN Scan (Stealth)

## Command Executed
```cmd
nmap -sS -T4 192.168.1.0/24 -oN network_scan_report.txt
```

## Scan Findings Summary
The scan successfully discovered 5 active hosts on the network pool:

1. **Host: 192.168.1.1 (Gateway/Router - Genexis International)**
   - Port 21/tcp (Open) - FTP (File Transfer)
   - Port 22/tcp (Open) - SSH (Secure Remote Management)
   - Port 23/tcp (Open) - Telnet (Insecure Legacy Management)
   - Port 53/tcp (Open) - Domain (DNS Service)
   - Port 80/tcp (Open) - HTTP (Router Web Interface)
2. **Host: 192.168.1.3 (vivo-1915 Mobile Device)**
   - All 1000 scanned ports are closed/ignored.
3. **Host: 192.168.1.5 (Krishna-s-M17 Device)**
   - All 1000 scanned ports are closed/ignored.
4. **Host: 192.168.1.6 (Redmi-9-Power Mobile Device)**
   - Host is active on the network.
5. **Host: 192.168.1.15 (Local Host Windows PC)**
   - Port 135/tcp (Open) - MSRPC (Remote Procedure Call)
   - Port 139/tcp (Open) - NetBIOS-SSN
   - Port 445/tcp (Open) - Microsoft-DS (SMB File Sharing)

---
