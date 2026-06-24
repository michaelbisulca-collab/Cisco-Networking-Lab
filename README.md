
# Cisco Networking Lab

## Overview

This project demonstrates the design and implementation of a multi-VLAN network using Cisco Packet Tracer. The lab simulates a small business environment with multiple departments separated into VLANs while maintaining controlled communication through routing and access control policies.

## Technologies and Concepts

* Cisco Packet Tracer
* Cisco IOS
* VLAN Configuration
* 802.1Q Trunking
* Router-on-a-Stick
* Inter-VLAN Routing
* DHCP
* Access Control Lists (ACLs)
* Network Troubleshooting

## Network Design

The network consists of three VLANs:

| VLAN | Department | Network         |
| ---- | ---------- | --------------- |
| 10   | Sales      | 198.168.10.0/24 |
| 20   | Office     | 198.168.20.0/24 |
| 30   | IT         | 198.168.30.0/24 |

Router subinterfaces were configured to provide gateway functionality for each VLAN:

* VLAN 10 Gateway: 198.168.10.1
* VLAN 20 Gateway: 198.168.20.1
* VLAN 30 Gateway: 198.168.30.1

## Features Implemented

### VLAN Segmentation

Created separate VLANs to logically divide devices into independent network segments.

### 802.1Q Trunking

Configured a trunk connection between the switch and router to carry traffic for multiple VLANs across a single physical link.

### Inter-VLAN Routing

Implemented Router-on-a-Stick using router subinterfaces to enable communication between VLANs.

### DHCP Services

Configured separate DHCP pools for each VLAN to automatically assign IP addresses, subnet masks, and default gateways.

### Access Control Lists (ACLs)

Implemented ACLs to restrict communication from VLAN 20 to other network segments, demonstrating basic network security and traffic filtering.

## Verification and Testing

The following Cisco IOS commands were used to verify network functionality:

show vlan brief
show ip interface brief
show ip route
show ip dhcp binding
show access-lists

Testing included:
* DHCP address assignment verification
* Inter-VLAN connectivity testing
* ACL enforcement testing
* Routing verification

## Skills Demonstrated

* Network segmentation using VLANs
* Cisco switch and router configuration
* DHCP deployment and troubleshooting
* Inter-VLAN routing configuration
* Access control implementation
* Network troubleshooting and verification
* Cisco IOS command-line administration
