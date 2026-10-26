# Secure Campus Network Design | Cisco Packet Tracer

A network security project developed as part of the **Cisco Virtual Cybersecurity Internship Program 2025**, focused on designing, simulating, and securing a college campus network using segmentation, access-control policies, hybrid remote-access concepts, and centralized logging.

## Project Overview

Traditional campus networks can expose sensitive resources when students, faculty, and servers share insufficiently segmented network infrastructure. This project addresses these risks by designing a multi-layered campus network security model for Amity Campus using Cisco Packet Tracer.

The project is divided into three parts:

1. **Attack Surface Analysis & VLAN Segmentation**
2. **Secure Hybrid Remote Access**
3. **Smart Web Filtering & Policy Framework**

## Objectives

- Separate faculty, student, and server traffic using VLANs and trust zones.
- Configure inter-VLAN routing to support controlled communication.
- Design a hybrid network topology for on-campus and remote access.
- Develop role-based network access policies.
- Simulate web-filtering rules and access restrictions.
- Use Syslog to monitor and record security-policy violations.

## Technologies & Tools

- **Cisco Packet Tracer** — Network topology design and simulation.
- **VLANs** — Logical separation of network devices and user groups.
- **Router-on-a-Stick** — Inter-VLAN routing using router subinterfaces.
- **Access Control Lists (ACLs)** — Traffic filtering and access control.
- **VPN Concepts** — Simulation of secure remote-access architecture.
- **Syslog** — Centralized logging and visibility into network events.
- **Firewall and Filtering Concepts** — Policy-based network protection.

## Project Architecture

The network is organized into three primary trust zones:

- **Faculty Zone:** Network access for faculty users.
- **Student Zone:** Segmented access for student devices.
- **Server Zone:** Internal resources with restricted communication policies.

The hybrid-access design extends the topology with a home router and a WAN connection between the campus and home routers. A filtering appliance and Syslog server are included in the web-filtering design.

### Network Components

| Component | Purpose |
|---|---|
| Routers | Routing between networks and remote-access connectivity |
| Switches | Connecting devices and supporting VLAN segmentation |
| VLANs | Separating traffic by user group |
| ACLs | Enforcing traffic permissions and restrictions |
| Filtering appliance | Representing the web-filtering policy layer |
| Syslog server | Recording network events and violation attempts |

## Implementation

### Part 1 — Attack Surface Analysis & VLAN Segmentation

**Objective:** Identify network security weaknesses and establish separated trust zones.

- Mapped the campus network topology using Cisco Packet Tracer.
- Created Faculty, Students, and Servers trust zones.
- Configured Router-on-a-Stick for inter-VLAN routing.
- Tested device connectivity across the simulated network.
- Identified security-control gaps and documented recommended countermeasures.

**Reported outcome:** The VLAN-based network zones were separated successfully, and the connectivity tests reported 0% packet loss.

### Part 2 — Secure Hybrid Remote Access

**Objective:** Design connectivity for users accessing campus resources from on-campus and remote locations.

- Added a home router to represent remote connectivity.
- Created a WAN link using the `200.1.1.0/30` network.
- Updated the topology to support communication between campus and home networks.
- Designed role-based access policies for different user groups.
- Simulated a VPN/SASE-based secure-access model.

**Reported outcome:** The report records successful simulated remote connectivity with 0% packet loss.

*Note: VPN/SASE concepts are represented in a simulated network design; this does not imply deployment of a production VPN or SASE service.*

### Part 3 — Smart Web Filtering & Policy Framework

**Objective:** Control network access according to user roles and security policies.

- Added a filtering appliance and Syslog server to the topology.
- Designed ACL-based filtering rules for students, faculty, and servers.
- Defined restrictions for streaming and social-media traffic during class hours.
- Designed broader faculty access with monitoring.
- Restricted server communication to internal traffic.
- Configured Syslog-based logging and alerts for policy-violation attempts.

**Reported outcome:** The project report describes successful simulated filtering, access control, and logging.

*Note: Time-based and content-category filtering are documented as policy goals. Actual enforcement depends on the capabilities and configuration of the simulated devices.*

## Testing & Results

The project report documents the following outcomes:

| Test area | Reported result |
|---|---|
| VLAN segmentation | Network zones separated successfully |
| Inter-VLAN routing | Connectivity verified |
| Hybrid connectivity | 0% packet loss reported |
| ACL-based filtering | Access-control policies simulated |
| Syslog monitoring | Violation logging and alerts reported |

These results describe the project report's findings. Individual test screenshots and device configurations can be added to this repository to provide further verification.

## Repository Structure

```text
Secure-Campus-Network-Design/
│
├── README.md
├── Part1PacketTracer.pkt
├── Part2PacketTracer[1].pkt
├── Part3PacketTracer[1] (1).pkt
│
├── reports/
│   ├── sipptt.pdf
│   ├── PacketTracerPart1Report.pdf
│   ├── PacketTracerPart2Report.pdf
│   └── PacketTracerPart3Report.pdf
│
├── screenshots/
│   ├── network-topology.png
│   ├── vlan-configuration.png
│   ├── connectivity-test.png
│   └── security-logging.png
│
└── demo/
    └── demo-link.md
```

*The structure above is a suggested organization. Rename the files or folders as needed when uploading your actual project.*

## How to Run the Project

1. Install Cisco Packet Tracer on your computer.
2. Clone or download this repository.
3. Open the required `.pkt` file in Cisco Packet Tracer.
4. Inspect the logical topology and device connections.
5. Open the router or switch CLI to review the available configurations.
6. Use `show vlan brief` to inspect VLAN membership on supported switches.
7. Use `show ip interface brief` to inspect interface status and addressing.
8. Use `show access-lists` where supported to inspect configured ACLs.
9. Test connectivity using `ping` from the relevant end devices.
10. Use Simulation Mode to inspect packet movement and document the observed results.

Commands and results may differ depending on the device model and configuration used in each simulation file.

## Live Demo

**Demo video:** Add your YouTube or other publicly accessible video link here.

The walkthrough should demonstrate:

- Network topology and trust zones.
- VLAN and routing configurations.
- Connectivity tests.
- Configured ACL rules and their observed effects.
- Syslog events and security monitoring, where implemented.

**Project report:** See `sipptt.pdf` and the individual part reports in the `reports/` directory.

## Future Improvements

- Integrate centralized authentication using RADIUS/AAA.
- Explore real firewall appliances such as FortiGate or Palo Alto.
- Implement and validate IDS/IPS capabilities.
- Extend the remote-access architecture using a cloud-based SASE solution.
- Add detailed screenshots, repeatable test cases, and configuration documentation.
- Validate filtering behavior against additional positive and negative test cases.

## Learning Outcomes

This project provided practical exposure to:

- Network segmentation and trust-zone design.
- Inter-VLAN routing and network connectivity troubleshooting.
- ACL-based access control and security-policy design.
- Hybrid network architecture and remote-access concepts.
- Security monitoring, logging, and documentation.
- Network simulation and cybersecurity risk assessment.
