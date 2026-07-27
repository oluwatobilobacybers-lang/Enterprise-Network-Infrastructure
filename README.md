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
![Status](https://img.shields.io/badge/Status-Phase_5_Complete-brightgreen?style=for-the-badge)

🚧 **Current Status**

✅ Phase 1 – VLAN Segmentation

✅ Phase 2 – Inter-VLAN Routing

✅ Phase 3 – Enterprise Services

✅ Phase 4 – Network Security

✅ Phase 5 – Switch Hardening

🚀 Currently Working On: Phase 6 – Syslog & NTP

## Table of Contents

- [Overview](#overview)
- [Business Scenario](#business-scenario)
- [Project Timeline](#project-timeline)
- [Design Decisions](#design-decisions)
- [Prerequisites](#prerequisites)
- [Enterprise Network Summary](#enterprise-network-summary)
- [Project Objectives](#project-objectives)
- [Architecture Overview](#architecture-overview)
- [Network Services](#network-services)
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
- [Verification Commands](#verification-commands)
- [Project Screenshots](#project-screenshots)
- [Project Metrics](#project-metrics)
- [Security Features](#security-features)
- [Security Architecture](#security-architecture)
- [Switch Hardening](#switch-hardening)
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

## Project Timeline

| Phase | Description | Status |
|-------|-------------|:------:|
| 1 | VLAN Segmentation | ✅ |
| 2 | Inter-VLAN Routing | ✅ |
| 3 | Enterprise Services (DHCP, DNS, HTTP, FTP) | ✅ |
| 4 | Network Security (SSH, ACLs, Port Security) | ✅ |
| 5 | Switch Hardening | ✅ |
| 6 | Syslog & NTP | ⏳ |
| 7 | NAT & Final Documentation | ⏳ |

## Design Decisions

Several design decisions were made to improve scalability, security, and maintainability:

- Router-on-a-Stick was selected due to the small network size.
- Each department was isolated into its own VLAN.
- Centralized services were placed in a dedicated Server VLAN.
- DHCP Relay was used instead of multiple DHCP servers.
- SSH replaced Telnet for secure remote management.
- ACLs were applied to enforce departmental security policies.
- Port Security was configured to prevent unauthorized endpoint connections.

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

## Architecture Overview

The enterprise network consists of a Cisco 2911 router connected to a Catalyst 2960 switch using IEEE 802.1Q trunking. Five VLANs provide logical segmentation for departmental traffic, while centralized services (DHCP, DNS, HTTP, and FTP) are hosted within a dedicated Server VLAN. Inter-VLAN communication is enabled through Router-on-a-Stick, and multiple security mechanisms—including ACLs, SSH, and Port Security—protect both management access and endpoint connectivity.

## Network Services

| Service | Purpose |
|---------|---------|
| DHCP | Automatic IP address allocation |
| DNS | Internal hostname resolution |
| HTTP | Internal web application hosting |
| FTP | File transfer services |
| SSH | Secure remote device administration |

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
| Enterprise Server  | 192.168.50.2 |
| DHCP Scope VLAN 10 | 192.168.10.100-199 |
| DHCP Scope VLAN 20 | 192.168.20.100-199 |
| DHCP Scope VLAN 30 | 192.168.30.100-199 |
| DHCP Scope VLAN 40 | 192.168.40.100-199 |

## Technologies Used

• Cisco Packet Tracer 8.2.2

### Hardware

- Cisco 2911 Router
- Cisco Catalyst 2960 Switch

### Layer 2 Technologies

- VLAN Segmentation
- IEEE 802.1Q Trunking
- Port Security

### Layer 3 Technologies

- Router-on-a-Stick
- Inter-VLAN Routing

### Network Services

- DHCP
- DHCP Relay
- DNS
- HTTP
- FTP

### Security

- SSH Version 2
- RSA Encryption
- Standard ACLs
- Extended ACLs
- Port Security
- Switch Hardening

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
    ├── show-access-lists.png
    ├── show-port-security.png
    ├── show-port-security-address.png
    ├── show-port-security-interface-fa01.png
    └── ping-report-after-disconnecting-admin-pc.png
    ├── show-spanning-tree-summary.png
    ├── show-bpduguard.png
    ├── show-portfast.png
    ├── show-unused-ports.png
```

## Key Achievements

- Designed and deployed a segmented enterprise network supporting five business departments.
- Implemented centralized DHCP, DNS, HTTP, and FTP services.
- Secured remote administration using SSH Version 2 with RSA encryption.
- Implemented Standard and Extended ACLs to enforce enterprise security policies.
- Successfully validated Layer 2, Layer 3, and enterprise network services through comprehensive connectivity, routing, and security testing.
- Hardened the enterprise switch using Cisco Layer 2 security best practices including PortFast, BPDU Guard, Management VLAN, and unused port protection.

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
- Switch Port Security
- Sticky MAC Address Learning
- MAC Address Limiting
- Violation Protection (Restrict Mode)
- Switch Hardening
- Disabled Unused Switch Ports
- Dedicated Unused VLAN (VLAN 999)
- PortFast Configuration
- BPDU Guard Protection
- Administrative Port Shutdown
- Management VLAN

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
- Verified Port Security by confirming Sticky MAC address learning, maximum MAC address limits, violation mode, and restricted access for unauthorized devices.
- Verified PortFast was enabled on all access ports.
- Verified BPDU Guard protection on access interfaces.
- Confirmed unused interfaces were assigned to VLAN 999.
- Verified unused interfaces were administratively shut down.
  
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
- [x] Port Security
- [x] Switch Hardening
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
- Configured Port Security to restrict unauthorized devices.
- Learned Sticky MAC address learning.
- Verified violation counters using show port-security.
- Understood Restrict, Protect and Shutdown violation modes.
- Implemented Layer 2 switch hardening using Cisco best practices.
- Learned the importance of disabling unused switch ports.
- Configured PortFast to reduce access-port startup delays.
- Enabled BPDU Guard to protect against rogue switches.
- Implemented a dedicated Management VLAN for improved administrative security.

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
- Layer 2 Security
- Switch Security
- Cisco Port Security
- Switch Hardening
- Spanning Tree Protocol (STP)
- Layer 2 Hardening
- BPDU Guard
- PortFast Configuration


## Configuration Highlights

### Layer 2 Configuration

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

### Port Security

```cisco
interface FastEthernet0/1
 switchport mode access
 switchport port-security
 switchport port-security maximum 1
 switchport port-security mac-address sticky
 switchport port-security violation restrict
```

### Layer 3 Configuration

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

```cisco
interface GigabitEthernet0/0.10
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.20
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.30
 ip helper-address 192.168.50.2

interface GigabitEthernet0/0.40
 ip helper-address 192.168.50.2
```

### Security Configuration

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

### Switch Hardening

The switch was hardened using Cisco Layer 2 security best practices to reduce the attack surface, protect against unauthorized devices, and improve overall network resilience.

```cisco
spanning-tree portfast default
spanning-tree portfast bpduguard default

interface range FastEthernet0/10-24
 switchport mode access
 switchport access vlan 999
 shutdown
 description UNUSED_PORT

interface FastEthernet0/1
 spanning-tree portfast
 spanning-tree bpduguard enable
```


## Verification Commands

The following Cisco IOS commands were used to verify the network configuration:

```cisco
show vlan brief
show interfaces trunk
show interfaces status

show spanning-tree summary
show spanning-tree interface fa0/1 detail

show port-security
show port-security interface fa0/1
show port-security address

show ip interface brief
show ip route

show ip dhcp binding
show ip dhcp pool

show access-lists

show ssh
show users

show running-config
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

### Enterprise Web Server Configuration

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

### Port Security Verification

Port Security was verified using Cisco IOS verification commands to confirm secure MAC address learning, configured maximum MAC addresses, violation mode, and interface protection after connecting an unauthorized device.

![Show Port Security](Screenshots/show-port-security.png)

![Show Port Security Address](Screenshots/show-port-security-address.png)

![Show Port Security Interface](Screenshots/show-port-security-interface-fa01.png)

![Show Ping Report](Screenshots/ping-report-after-disconnecting-admin-pc.png)

### Switch Hardening Verification

The switch hardening configuration was verified by confirming that PortFast and BPDU Guard were enabled globally, unused interfaces were assigned to VLAN 999 and administratively shut down, and spanning-tree settings were successfully applied.

![Spanning Tree Summary](Screenshots/show-spanning-tree-summary.png)

![BPDU Guard](Screenshots/show-bpduguard.png)

![PortFast](Screenshots/show-portfast.png)

![Unused Ports](Screenshots/show-unused-ports.png)

The screenshots below validate that Layer 2 hardening was successfully implemented using PortFast, BPDU Guard, and secure handling of unused interfaces.


## Project Metrics

| Item                      | Count |
| ------------------------- | ----: |
| VLANs                     | 5 |
| Router                    | 1 |
| Switches                  | 1 |
| PCs                       | 8 |
| Servers                   | 1 |
| Network Services          | 6 |
| Routing Technologies      | 2 |
| Security Technologies     | 13 |
| Hardening Techniques      | 5 |

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
- Port Security
- Sticky MAC Address Learning
- MAC Address Limiting
- Unauthorized Device Protection
- Switch Hardening
- PortFast
- BPDU Guard
- Unused Port Hardening
- Management VLAN


## Security Architecture

The network adopts a defense-in-depth security model by implementing complementary security controls at multiple layers of the network, including Layer 2 switching and Layer 3 routing. Network segmentation, traffic filtering, secure device management, and endpoint protection work together to reduce the attack surface and mitigate unauthorized access.

Implemented security technologies include:

| Security Technology         | Purpose |
|---------------------        |---------|
| VLAN Segmentation           | Isolates departmental traffic |
| Standard ACLs               | Restricts network access between VLANs |
| Extended ACLs               | Filters traffic by protocol, source, and destination |
| SSH Version 2               | Provides encrypted remote administration |
| RSA Encryption              | Secures SSH key exchange |
| Local User Authentication   | Restricts administrative access |
| Secure VTY Configuration    | Disables Telnet and permits SSH only |
| Port Security               | Prevents unauthorized endpoint connections |
| Sticky MAC Address Learning | Dynamically learns and secures trusted devices |
| PortFast	                  | Reduces access-port startup delay
| BPDU Guard                  | Protects against rogue switches and STP attacks
| Unused Port Hardening       | Disables unused interfaces to reduce the attack surface
| Management VLAN	          | Separates management traffic from user traffic

These layered controls help reduce unauthorized access while protecting enterprise resources.


## Switch Hardening

To strengthen Layer 2 security, several switch hardening measures were implemented following Cisco best practices.

Implemented controls include:

- Disabled unused switch ports
- Assigned unused interfaces to VLAN 999
- Administratively shut down unused interfaces
- Enabled PortFast on access ports
- Enabled BPDU Guard to protect against rogue switches
- Configured a dedicated Management VLAN

These controls reduce the attack surface, prevent unauthorized physical access, and improve the resilience of the enterprise switching infrastructure.


## Future Improvements

The following enhancements are planned for upcoming project phases:

### Phase 6 — Network Monitoring & Management

- [ ] Configure Syslog Server
- [ ] Configure NTP
- [ ] Centralize device logging

### Phase 7 — Internet Connectivity & Finalization

- [ ] Configure NAT
- [ ] Validate Internet connectivity
- [ ] Finalize documentation

## Conclusion

This project demonstrates the implementation of a secure enterprise network using Cisco Packet Tracer. It incorporates VLAN segmentation, inter-VLAN routing, centralized network services, secure remote management, and access control mechanisms commonly deployed in enterprise environments.

Throughout the project, I gained hands-on experience in network design, configuration, troubleshooting, and security while documenting each implementation phase using industry-standard practices.

## Disclaimer

This project was developed in Cisco Packet Tracer for educational and portfolio purposes. While it demonstrates enterprise networking concepts and security best practices, certain behaviors may differ from production Cisco IOS devices.

## Author

**Banjo Oluwatobiloba Adekunle**

Aspiring Cybersecurity Analyst

- ISC² Certified in Cybersecurity (CC)
- CompTIA Security+
- CEH Candidate

🔗 **LinkedIn:** https://www.linkedin.com/in/oluwatobiloba-banjo-b2368819b/

💻 **GitHub:** https://github.com/oluwatobilobacybers-lang

