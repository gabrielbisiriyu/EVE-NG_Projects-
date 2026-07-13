# IP Addressing Plan

## Project Atlas

### VLAN Networks

| Network | Purpose | Gateway |
|---------|---------|---------|
| 10.10.10.0/24 | IT | 10.10.10.254 |
| 10.10.20.0/24 | HR | 10.10.20.254 |
| 10.10.30.0/24 | Finance | 10.10.30.254 |
| 10.10.40.0/24 | Sales | 10.10.40.254 |
| 10.10.50.0/24 | Servers | 10.10.50.254 |
| 10.10.95.0/24 | Management | 10.10.95.1 |

---

## WAN Transit Network

| Network | Devices |
|---------|---------|
| 10.255.255.0/30 | HQ-SW1 ↔ HQ-R1 |

- HQ-SW1: **10.255.255.1**
- HQ-R1: **10.255.255.2**

---

## Current Static Addresses

| Device | Interface | IP Address |
|---------|-----------|------------|
| HQ-SW1 | VLAN95 | 10.10.95.1 |
| HQ-SW1 | VLAN10 | 10.10.10.254 |
| HQ-SW1 | VLAN20 | 10.10.20.254 |
| HQ-SW1 | VLAN30 | 10.10.30.254 |
| HQ-SW1 | VLAN40 | 10.10.40.254 |
| HQ-SW1 | VLAN50 | 10.10.50.254 |
| HQ-R1 | Ethernet0/0 | 10.255.255.2 |
| Ubuntu Server | ens3 | 10.10.50.10 |