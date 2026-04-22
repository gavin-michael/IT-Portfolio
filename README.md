# Gavin White — IT & Networking Portfolio

## About Me

I'm an aspiring network engineer with a CompTIA Security+ certification and hands-on experience building production-style infrastructure from scratch. I focus on network engineering, security, and infrastructure monitoring — learning by building real systems, breaking them, and documenting everything along the way.

My primary project is a full homelab environment running on Proxmox with a virtualized OPNsense firewall, VLAN segmentation, and a complete observability stack covering metrics, logs, and availability monitoring. Every component is documented with the depth and detail expected in a professional environment.

---

## Certifications

| Certification | Status |
|--------------|--------|
| CompTIA Security+ (CE) | ✅ Earned |
| CCNA | 📚 In Progress |

---

## Technical Skills

| Category | Skills |
|----------|--------|
| Networking | VLANs (802.1Q), inter-VLAN routing, firewall policy design, DHCP, DNS, SNMP (v2c), syslog, TCP/IP, subnetting, NAT |
| Firewalls | OPNsense — stateful rules, per-VLAN security policies, NAT, DNSSEC, Net-SNMP |
| Virtualization | Proxmox VE — VLAN-aware bridges, trunk/access port configuration, VM provisioning |
| Containerization | Docker, Docker Compose, Portainer |
| Monitoring | Prometheus, Grafana, Node Exporter, SNMP Exporter, Uptime Kuma |
| Log Aggregation | Grafana Loki, Grafana Alloy (Docker log collection + syslog reception) |
| Query Languages | PromQL (metrics), LogQL (logs) |
| Operating Systems | Ubuntu Server 24.04, Windows Server, Windows 11 |
| Switching | Netgear JGS516PE — 802.1Q VLANs, trunk/access ports, PVID configuration |
| Tools | SSH, netplan, bash, nano, Docker CLI, snmpwalk, tcpdump |
| Active Directory | Domain controller setup, user/group management, Group Policy, domain joins |

---

## Projects

### HomeLab Server — Production-Style Infrastructure
**Status:** Active | **Repo:** [HomeLab-Server](https://github.com/gavin-michael/HomeLab-Server)

A full homelab built on Proxmox VE with enterprise-grade network segmentation, a virtualized firewall, and a complete monitoring and observability stack. This is my primary project and portfolio centerpiece.

**What I built:**
- Proxmox hypervisor with VLAN-aware virtual networking (trunk and access ports)
- OPNsense firewall/router handling inter-VLAN routing, DHCP, DNS, and per-VLAN security policies
- 4 active VLANs (Trusted, Lab, IoT, Guest) with restrictive firewall rules
- Prometheus + Node Exporter + SNMP Exporter for metrics collection
- Grafana dashboards with friendly interface names via metric relabeling
- Loki + Grafana Alloy for centralized log aggregation (Docker logs + OPNsense firewall syslog)
- Uptime Kuma monitoring 7 services
- Full documentation: build phases, network architecture, lessons learned

**Key decisions:**
- Chose Grafana Alloy over Promtail after discovering Promtail reached end-of-life in March 2026
- Used Prometheus metric_relabel_configs to rename raw SNMP interface IDs to friendly names
- Configured OPNsense syslog as RFC3164 (BSD format) after debugging Alloy's default RFC5424 parser

---

### Active Directory Lab
**Status:** Complete | **Repo:** [active-directory-lab](https://github.com/gavin-michael/active-directory-lab)

Built a Windows Server Active Directory environment to practice enterprise identity management.

- Windows Server 2022 Domain Controller
- Active Directory Domain Services (AD DS)
- User and group management with organizational units
- Group Policy Object (GPO) configuration
- Domain-joined Windows 10 client

---

### Home Lab Network
**Status:** Complete | **Repo:** [home-lab-network](https://github.com/gavin-michael/home-lab-network)

My first networking project — a virtual network built in VirtualBox to learn TCP/IP fundamentals.

- Internal network (192.168.10.0/24) with static IP addressing
- Windows and Ubuntu VMs communicating across the network
- Troubleshot connectivity, firewall, and routing issues

---

## What I'm Currently Working On

- Studying for CCNA (Jeremy's IT Lab on YouTube)
- Rebuilding Active Directory lab inside Proxmox with proper VLAN segmentation
- Planning GNS3/EVE-NG deployment for OSPF and BGP routing labs
- Documenting homelab build on LinkedIn and YouTube

---

## Contact

- **LinkedIn:** [linkedin.com/in/gavin-white-812345315](https://www.linkedin.com/in/gavin-white-812345315)
- **GitHub:** [github.com/gavin-michael](https://github.com/gavin-michael)
- **Email:** whitegavin2000@gmail.com
