# VLAN Plan

## Project Atlas

| VLAN ID | Name | Purpose | Subnet | Default Gateway |
|---------:|------|---------|--------|-----------------|
| 10 | IT | Information Technology Department | 10.10.10.0/24 | 10.10.10.254 |
| 20 | HR | Human Resources Department | 10.10.20.0/24 | 10.10.20.254 |
| 30 | FINANCE | Finance Department | 10.10.30.0/24 | 10.10.30.254 |
| 40 | SALES | Sales Department | 10.10.40.0/24 | 10.10.40.254 |
| 50 | SERVERS | Enterprise Servers | 10.10.50.0/24 | 10.10.50.254 |
| 95 | MANAGEMENT | Network Device Management | 10.10.95.0/24 | 10.10.95.1 |
| 99 | NATIVE | Native VLAN for Trunk Links | N/A | N/A |

## Notes

- User traffic is separated into departmental VLANs.
- VLAN 50 hosts enterprise servers.
- VLAN 95 is reserved for management traffic.
- VLAN 99 is configured as the native VLAN on all trunk links.