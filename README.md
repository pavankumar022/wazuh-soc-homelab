
# Wazuh SOC Home Lab

A complete, hands-on Security Operations Center (SOC) lab built using Wazuh SIEM.
This project demonstrates real attack simulation, detection, and evidence collection
across a 3-machine environment.

---

## Lab Architecture

| Machine | OS | IP | Role |
|---------|----|----|------|
| Ubuntu VM | Ubuntu Server 22.04 | Wazuh Manager + Dashboard |
| Windows PC | Windows 11 Home | Wazuh Agent (Victim) |
| Kali Linux | Kali 2026.1 | Attacker Machine |

---

## What This Lab Covers

- Wazuh SIEM setup and agent deployment
- File Integrity Monitoring (FIM) — real-time file add, modify, delete detection
- Brute force attack simulation using Hydra — 2,367 alerts generated
- MITRE ATT&CK technique mapping (T1110 — Brute Force, T1021.004 — SSH)
- Network traffic capture using Wireshark (SYN packet analysis)
- iptables firewall rules — blocking attacker IP with evidence export
- Vulnerability scanning using Nmap vuln scripts
- 15 real evidence screenshots collected
<img width="1112" height="383" alt="Screenshot 2026-07-11 095112" src="https://github.com/user-attachments/assets/63d64957-f5aa-4566-a15f-7c88c070ed11" />
---

## Evidence

| SS | Description |
|----|-------------|
| SS-01 | Ubuntu VM network — 192.168.1.10 confirmed |
| SS-02 | Wazuh dashboard home — 0 agents |
| SS-03 | Windows agent Active (1) on dashboard |
| SS-04 | FIM alert — file added (rule 554, level 5) |
| SS-05 | FIM alert — file modified (rule 550, level 7) |
| SS-06 | FIM alert — file deleted (rule 553, level 7) |
| SS-07 | Nmap scan — ports 135 and 445 open on Windows |
| SS-09 | Hydra brute force — SSH attack on Ubuntu |
| SS-10 | Wazuh — 2,367 brute force alerts detected |
| SS-11 | MITRE ATT&CK mapping — T1110.001, T1021.004 |
| SS-12 | Multiple auth failures — rule 40111, level 10 |
| SS-13 | Wireshark — SYN packet capture (2,683 packets) |
| SS-14 | iptables — DROP rules blocking Kali IP |
| SS-15 | Nmap vuln scan — Windows SMB scripts |

---

## Manual

Covers all 5 phases with exact commands, evidence checkpoints, and troubleshooting.

---

## Tools Used

`Wazuh` `Wireshark` `Nmap` `Hydra` `iptables` `Kali Linux` `Ubuntu Server`
`Windows 11` `VirtualBox` `SSH` `MITRE ATT&CK`

---

## Author

**Pavan Kumar**
Cybersecurity & IoT Engineering Student
[LinkedIn](https://www.linkedin.com/in/pavankumar022) •
[GitHub](https://github.com/pavankumar022) •
pavankumar797524@gmail.com
