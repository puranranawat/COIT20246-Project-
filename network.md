## Assumptions

The project scenario does not specify all organisational and technical details. Therefore, the following assumptions have been made to support the proposed network design. These assumptions are realistic, comply with the project requirements, and represent a medium-sized Australian organisation.

### Headquarters Location

The headquarters of Truelec is assumed to be located in Brisbane, Queensland, Australia.

Justification:  
Brisbane is a major Australian metropolitan city with well-developed ICT infrastructure, access to enterprise-grade internet service providers, and a skilled professional workforce. These factors make it a suitable location for hosting the organisation’s central administrative, operational, and IT services.

### Branch Office Locations

The organisation is assumed to operate three branch offices in the following Australian cities:
- Perth, Western Australia  
- Adelaide, South Australia  
- Hobart, Tasmania  

Justification:  
These locations align with the scenario description and provide broad geographic coverage across Australia. Each city supports industrial, construction, and infrastructure-related activities, which are relevant to the organisation’s operations.

### Number of Staff at Headquarters

The headquarters is assumed to employ 60 staff members.

Justification:  
This figure falls within the required range of 50 to 75 staff and represents a medium-sized headquarters comprising senior management, project managers, marketing personnel, and ICT staff. It also allows sufficient capacity for future growth.

### Number of Staff at Branch Office

Each branch office is assumed to employ 20 staff members.

Justification:  
This number satisfies the requirement of 15 to 30 staff per branch office and reflects a typical operational branch consisting of electricians, electrical engineers, site supervisors, and administrative support staff.

### Scope of Branch Network Design

For this project, a detailed network design is provided for one branch office. It is assumed that the remaining branch offices will implement a similar network architecture and configuration.

Justification:  
Branch offices are expected to have comparable operational requirements. Designing a single branch network provides a scalable and repeatable model that can be consistently applied to other branch locations.








## 4.1.2 IP Addressing Plan

A structured IP addressing scheme has been designed to support the headquarters and branch office networks. The addressing plan ensures logical separation of network segments, scalability, and ease of management. All IP address ranges comply with the project requirements, using only /16 or /24 network masks, and the first octet of all IP addresses is based on the last two digits of a group member’s student ID.

### IP Addressing Design Principles

The following principles were applied when designing the IP addressing scheme:
- Clear separation between headquarters and branch office networks
- Dedicated address ranges for servers and wireless networks
- Use of summarised address blocks to allow future expansion
- Compliance with public-style addressing, avoiding private IP ranges

---

### Headquarters IP Address Allocation

| Network Segment | Purpose | IP Address Range | Subnet Mask |
|-----------------|---------|------------------|-------------|
| HQ Wired LAN | Wired user devices and office systems | 22.10.0.0/16 | 255.255.0.0 |
| HQ Wireless LAN | Staff wireless devices | 22.20.0.0/24 | 255.255.255.0 |
| HQ Server Network | Internal servers and application services | 22.30.0.0/24 | 255.255.255.0 |
| HQ Security Devices | CCTV, IoT sensors, RFID access systems | 22.40.0.0/24 | 255.255.255.0 |

Justification:  
A /16 network has been allocated to the headquarters wired LAN to support a larger number of devices and allow future growth. Separate /24 networks are used for wireless access, servers, and security devices to improve organisation, manageability, and fault isolation.

---

### Branch Office IP Address Allocation

| Network Segment | Purpose | IP Address Range | Subnet Mask |
|-----------------|---------|------------------|-------------|
| Branch Wired LAN | Branch office wired devices | 22.50.0.0/24 | 255.255.255.0 |
| Branch Wireless LAN | Branch staff wireless devices | 22.60.0.0/24 | 255.255.255.0 |

Justification:  
Each branch office is assigned separate /24 networks for wired and wireless connectivity. This provides sufficient address space for branch operations while maintaining simplicity and consistency across branch locations.

---

### Scalability and Future Expansion

The IP addressing scheme allows additional networks and devices to be added without major restructuring. Additional branch offices can be allocated new /24 networks following the same addressing pattern, ensuring consistency across the organisation.

---

### Summary

This IP addressing plan provides a logical, scalable, and standards-compliant structure for the organisation’s network. It supports current operational requirements while allowing for future expansion and simplified network management.

