Enterprise Network Infrastructure & High Availability Lab

A Cisco Packet Tracer enterprise network lab designed to simulate a redundant, scalable, and secure corporate network infrastructure using hierarchical network design, dynamic routing, gateway redundancy, VLAN segmentation, and network services.

The project focuses on practical network engineering and IT infrastructure concepts, including routing & switching, high availability, network segmentation, infrastructure services, and security hardening.

---

📌 Project Overview

This project simulates an enterprise network designed to provide:

- High availability and redundancy
- Segmented corporate networks
- Dynamic Layer 3 routing
- Redundant default gateways
- Resilient switch-to-switch connectivity
- Centralized network services
- Secure device management
- Separation of corporate and guest traffic

The environment was designed and implemented using Cisco Packet Tracer and Cisco IOS.

---

🏗️ Network Architecture

The network follows a hierarchical enterprise architecture with redundant infrastructure across multiple layers.

WAN / Internet Edge

- ISP Router
- Redundant Edge Routers
- Multiple paths toward the internal network

Core Layer

- CORE-SW1
- CORE-SW2
- Layer 3 switching
- OSPF dynamic routing
- Redundant Layer 3 paths

Distribution Layer

- DIST-SW1
- DIST-SW2
- Inter-VLAN Routing
- HSRP gateway redundancy
- ACLs
- DHCP Relay

Access Layer

- ACCESS-SW1
- ACCESS-SW2
- VLAN-based segmentation
- Redundant uplinks
- Spanning Tree
- Port Security

Endpoints & Services

- Corporate users
- Cisco IP Phones
- Corporate Wi-Fi
- Guest Wi-Fi
- DHCP / DNS / AAA services
- Web / File / Email services

---

🖼️ Network Topology

"Network Topology" (01-topology.png)

The topology demonstrates the overall enterprise architecture, including redundant routing and switching infrastructure, VLAN segmentation, server services, and end-user connectivity.

---

🌐 VLAN & Network Segmentation

The network uses VLAN segmentation to separate different types of traffic and improve network organization and security.

VLAN| Name| Purpose
10| MANAGEMENT| Network device management
20| USERS| Corporate users
30| VOICE| IP telephony
40| SERVERS| Server infrastructure
50| WIFI-CORP| Corporate wireless
60| WIFI-GUEST| Guest wireless
99| NATIVE-MGMT| Native / management traffic

This segmentation provides logical separation between users, servers, voice, management, and guest traffic.

---

🔄 Routing & Switching

OSPF

OSPF is used as the dynamic routing protocol to provide:

- Dynamic route exchange
- Automatic path selection
- Faster convergence
- Redundant Layer 3 paths
- Scalable routing between network segments

Inter-VLAN Routing

Layer 3 switching is used to provide communication between VLANs while maintaining logical network segmentation.

STP / PVST

Spanning Tree is used to prevent Layer 2 loops while maintaining redundant physical paths.

EtherChannel / LACP

LACP EtherChannel is used to combine multiple physical links into a logical link, providing:

- Increased bandwidth
- Link redundancy
- Improved resiliency

---

🛡️ High Availability

High availability is one of the main objectives of this project.

HSRP

HSRP provides redundant default gateways for end devices.

If the active gateway becomes unavailable, the standby device can take over gateway responsibilities, reducing the impact of device failure.

OSPF Redundancy

OSPF provides alternative Layer 3 paths between network devices, allowing traffic to use another available route when a path becomes unavailable.

Redundant Uplinks

Multiple uplinks are used between network layers to improve resiliency and reduce single points of failure.

EtherChannel

LACP EtherChannel provides link-level redundancy while logically combining multiple physical interfaces.

---

🔐 Network Security

The project incorporates multiple network security controls and secure management practices.

Device Management

- SSH-based remote management
- Dedicated management VLAN
- Local authentication
- AAA concepts

Layer 2 Security
[10/7/2026 11:48 AM] H.A: - Port Security
- Sticky MAC
- BPDU Guard
- DHCP Snooping
- Dynamic ARP Inspection

Network Segmentation

- Dedicated Management VLAN
- Separate Server VLAN
- Separate Voice VLAN
- Corporate Wi-Fi isolation
- Guest Wi-Fi segmentation

These controls help reduce unauthorized access, Layer 2 attacks, and unnecessary communication between network segments.

---

🖥️ Network Services

The server infrastructure is designed to provide common enterprise network services.

DHCP

Provides automated IP address allocation to network clients.

DNS

Provides hostname resolution for internal services and applications.

AAA

Provides centralized authentication and authorization concepts for network device access.

Web / File / Email Services

The lab also includes application-level services to simulate common enterprise infrastructure workloads.

---

🧪 Testing & Verification

The network was verified through practical connectivity and infrastructure tests.

Routing

- OSPF neighbor verification
- Routing table verification
- End-to-end connectivity testing
- Redundant path verification

Switching

- VLAN verification
- Trunk verification
- STP verification
- EtherChannel / LACP verification

High Availability

- HSRP status verification
- Gateway failover testing
- Redundant path testing

Network Services

- DHCP address assignment
- DNS resolution
- Server connectivity
- Email connectivity

Security

- Port Security verification
- Management access verification
- Guest network isolation
- Layer 2 security verification

---

📸 Project Screenshots

Additional configuration and verification screenshots are available in the ""screenshots"" (./screenshots) directory.

The screenshots document important stages of the implementation, configuration, and testing process.

---

🗂️ Repository Structure

enterprise-network-infrastructure-high-availability-lab/
│
├── documentation/
│   └── Project documentation
│
├── screenshots/
│   └── Configuration & verification screenshots
│
├── 01-topology.png
│
├── Enterprise Network Infrastructure High Availability.pkt
│
└── README.md

---

🛠️ Technologies & Tools

Networking

- Cisco IOS
- Cisco Packet Tracer
- VLANs
- Inter-VLAN Routing
- OSPF
- HSRP
- STP / PVST
- EtherChannel / LACP
- ACLs
- DHCP Relay

Network Services

- DHCP
- DNS
- AAA
- HTTP
- FTP
- SMTP / POP3

Security

- SSH
- Port Security
- Sticky MAC
- BPDU Guard
- DHCP Snooping
- Dynamic ARP Inspection
- Network Segmentation

---

🎯 Key Learning Outcomes

Through this project, I gained practical experience in:

- Designing hierarchical enterprise network architectures
- Configuring Layer 2 and Layer 3 switching
- Implementing VLAN segmentation
- Configuring OSPF dynamic routing
- Implementing HSRP gateway redundancy
- Configuring EtherChannel using LACP
- Implementing network services such as DHCP and DNS
- Applying Layer 2 security controls
- Troubleshooting routing and switching connectivity
- Testing network redundancy and failover scenarios
- Documenting network infrastructure and configurations

---

📚 Project Focus

This project demonstrates practical knowledge aligned with:

Network Engineering · Routing & Switching · Network Infrastructure · High Availability · Network Operations · IT Infrastructure

---

👩‍💻 Author

Wadha Alharbi

Computer Science & Engineering Graduate
Network Engineering & IT Infrastructure

- LinkedIn: "linkedin.com/in/wadha-alharbi" (https://linkedin.com/in/wadha-alharbi)
- GitHub: "github.com/wadhaharbi" (https://github.com/wadhaharbi)

---

📄 Project File

The complete Cisco Packet Tracer project is available here:

"Enterprise Network Infrastructure High Availability.pkt" (./Enterprise%20Network%20Infrastructure%20High%20Availability.pkt)
