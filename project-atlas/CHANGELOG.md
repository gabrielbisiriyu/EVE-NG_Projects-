# Changelog

## Version 0.3.0

### Added

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

### Added

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

### Added

* Created Project Atlas repository
* Built headquarters initial topology in EVE-NG
* Created Layer 2 enterprise topology
* Defined VLAN plan
* Configured VLANs
* Configured trunk links
* Configured basic switch security
