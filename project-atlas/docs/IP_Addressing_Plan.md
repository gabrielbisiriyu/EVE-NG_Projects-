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
| 10.255.255.0/30 | HQ-DSW1 ↔ HQ-R1 |
| 10.255.255.4/30 | HQ-DSW2 ↔ HQ-R1 |
| 10.255.255.8/30 | HQ-DSW1 ↔ HQ-DSW2 |

- HQ-DSW1: **10.255.255.1**
- HQ-DSW2: **10.255.255.5**
- HQ-R1: **10.255.255.2**
- HQ-R1: **10.255.255.6**

---

## Current Static Addresses

| Device | Interface | IP Address |
|---------|-----------|------------|
| HQ-DSW1 | VLAN95 | 10.10.95.11 |              
| HQ-DSW1 | VLAN10 | 10.10.10.252 |                
| HQ-DSW1 | VLAN20 | 10.10.20.252 |    
| HQ-DSW1 | VLAN30 | 10.10.30.252 |    
| HQ-DSW1 | VLAN40 | 10.10.40.252 |     
| HQ-DSW1 | VLAN50 | 10.10.50.252 |   
| HQ-DSW1 | e0/0   | 10.255.255.1 |    
| HQ-DSW1 | po1(e1/0-3)| 10.255.255.9 |  
| HQ-DSW2 | VLAN95 | 10.10.95.12 |    
| HQ-DSW2 | VLAN10 | 10.10.10.253 |   
| HQ-DSW2 | VLAN20 | 10.10.20.253 |    
| HQ-DSW2 | VLAN30 | 10.10.30.253 |    
| HQ-DSW2 | VLAN40 | 10.10.40.253 |    
| HQ-DSW2 | VLAN50 | 10.10.50.253 |  
| HQ-DSW2 | e0/0   | 10.255.255.5 |  
| HQ-DSW1 | po1(e1/0-3) | 10.255.255.10 |  
| HQ-R1 | Ethernet0/0 | 10.255.255.2 |
| HQ-R1 | Ethernet0/1 | 10.255.255.6 |
| Ubuntu Server | ens3 | 10.10.50.10 |