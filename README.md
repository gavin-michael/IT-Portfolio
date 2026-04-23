# Gavin White -- IT & Networking Portfolio

**Portfolio:** [gavinwhite.dev](https://gavinwhite.dev) | **Status:** [status.gavinwhite.dev](https://status.gavinwhite.dev)

## About Me

I'm an aspiring network engineer with a CompTIA Security+ certification and hands-on experience building production-style infrastructure from scratch. I focus on network engineering, security, and infrastructure monitoring -- learning by building real systems, breaking them, and documenting everything along the way.

My primary project is a full homelab environment running on Proxmox with a virtualized OPNsense firewall, VLAN segmentation, a complete observability stack, and a suite of self-hosted services -- all accessible locally via clean URLs and publicly via a custom domain. Every component is documented with the depth and detail expected in a professional environment.

---

## Certifications

| Certification | Status |
|--------------|--------|
| CompTIA Security+ (CE) -- SY0-701 | Earned |
| CCNA | In Progress (expected 2026) |

---

## Technical Skills

| Category | Skills |
|----------|--------|
| Networking | VLANs (802.1Q), inter-VLAN routing, firewall policy design, DHCP, DNS, SNMP (v2c), syslog, TCP/IP, subnetting, NAT |
| Firewalls | OPNsense -- stateful rules, per-VLAN security policies, NAT, DNSSEC, Net-SNMP |
| Virtualization | Proxmox VE -- VLAN-aware bridges, trunk/access port configuration, VM provisioning |
| Containerization | Docker, Docker Compose, Portainer |
| Monitoring | Prometheus, Grafana, Node Exporter, SNMP Exporter, Uptime Kuma |
| Log Aggregation | Grafana Loki, Grafana Alloy (Docker log collection + syslog reception) |
| DNS & Ad Blocking | Pi-hole (DNS sinkhole), OPNsense Unbound (DNSSEC), local DNS records |
| Reverse Proxy | Nginx Proxy Manager -- hostname-based routing for internal services |
| Remote Access | Tailscale VPN mesh, Cloudflare Tunnel (zero-trust public hosting) |
| Query Languages | PromQL (metrics), LogQL (logs) |
| Operating Systems | Ubuntu Server 24.04, Windows Server 2022, Windows 11 |
| Switching | Netgear JGS516PE -- 802.1Q VLANs, trunk/access ports, PVID configuration |
| Tools | SSH, netplan, bash, nano, Docker CLI, snmpwalk, tcpdump |
| Active Directory | Domain controller setup, user/group management, Group Policy, domain joins |
| Web Development | HTML, CSS, static site hosting via Nginx |

---

## Projects

### HomeLab Server -- Production-Style Infrastructure
**Status:** Active | **Repo:** [HomeLab-Server](https://github.com/gavin-michael/HomeLab-Server) | **Live:** [gavinwhite.dev](https://gavinwhite.dev)

A full homelab built on Proxmox VE with enterprise-grade network segmentation, a virtualized firewall, a complete monitoring and observability stack, and self-hosted services exposed both locally and publicly. This is my primary project and portfolio centerpiece.

**What I built:**
- Proxmox hypervisor with VLAN-aware virtual networking (trunk and access ports)
- OPNsense firewall/router handling inter-VLAN routing, DHCP, DNS, and per-VLAN security policies
- 4 active VLANs (Trusted, Lab, IoT, Guest) with restrictive firewall rules
- Prometheus + Node Exporter + SNMP Exporter for metrics collection
- Grafana dashboards with friendly interface names via metric relabeling
- Loki + Grafana Alloy for centralized log aggregation (Docker logs + OPNsense firewall syslog)
- Pi-hole for network-wide DNS ad blocking across all VLANs, forwarding to OPNsense Unbound with DNSSEC
- Nginx Proxy Manager with 10 local proxy hosts for clean *.homelab.local URLs
- Custom portfolio website served via Nginx, publicly accessible at gavinwhite.dev through Cloudflare Tunnel
- Tailscale VPN mesh for secure remote access to the entire lab from any device
- Uptime Kuma with public status page at status.gavinwhite.dev
- Homepage internal dashboard organizing all services
- Full documentation: build phases, network architecture, lessons learned, 31 annotated screenshots

**Key decisions:**
- Chose Grafana Alloy over Promtail after discovering Promtail reached end-of-life in March 2026
- Used Prometheus metric_relabel_configs to rename raw SNMP interface IDs to friendly names
- Configured OPNsense syslog as RFC3164 (BSD format) after debugging Alloy's default RFC5424 parser
- Separated Docker compose stacks into /opt/monitoring/ and /opt/services/ for operational isolation
- Used Cloudflare Tunnel instead of port forwarding -- zero exposed ports, zero-trust architecture

---

### Active Directory Lab
**Status:** Complete | **Repo:** [active-directory-lab](https://github.com/gavin-michael/active-directory-lab)

Built a Windows Server Active Directory environment to practice enterprise identity management.

- Windows Server 2022 Domain Controller with AD DS and integrated DNS
- User and group management with organizational units
- Group Policy Objects (GPOs) for endpoint security controls
- Domain-joined Windows 10 client
- Troubleshot DNS resolution failures, domain join errors, and Kerberos time synchronization issues

---

### Home Lab Network
**Status:** Complete | **Repo:** [home-lab-network](https://github.com/gavin-michael/home-lab-network)

My first networking project -- a virtual network built in VirtualBox to learn TCP/IP fundamentals.

- Internal network (192.168.10.0/24) with static IP addressing
- Windows and Ubuntu VMs communicating across the network
- Troubleshot connectivity, firewall, and routing issues

---

## What I'm Currently Working On

- Studying for CCNA (Jeremy's IT Lab on YouTube)
- Deploying Jellyfin self-hosted media server
- Planning Ansible infrastructure automation
- Planning Wazuh SIEM deployment
- Rebuilding Active Directory lab inside Proxmox with proper VLAN segmentation
- Applying to NOC Technician roles

---

## Contact

- **Portfolio:** [gavinwhite.dev](https://gavinwhite.dev)
- **LinkedIn:** [linkedin.com/in/gavin-white-812345315](https://www.linkedin.com/in/gavin-white-812345315)
- **GitHub:** [github.com/gavin-michael](https://github.com/gavin-michael)
- **Email:** whitegavin2000@gmail.com
