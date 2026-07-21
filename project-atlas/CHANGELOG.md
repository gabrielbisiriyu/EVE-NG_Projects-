# Changelog


## Version 0.5.0

### Enterprise Access Layer Security

- Enabled PortFast on end-device interfaces
- Enabled BPDU Guard on access ports
- Implemented DHCP Snooping
- Configured trusted and untrusted DHCP ports
- Applied DHCP Snooping rate limiting on user-facing interfaces
- Implemented Dynamic ARP Inspection (DAI) on user VLANs
- Configured Port Security using sticky MAC learning
- Configured secure MAC address limits and violation actions

---

## Version 0.4.0

### Campus Core Redundancy & High Availability

- Redesigned the campus topology into a dual-distribution architecture
- Added HQ-DSW1 and HQ-DSW2 as redundant distribution switches
- Implemented Layer 3 EtherChannel (LACP) between distribution switches
- Configured trunked Port-Channel carrying all enterprise VLANs
- Dual-homed all access switches to both distribution switches
- Implemented HSRP gateway redundancy across user VLANs
- Configured HSRP load balancing between distribution switches
- Updated DNS records for renamed infrastructure devices
- Updated enterprise topology documentation
- Added management IP addresses for new infrastructure devices

---


## Version 0.3.0

#### Enterprise Infrastructure Services

* Configured ISC DHCP Server
* Configured DHCP Relay (`ip helper-address`) on Layer 3 SVIs
* Created DHCP scopes for enterprise VLANs
* Deployed BIND9 DNS Server
* Configured forward lookup zones
* Configured reverse lookup zones
* Implemented local enterprise DNS namespace (`atlas.local`)
* Configured recursive DNS forwarding
* Deployed Apache Web Server
* Hosted internal company website (`www.atlas.local`)
* Deployed Samba File Server
* Created departmental shared folders
* Configured shared folder permissions
* Verified file upload and download from Windows and Linux clients
* Verified DNS name resolution across multiple VLANs

---

## Version 0.2.0

### Enterprise Routing & Network Foundation

* Configured management VLAN (VLAN 95)
* Configured Switch Virtual Interfaces (SVIs) for inter-VLAN routing
* Configured static routing between HQ-SW1 and HQ-R1
* Configured SSH secure remote management
* Configured management access control list (ACL)
* Configured WAN connectivity to VMware Cloud
* Configured NAT/PAT for Internet access
* Connected Ubuntu Server to the enterprise network
* Configured static IP addressing for Ubuntu Server
* Verified end-to-end Internet connectivity

---

## Version 0.1.0

### Initial Enterprise Network Deployment

* Created Project Atlas repository
* Built headquarters initial topology in EVE-NG
* Created Layer 2 enterprise topology
* Defined VLAN plan
* Configured VLANs
* Configured trunk links

