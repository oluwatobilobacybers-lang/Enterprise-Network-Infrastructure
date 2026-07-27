# Enterprise Network Infrastructure

![Cisco](https://img.shields.io/badge/Cisco-Packet_Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Router](https://img.shields.io/badge/Router-2911-blue?style=for-the-badge)
![Switch](https://img.shields.io/badge/Switch-Catalyst_2960-blue?style=for-the-badge)
![VLAN](https://img.shields.io/badge/VLAN-Configured-success?style=for-the-badge)
![Inter-VLAN Routing](https://img.shields.io/badge/Inter--VLAN-Routing-success?style=for-the-badge)
![DHCP](https://img.shields.io/badge/DHCP-Configured-success?style=for-the-badge)
![DNS](https://img.shields.io/badge/DNS-Configured-success?style=for-the-badge)
![HTTP](https://img.shields.io/badge/HTTP-Web_Server-success?style=for-the-badge)
![FTP](https://img.shields.io/badge/FTP-Configured-success?style=for-the-badge)
![SSH](https://img.shields.io/badge/SSH-Secured-success?style=for-the-badge)
![Standard ACL](https://img.shields.io/badge/Standard_ACL-Configured-success?style=for-the-badge)
![Extended ACL](https://img.shields.io/badge/Extended_ACL-Configured-success?style=for-the-badge)

![Project](https://img.shields.io/badge/Project-Enterprise_Network-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In_Progress-yellow?style=for-the-badge)

🚧 **Status:** In Progress

## Table of Contents

- [Overview](#overview)
- [Business Scenario](#business-scenario)
- [Prerequisites](#prerequisites)
- [Enterprise Network Summary](#enterprise-network-summary)
- [Project Objectives](#project-objectives)
- [Network Topology](#network-topology)
- [IP Addressing Scheme](#ip-addressing-scheme)
- [Technologies Used](#technologies-used)
- [Repository Structure](#repository-structure)
- [Key Achievements](#key-achievements)
- [Features Implemented](#features-implemented)
- [Testing & Verification](#testing--verification)
- [Troubleshooting](#troubleshooting)
- [Current Progress](#current-progress)
- [Lessons Learned](#lessons-learned)
- [Skills Demonstrated](#skills-demonstrated)
- [Configuration Highlights](#configuration-highlights)
- [Project Screenshots](#project-screenshots)
- [Project Metrics](#project-metrics)
- [Future Improvements](#future-improvements)
- [Conclusion](#conclusion)
- [Author](#author)

## Overview

This project demonstrates the design and implementation of a secure enterprise network infrastructure using Cisco Packet Tracer. It showcases network segmentation, inter-VLAN routing, centralized network services, and foundational security controls commonly used in enterprise environments.

The objective is to build a secure and scalable network that supports multiple departments through VLAN segmentation and Inter-VLAN Routing.

## Business Scenario

A growing enterprise requires a secure and scalable network to support multiple departments while maintaining centralized services and controlled communication between business units.

This project addresses those requirements by implementing:

- VLAN segmentation
- Inter-VLAN Routing
- Enterprise DHCP and DNS services
- Secure SSH remote administration
- Standard and Extended ACLs
- Centralized web and file services

The resulting design improves scalability, security, and manageability while reflecting networking practices commonly used in enterprise environments.

## Prerequisites

To explore or replicate this project, you should have:

- Cisco Packet Tracer 8.2.2 or later
- Basic understanding of IPv4 addressing
- Familiarity with Cisco IOS CLI
- Basic networking concepts (VLANs, Routing, DHCP)

## Enterprise Network Summary

This project simulates an enterprise network consisting of five departmental VLANs connected through Router on a Stick architecture. Core enterprise services, including DHCP, DNS, HTTP, FTP, SSH, and Access Control Lists (ACLs), were implemented to provide centralized management, secure communication, and controlled network access.

The project follows industry best practices for network segmentation, service deployment, and security while demonstrating practical Cisco IOS configuration and troubleshooting skills.

## Project Objectives

- Design an enterprise network topology
- Implement VLAN segmentation
- Configure Router-on-a-Stick
- Enable Inter-VLAN Routing
- Verify connectivity between departments
- Document network configurations and testing

## Network Topology

Departments included:

| VLAN | Department | Network         | Gateway      |
| ---- | ---------- | --------------- | ------------ |
| 10   | Admin      | 192.168.10.0/24 | 192.168.10.1 |
| 20   | Finance    | 192.168.20.0/24 | 192.168.20.1 |
| 30   | HR         | 192.168.30.0/24 | 192.168.30.1 |
| 40   | IT         | 192.168.40.0/24 | 192.168.40.1 |
| 50   | Servers    | 192.168.50.0/24 | 192.168.50.1 |

## IP Addressing Scheme

| Device/Network | IP Address |
|---------------|------------|
| Router VLAN 10 Gateway | 192.168.10.1 |
| Router VLAN 20 Gateway | 192.168.20.1 |
| Router VLAN 30 Gateway | 192.168.30.1 |
| Router VLAN 40 Gateway | 192.168.40.1 |
| Router VLAN 50 Gateway | 192.168.50.1 |
| Enterprise Server | 192.168.50.2 |
| DHCP Scope VLAN 10 | 192.168.10.100-199 |
| DHCP Scope VLAN 20 | 192.168.20.100-199 |
| DHCP Scope VLAN 30 | 192.168.30.100-199 |
| DHCP Scope VLAN 40 | 192.168.40.100-199 |

## Technologies Used

- Cisco Packet Tracer 8.2.2
- Cisco 2911 Integrated Services Router
- Cisco Catalyst 2960 Switch
- VLAN Segmentation
- IEEE 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- DHCP
- DHCP Relay (ip helper-address)
- DNS
- HTTP
- FTP
- SSH Version 2
- RSA Encryption
- Standard ACLs
- Extended ACLs

## Repository Structure

```
Enterprise-Network-Infrastructure/
│
├── README.md
├── Enterprise-Network-Infrastructure.pkt
└── Screenshots/
    ├── enterprise-network-diagram.png
    ├── vlan-creation-and-configuration.png
    ├── vlan-trunk-configuration.png
    ├── dhcp-server-configuration.png
    ├── dns-service-enabled-record.png
    ├── http-homepage.png
    ├── web-server-test.png
    ├── ftp-user-authentication.png
    ├── ssh-login.png
    ├── ssh-configuration.png
    ├── rsa-key-generation.png
    ├── acl-configuration.png
    ├── extended-acl-verification.png
    ├── show-extended-acl.png
    └── show-access-lists.png
```

## Key Achievements

- Designed and deployed a segmented enterprise network supporting five business departments.
- Implemented centralized DHCP, DNS, HTTP, and FTP services.
- Secured remote administration using SSH Version 2 with RSA encryption.
- Implemented Standard and Extended ACLs to enforce enterprise security policies.
- Successfully validated Layer 2, Layer 3, and enterprise network services through comprehensive connectivity, routing, and security testing.

## Features Implemented

- VLAN segmentation (VLANs 10, 20, 30, 40 and 50)
- Router-on-a-Stick (Inter-VLAN Routing)
- IEEE 802.1Q Trunk Configuration
- Enterprise DHCP Server
- DHCP Relay using `ip helper-address`
- Enterprise DNS Server
- Internal HTTP Web Server
- Enterprise FTP Server
- FTP User Authentication
- Secure Shell (SSH) Remote Management
- RSA Key Generation
- SSH Version 2
- Local User Authentication
- Secure VTY Configuration
- Standard Access Control Lists (ACLs)
- Inter-VLAN Traffic Filtering
- Department-Based Access Control
- Extended Access Control Lists (ACLs)
- Protocol-specific traffic filtering

## Testing & Verification

The following tests were successfully completed:
- Verified communication between devices within the same VLAN.
- Verified Inter-VLAN Routing between all departments.
- Confirmed DHCP automatic IP address assignment.
- Verified DNS hostname resolution.
- Successfully accessed the internal web server using both IP address and DNS hostname.
- Successfully authenticated to the FTP server from multiple VLANs.
- Successfully established encrypted SSH remote access using a local administrator account.
- Verified SSH Version 2 configuration and RSA key generation.
- Confirmed Standard ACL functionality by restricting Finance VLAN access to the HR VLAN.
- Verified authorized traffic continued to pass after ACL implementation.
- Verified Extended ACLs by restricting specific application traffic while allowing authorized communication between departments.
  
## Troubleshooting

### Issue: Server VLAN (VLAN 50) Connectivity

During the implementation of the Server VLAN (VLAN 50), connectivity between the router and the server initially failed.

#### Root Cause

Although VLAN 50 had been created and assigned to the server access port (Fa0/9), it was not included in the list of VLANs allowed across the trunk link between the switch and the router.

#### Resolution

The issue was resolved by updating the trunk configuration:

```bash
interface GigabitEthernet0/1
switchport trunk allowed vlan add 50
```

After verifying the trunk configuration, connectivity between the router and the server was successfully restored.

#### Verification

- Successfully pinged the server (192.168.50.2) from the router.
- Successfully pinged the server from devices in other VLANs.
- Confirmed VLAN 50 was active and forwarding on the trunk link using:

```bash
show interfaces trunk
```

## Current Progress

- [x] VLAN Segmentation
- [x] Inter-VLAN Routing
- [x] Server VLAN
- [x] DHCP
- [x] DNS
- [x] HTTP Server
- [x] FTP Server
- [x] SSH
- [x] Standard ACLs
- [x] Extended ACLs
- [ ] Port Security
- [ ] Switch Hardening
- [ ] Syslog
- [ ] NTP
- [ ] NAT
- [ ] Final Documentation

## Lessons Learned

This project strengthened my understanding of:
- VLAN segmentation and network design.
- Router-on-a-Stick configuration.
- IEEE 802.1Q trunking.
- Systematic troubleshooting using Cisco IOS verification commands.
- The importance of validating configurations before making changes.
- Learned how DHCP works in enterprise networks.
- Configured a centralized DHCP server for multiple VLANs.
- Used DHCP Relay (`ip helper-address`) to forward DHCP requests across VLANs.
- Verified automatic IP assignment and successful inter-VLAN communication.
- Configured an enterprise DNS server.
- Created DNS A records for internal services.
- Verified hostname resolution from client PCs.
- Learned how DNS integrates with DHCP to provide automatic name resolution.
- Configured an enterprise HTTP server.
- Created and deployed a custom HTML homepage.
- Verified web access using both IP address and DNS hostname.
- Understood the relationship between DNS and HTTP services.
- Learned how FTP provides centralized file transfer services in enterprise networks.
- Configured and tested FTP user authentication.
- Observed that Cisco Packet Tracer simulates FTP functionality but has limitations compared to production FTP servers.
- Configured Secure Shell (SSH) for encrypted remote device management.
- Generated RSA keys to secure remote administrative access.
- Configured local user authentication for privileged access.
- Restricted VTY lines to SSH, eliminating insecure Telnet access.
- Verified successful remote login using SSH.
- Configured Standard Access Control Lists to restrict inter-VLAN communication.
- Applied ACLs to router subinterfaces to enforce security policies.
- Verified access restrictions through connectivity testing.
- Learned the difference between Standard and Extended ACLs.
- Applied Extended ACLs to filter traffic based on source, destination, and protocol.
- Understood the importance of placing Extended ACLs close to the traffic source.

## Skills Demonstrated

- Enterprise Network Design
- VLAN Segmentation
- Layer 2 Switching
- Layer 3 Routing
- Inter-VLAN Routing
- DHCP Configuration
- DNS Configuration
- Web Server Deployment
- FTP Configuration
- Network Troubleshooting
- Cisco IOS Configuration
- Technical Documentation
- Access Control Lists (ACLs)
- Network Access Control
- Enterprise Security Policy Implementation
- SSH Configuration
- Secure Remote Administration
- Extended Access Control Lists
- Traffic Filtering
- Cisco IOS Security
- Enterprise Network Security
- Network Documentation

## Configuration Highlights

### VLAN Configuration

```cisco
vlan 10
 name Admin

vlan 20
 name Finance

vlan 30
 name HR

vlan 40
 name IT

vlan 50
 name Servers
```

### Trunk Configuration

```cisco
interface GigabitEthernet0/1
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30,40,50
```

### Router-on-a-Stick

```cisco
interface GigabitEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface GigabitEthernet0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
```

### DHCP Relay

```
interface GigabitEthernet0/0.10
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.20
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.30
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.40
 ip helper-address 192.168.50.2
```
### SSH Configuration

```cisco
hostname Enterprise-Router
ip domain-name enterprise.local

crypto key generate rsa

username admin privilege 15 secret ********

line vty 0 4
 login local
 transport input ssh
```

### Standard ACL

```cisco
access-list 10 deny 192.168.20.0 0.0.0.255
access-list 10 permit any
```

### Extended ACL

```cisco
ip access-list extended BLOCK_HTTP
 deny tcp 192.168.20.0 0.0.0.255 host 192.168.50.2 eq 80
 permit ip any any
```

## Verification Commands

The following Cisco IOS commands were used to verify the network configuration:

```cisco
show vlan brief
show interfaces trunk
show ip route
show ip dhcp binding
show ip dhcp pool
show ip interface brief
show access-lists
show running-config
show ssh
show users
```

## Project Screenshots

### Enterprise Network Diagram

The enterprise topology consists of five VLANs connected through Router-on-a-Stick architecture with centralized DHCP, DNS, HTTP, FTP, and SSH services hosted in the Server VLAN.

![Enterprise Network Diagram](Screenshots/enterprise-network-diagram.png)

### VLAN Configuration

![VLAN Configuration](Screenshots/vlan-creation-and-configuration.png)

### Trunk Configuration

![Trunk Configuration](Screenshots/vlan-trunk-configuration.png)

### DNS Configuration

![DNS Record](Screenshots/dns-service-enabled-record.png)

### DHCP Configuration

![DHCP Configuration](Screenshots/dhcp-server-configuration.png)

### Enterprise Web Server

![HTML Home Page](Screenshots/http-homepage.png)
![HTTP Web Server Test](Screenshots/web-server-test.png)

### FTP Authentication

![FTP User Accounts](Screenshots/ftp-user-authentication.png)

### SSH Login

![SSH Login](Screenshots/ssh-login.png)

### SSH Configuration

![SSH Configuration](Screenshots/ssh-configuration.png)

### RSA Key Generation

![RSA Key Generation](Screenshots/rsa-key-generation.png)

### ACL Configuration

![ACL Configuration](Screenshots/acl-configuration.png)

### Extended ACL Verification

![Extended ACL Verification](Screenshots/extended-acl-verification.png)

### Show Extended ACL Verification

![Show Extended ACL](Screenshots/show-extended-acl.png)

### Show Access Lists

![Show Extended ACL](Screenshots/show-access-lists.png)

## Project Metrics

| Item                  | Count |
| --------------------- | ----: |
| VLANs                 |     5 |
| Router                |     1 |
| Switches              |     1 |
| PCs                   |     8 |
| Servers               |     1 |
| Enterprise Services   |     6 |
| ACL Types             |     2 |
| Security Technologies |     7 |

## Security Features

The following security mechanisms have been implemented:

- VLAN Segmentation
- Standard ACLs
- Extended ACLs
- SSH Version 2
- RSA Key Encryption
- Local User Authentication
- Secure VTY Access
- Telnet Disabled
- Department-Based Traffic Filtering

## Future Improvements

The following enhancements are planned to further strengthen the enterprise network:

- [ ] Configure Switch Port Security to prevent unauthorized device connections.
- [ ] Apply Switch Security Hardening (disable unused ports, secure management access, and implement security best practices).
- [ ] Configure Syslog for centralized logging and monitoring.
- [ ] Configure NTP for synchronized network device timekeeping.
- [ ] Implement Network Address Translation (NAT) for Internet connectivity simulation.
- [ ] Perform comprehensive end-to-end testing and finalize project documentation.

## Conclusion

This project demonstrates the implementation of a secure enterprise network using Cisco Packet Tracer. It incorporates VLAN segmentation, inter-VLAN routing, centralized network services, secure remote management, and access control mechanisms commonly deployed in enterprise environments.

Throughout the project, I gained hands-on experience in network design, configuration, troubleshooting, and security while documenting each implementation phase using industry-standard practices.

## Author

**Banjo Oluwatobiloba Adekunle**

Aspiring Cybersecurity Analyst

- ISC² Certified in Cybersecurity (CC)
- CompTIA Security+
- CEH Candidate

🔗 **LinkedIn:** https://www.linkedin.com/in/oluwatobiloba-banjo-b2368819b/

💻 **GitHub:** https://github.com/oluwatobilobacybers-lang

