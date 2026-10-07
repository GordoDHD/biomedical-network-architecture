# Secure Hospital Network

This project is a simulation of a hospital network built with Cisco Packet Tracer / GNS3.

The main idea is to keep the different parts of the network separated. Medical devices, EHR systems, staff PCs and guest users are placed in different VLANs, with ACLs used to control which networks can communicate with each other.

## Network Setup

The network is divided into four VLANs:

* **VLAN 10 – Medical Devices:** EKG, MRI and PACS workstations. This VLAN is isolated from the Internet.
* **VLAN 20 – EHR:** Servers and workstations related to electronic health records.
* **VLAN 30 – Staff:** PCs used by hospital staff for normal internal activities.
* **VLAN 40 – Guest Wi-Fi:** For visitors. Guests can access the Internet but cannot reach the internal network.

## Technologies

The project uses:

* Cisco Packet Tracer / GNS3
* VLANs
* Inter-VLAN Routing
* OSPF
* NAT/PAT
* ACLs
* Port Security
* DHCP Snooping
* Dynamic ARP Inspection
* STP

## Security

ACLs are used to control traffic between the different VLANs. For example, access to the PACS and biomedical systems is only allowed from the networks that need it.

Port Security is configured on the access ports to limit which devices can connect to the switches.

DHCP Snooping and Dynamic ARP Inspection are also enabled to protect the network against common Layer 2 attacks.

STP is used to avoid switching loops.

## Repository

```text
/configs/
    Cisco IOS configuration files

/topology/
    Packet Tracer topology (.pkt)
```

The project is mainly meant to show how network segmentation and basic security controls can be used in a healthcare environment.
