# Enterprise Network Architecture & Security with FortiGate

## 📌 Project Overview
This lab demonstrates an enterprise network design featuring secure multi-zone environments (LANs, Admin VLAN, and a DMZ Web Server) interconnected using dual FortiGate firewalls with an explicit internet gateway connection.

## 🗺️ Network Topology
![Network Topology](/home/mr_ahmed/GNS3/github-projects/lab-1/Screenshot from 2026-05-24 20-36-08.png)

## 🛠️ Tech Stack & Lab Environment
* **Emulation:** GNS3
* **Security:** FortiGate Firewalls (FortiOS)
* **Switching:** Cisco IOS Switches
* **Services:** Linux Web Server (HTTP), FTP File Server

## 🔒 Key Implementation & Troubleshooting Features
1. **Multi-VLAN Inter-Routing:** Managed and segregated VLAN 10, 20, and 30 on FortiGate-1.
2. **Deterministic Routing (Admin Distance):** Resolved a dual-WAN routing conflict on FortiGate-1 by tuning administrative distances to force traffic through the correct internet path (FortiGate-2).
3. **Advanced NAT Integration:** Implemented specific Dynamic NAT IP Pools on FortiGate-1 to differentiate between regular traffic and administrative traffic.
4. **Local-In Policy Management:** Secured FortiGate-2 management interfaces by applying `local-in-policy` filters to explicitly allow access ONLY from the Admin IP Pool, preventing other VLANs from unauthorized access.
5. **DNAT & Server Publishing (Virtual IP):** Configured a Virtual IP (VIP) on FortiGate-2 to securely map public internet traffic to the internal DMZ Web Server.
6. **Enterprise Services Deployment:** Configured and validated centralized FTP file services and external HTTP web hosting within the topology.

## 📄 Device Configurations
You can find the full CLI configurations (including Firewalls, Cisco Switches, and Server network profiles) inside the repository directory.
