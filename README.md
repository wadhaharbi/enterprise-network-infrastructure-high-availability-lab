Enterprise Network Infrastructure & High Availability Lab

«Enterprise Network Design • Routing & Switching • High Availability • Network Security»

A hands-on enterprise network infrastructure lab built using Cisco Packet Tracer and Cisco IOS.

The project simulates a corporate network environment with VLAN segmentation, OSPF dynamic routing, HSRP gateway redundancy, EtherChannel, network services, Layer 2 security, and guest network isolation.

---

📌 Project Overview

This project was designed to simulate a resilient enterprise network infrastructure with a focus on:

- Enterprise network architecture
- Routing and switching
- VLAN segmentation
- Dynamic routing using OSPF
- Gateway redundancy using HSRP
- Link redundancy using EtherChannel
- Enterprise network services
- Layer 2 security
- Guest network isolation
- Network troubleshooting and verification

The goal was to design, configure, test, and document a network that remains operational during common infrastructure failures.

---

🏗️ Network Topology

The network uses a hierarchical design with redundant Layer 3 switching and segmented access networks.

"Enterprise Network Topology" (./screenshots/01-topology.png)

Main Design Components

- Redundant distribution switches
- Layer 3 switching
- OSPF dynamic routing
- HSRP gateway redundancy
- VLAN-based segmentation
- EtherChannel / LACP
- Access layer switching
- Dedicated server infrastructure
- Corporate and guest networks

---

🔄 Routing — OSPF

OSPF is used as the dynamic routing protocol to provide communication between Layer 3 devices and redundant routing paths.

OSPF Configuration & Verification

"OSPF Neighbors" (./screenshots/02-ospf-neighbors.png)

OSPF provides:

- Dynamic route exchange
- Automatic path selection
- Redundant Layer 3 paths
- Faster convergence
- Scalable routing

OSPF neighbor relationships were verified to ensure that the Layer 3 routing infrastructure was operating correctly.

---

🛡️ High Availability — HSRP

HSRP provides default gateway redundancy for end devices.

The distribution switches operate as an active/standby gateway pair. If the active gateway becomes unavailable, the standby device can take over gateway responsibilities.

"HSRP Configuration" (./screenshots/03-hsrp.png)

High Availability Benefits

- Redundant default gateway
- Reduced single point of failure
- Gateway failover
- Improved network availability

---

🔗 EtherChannel / LACP

EtherChannel was implemented using LACP to combine multiple physical links into a single logical connection.

"EtherChannel Configuration" (./screenshots/04-etherchannel.png)

Benefits

- Link redundancy
- Increased bandwidth
- Improved resiliency
- Logical management of multiple physical interfaces

The configuration was verified to ensure the bundled links were operating correctly.

---

🌐 VLAN Segmentation

VLANs are used to logically separate different types of network traffic.

"VLAN Configuration" (./screenshots/05-vlans.png)

VLAN| Name| Purpose
10| MANAGEMENT| Network device management
20| USERS| Corporate users
30| VOICE| IP telephony
40| SERVERS| Server infrastructure
50| WIFI-CORP| Corporate wireless
60| WIFI-GUEST| Guest wireless
99| NATIVE-MGMT| Native / management traffic

Why VLAN Segmentation?

VLAN segmentation improves:

- Network organization
- Traffic separation
- Security
- Broadcast domain management
- Troubleshooting

---

🔌 Trunking

802.1Q trunking is used to carry multiple VLANs across inter-switch links.

"Trunk Configuration" (./screenshots/06-trunks.png)

Trunk links allow VLAN traffic to be transported between switches while maintaining logical segmentation across the network.

---

🔐 Network Security

Security controls were implemented at both the management and Layer 2 levels.

"Network Security" (./screenshots/07-security.png)

Security Controls

- SSH
- Local authentication
- Port Security
- Sticky MAC
- BPDU Guard
- DHCP Snooping
- Dynamic ARP Inspection
- VLAN segmentation
- Guest network isolation
[10/7/2026 11:54 AM] H.A: These controls help protect the switching infrastructure and reduce unauthorized network access.

---

🛡️ DHCP Snooping

DHCP Snooping was implemented as a Layer 2 security mechanism to help protect clients from unauthorized DHCP servers.

"DHCP Snooping" (./screenshots/08-dhcp%20snooping.png)

DHCP Snooping helps prevent:

- Rogue DHCP servers
- Unauthorized DHCP responses
- DHCP-based network attacks

The configuration was verified to ensure trusted and untrusted interfaces were handled appropriately.

---

📡 DHCP

DHCP provides automatic IP address assignment to network clients.

"DHCP" (./screenshots/09-dhcp.png)

The DHCP configuration was tested to verify that clients could obtain their network configuration automatically.

---

🌎 DNS

DNS provides hostname resolution for internal network services.

"DNS" (./screenshots/10-dns.png)

The DNS service was configured to allow clients to resolve internal hostnames and services.

---

🌐 Web Server

A web server was configured to simulate an internal enterprise application/service.

"Web Server" (./screenshots/11-web.png)

This was used to verify application-level connectivity across the network.

---

📧 Email Service

An email service was configured to simulate internal enterprise communication.

"Email Service" (./screenshots/12-email.png)

Email connectivity was tested between network clients to verify communication with the mail server.

---

🚫 Guest Network Isolation

The guest wireless network is separated from the corporate network using VLAN-based segmentation and access controls.

"Guest Network Isolation" (./screenshots/13-guest-isolation.png)

Objective

Guest devices should be able to access permitted external/network services without gaining unnecessary access to internal corporate resources.

This demonstrates the practical use of network segmentation and traffic isolation in an enterprise environment.

---

🧪 Testing & Verification

The network was verified through configuration checks and connectivity testing.

Routing

- OSPF neighbor verification
- Routing table verification
- End-to-end connectivity
- Redundant path verification

Switching

- VLAN verification
- Trunk verification
- EtherChannel verification
- STP verification

High Availability

- HSRP status verification
- Gateway failover
- Redundant path testing

Network Services

- DHCP address assignment
- DNS resolution
- Web connectivity
- Email connectivity

Security

- DHCP Snooping verification
- Layer 2 security configuration
- Guest network isolation

---

📊 High Availability Design

Component| Implementation
Dynamic Routing| OSPF
Default Gateway Redundancy| HSRP
Link Redundancy| LACP EtherChannel
Loop Prevention| STP
Network Segmentation| VLANs
Secure Management| SSH
Layer 2 Protection| Port Security / DHCP Snooping
Guest Isolation| VLAN Segmentation

---

🛠️ Technologies & Tools

Networking

- Cisco Packet Tracer
- Cisco IOS
- VLANs
- 802.1Q Trunking
- Inter-VLAN Routing
- OSPF
- HSRP
- STP
- EtherChannel / LACP

Network Services

- DHCP
- DNS
- Web
- Email

Security

- SSH
- Port Security
- Sticky MAC
- BPDU Guard
- DHCP Snooping
- Dynamic ARP Inspection
- Network Segmentation
- Guest Network Isolation

---

🎯 Key Learning Outcomes

This project provided practical experience in:

- Designing enterprise network architectures
- Configuring Layer 2 and Layer 3 switching
- Implementing VLAN segmentation
- Configuring 802.1Q trunking
- Implementing OSPF dynamic routing
- Configuring HSRP gateway redundancy
- Implementing LACP EtherChannel
- Configuring DHCP and DNS services
- Implementing Layer 2 security controls
- Isolating guest network traffic
- Troubleshooting routing and switching issues
- Verifying network redundancy and connectivity
- Documenting network infrastructure

---

📂 Repository Structure
[10/7/2026 11:54 AM] H.A: enterprise-network-infrastructure-high-availability-lab/
│
├── documentation/
│
├── screenshots/
│   ├── 01-topology.png
│   ├── 02-ospf-neighbors.png
│   ├── 03-hsrp.png
│   ├── 04-etherchannel.png
│   ├── 05-vlans.png
│   ├── 06-trunks.png
│   ├── 07-security.png
│   ├── 08-dhcp snooping.png
│   ├── 09-dhcp.png
│   ├── 10-dns.png
│   ├── 11-web.png
│   ├── 12-email.png
│   └── 13-guest-isolation.png
│
├── Enterprise Network Infrastructure High Availability.pkt
│
└── README.md

---

📄 Packet Tracer Project

The complete Cisco Packet Tracer project is available below:

"Open the Cisco Packet Tracer Project" (./Enterprise%20Network%20Infrastructure%20High%20Availability.pkt)

---

👩‍💻 Author

Wadha Alharbi

Computer Science & Engineering Graduate | Network Engineering & IT Infrastructure

Interested in:

Network Engineering · Network Operations · Routing & Switching · IT Infrastructure · Network Automation

Connect

- "LinkedIn" (https://linkedin.com/in/wadha-alharbi)
- "GitHub" (https://github.com/wadhaharbi)

---

⭐ Project Focus

«Design → Configure → Secure → Troubleshoot → Verify»

This project demonstrates practical application of enterprise networking concepts with a focus on routing & switching, network infrastructure, high availability, network security, and resilient network design.
