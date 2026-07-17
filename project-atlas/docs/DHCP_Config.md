# DHCP Server Configuration

## Overview

Project Atlas uses an Ubuntu Server running the ISC DHCP Server to automatically assign IPv4 addresses to end devices across multiple VLANs.

Rather than deploying a DHCP server in every subnet, a centralized DHCP server is used together with DHCP Relay (`ip helper-address`) configured on the Layer 3 switch.

---

## DHCP Server

* Operating System: Ubuntu Server 20.04
* DHCP Software: ISC DHCP Server
* Server IP: 10.10.50.10

---

## Configuration Files

Main configuration file:

```text
/etc/dhcp/dhcpd.conf
```

Interface configuration:

```text
/etc/default/isc-dhcp-server
```

---

## Implementation

The DHCP server contains a subnet declaration for every VLAN.

Each subnet defines:

* Network address
* Subnet mask
* Default gateway
* DNS server
* Domain name
* DHCP address pool
* Lease timers

---

## DHCP Relay

Since the DHCP server is located in the Server VLAN, broadcasts from client VLANs cannot reach it directly.

To solve this, DHCP Relay (`ip helper-address`) was configured on each Layer 3 Switch Virtual Interface (SVI).

This converts DHCP broadcasts into unicast packets destined for the DHCP server.

---

## Verification

The implementation was verified by confirming that client devices automatically received:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server
* Domain Name

using DHCP.

---


