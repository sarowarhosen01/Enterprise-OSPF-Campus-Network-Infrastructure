# 🏢 Enterprise OSPF Campus Network Infrastructure

**Single-Area OSPF Deployment with FortiGate Security, Automation & Monitoring**

![OSPF Badge](https://img.shields.io/badge/OSPF-Multi--Vendor-blue?style=for-the-badge&logo=cisco)
![FortiGate Badge](https://img.shields.io/badge/FortiGate-Next--Gen%20Firewall-red?style=for-the-badge)
![Automation Badge](https://img.shields.io/badge/Automation-Ansible%20%2B%20Python-00A86B?style=for-the-badge)
![CCNA](https://img.shields.io/badge/CCNA-Certified-007ACC?style=for-the-badge)

---

## 📋 Project Overview

This project showcases the **design, implementation, and automation** of a modern enterprise campus network using **Single-Area OSPF** as the core dynamic routing protocol. The infrastructure integrates Cisco Layer 2/3 switching, FortiGate next-generation firewalling, secure VPN connectivity, and comprehensive network automation.

Built in Cisco Packet Tracer and extended with real-world configurations, the network demonstrates production-grade practices in routing, segmentation, security, and observability. It highlights skills in **CCNA-level routing & switching**, **FortiGate security**, **Infrastructure as Code (IaC)**, and **network automation**.

**Key Highlights:**
- Fully functional Single-Area OSPF domain with fast convergence
- VLAN segmentation and inter-VLAN routing
- Enterprise security with FortiGate NGFW policies
- Site-to-Site and Remote Access VPN
- Automated configuration management using Ansible & Python
- Monitoring stack with Zabbix + Grafana

This project represents a complete **end-to-end network engineering solution** suitable for medium-to-large enterprise campuses or multi-building corporate environments.

---

## 🎯 Project Goals

- Implement a scalable, redundant Single-Area OSPF backbone
- Achieve sub-second convergence and optimal path selection
- Enforce Zero-Trust security principles using FortiGate
- Automate device provisioning and configuration drift prevention
- Establish comprehensive monitoring and logging
- Document enterprise-grade network operations for portfolio demonstration

---

## ✨ Features

- ✅ Single-Area OSPF (Area 0) with multi-vendor support
- ✅ VLAN segmentation (Data, Voice, Management, Guest)
- ✅ Inter-VLAN routing via Layer 3 switches
- ✅ Advanced Firewall Policies (FortiGate)
- ✅ IPsec Site-to-Site VPN + SSL VPN
- ✅ Centralized Authentication (RADIUS/TACACS+ simulation)
- ✅ Network Automation (Ansible Playbooks)
- ✅ Python scripting for custom monitoring/reporting
- ✅ Zabbix + Grafana observability
- ✅ Comprehensive documentation and troubleshooting guides

---

## 🛠 Technologies Used

| Category              | Technologies |
|-----------------------|--------------|
| **Routing & Switching** | Cisco IOS, OSPF, VLANs, EtherChannel, STP |
| **Security**          | FortiGate NGFW, IPsec, SSL VPN, ACLs |
| **Automation**        | Ansible, Python (Netmiko, NAPALM), Jinja2 |
| **Monitoring**        | Zabbix, Grafana, SNMPv3, Syslog |
| **OS/Platforms**      | Cisco IOS, FortiOS, Linux (Ubuntu Server) |
| **Tools**             | Cisco Packet Tracer, GNS3 (extension), VS Code, Git |

---

## 🗺 Network Architecture Overview

The network follows a **Collapsed Core** design with:
- **Core/Distribution Layer**: Layer 3 switches running OSPF
- **Access Layer**: Layer 2 switches with VLAN trunking
- **Security Perimeter**: FortiGate NGFW handling edge routing, NAT, and VPN termination
- **Management**: Out-of-band management VLAN

**Single-Area OSPF** ensures all routers maintain a single Link-State Database, providing simplicity and fast convergence for the campus footprint.

---

## 📊 Network Topology Diagram (ASCII)

```ascii
                          Internet
                              │
                        [FortiGate NGFW]
                              │
                  ┌───────────┴───────────┐
                  │                       │
             [DIST-01] ─── OSPF ─── [DIST-02]
                  │                       │
             EtherChannel             EtherChannel
                  │                       │
        ┌─────────┴────────┐    ┌─────────┴────────┐
        │                  │    │                  │
     [ACC-01]           [ACC-02]               [ACC-03]
        │                  │    │                  │
   VLANs 10,20,30     VLANs 10,20,30        VLANs 10,20,30
   (Data/Voice/Mgmt)   (Data/Voice/Mgmt)    (Data/Voice/Mgmt)
