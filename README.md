# CSC 3570 — IT Security: Pompeii Strategies Lab Project

A semester-long IT Security lab project (Tennessee Tech University, CSC 3570, Fall 2025) simulating an incoming IT team hired to take over, document, and secure an undocumented enterprise network, built and tested inside Tennessee Tech's CEROC CyberRange.

**Team:** Anthony Lamantia, Adam Campbell, Thomas Herbert

---

## Scenario

We stepped into the role of a new IT department for *Pompeii Strategies*, a company whose previous IT team left almost no documentation. Starting from four bare virtual machines, we inventoried, rebuilt, and progressively hardened the environment across eight lab modules while keeping the business running, not wiping and starting over.

## Environment

| Component | Details |
|---|---|
| Domain | `pompeii01.net` (Active Directory) |
| Domain Controller | Windows Server 2019 — `192.168.1.121` |
| Workstation | Windows 10 — `192.168.1.122` |
| Web Server | Ubuntu Server (Apache2 + PHP) — `192.168.1.130` |
| Firewall / Router | OpenWrt — WAN / LAN / DMZ zones, `192.168.1.1` |
| Platform | Tennessee Tech CEROC CyberRange (LXD-based) |

## Labs

| # | Lab | Focus |
|---|---|---|
| 1 | Introduction | Environment setup, static IPs, AD forest/domain creation, domain join |
| 2 | Baseline Security | Malwarebytes, ClamAV, Lynis, Flan Scan vulnerability scanning |
| 3 | User Authentication & Group Policy | AD OUs/groups/users, 6 GPOs (password, lockout, guest, admin rename, NTLMv2, printer policy) |
| 4 | Configuration Management | Dockerized SaltStack lab — states, pillars, automated package/user provisioning |
| 5 | Firewalls | OpenWrt zone-based rules (WAN/LAN/DMZ), NAT, port forwarding, UFW host firewall |
| 7 | SSH & SSH Keys | Key-based auth, disabling password login, SSH config aliases, SSH tunneling |
| 8 | Intrusion Detection/Prevention | Fail2ban jail configuration and live brute-force ban testing |

*(Lab 6 — Wireshark packet-capture analysis — was part of the course but is not included in this repository.)*

## What's in This Repo

- **`CSC3570_Lab_Portfolio.docx`** — Full write-up covering objectives, actions taken, screenshots, deliverable answers, and changelog excerpts for each completed lab.
- Lab instruction documents, changelogs, and supporting screenshots (as applicable).

## Skills & Tools Demonstrated

- **Windows Server / Active Directory:** domain promotion, OUs, security groups, Group Policy Objects, password/lockout/authentication policy
- **Linux Administration:** Ubuntu user/permission management, ClamAV, Lynis, Fail2ban, UFW
- **Networking & Firewalls:** OpenWrt zone-based (WAN/LAN/DMZ) rule design, NAT, port forwarding
- **Configuration Management:** SaltStack states/pillars, Docker-based lab orchestration
- **Remote Access Security:** SSH key-based authentication, SSH tunneling, disabling password auth
- **Vulnerability Management:** Flan Scan / Nmap-based scanning, CVE triage and remediation planning
- **Change Management:** running changelog documenting every configuration change with rationale

## Disclaimer

This project was completed for an academic IT Security course inside an isolated, instructor-provided cyber range. All IP addresses, domains, and credentials referenced are lab-only values with no connection to production systems.

