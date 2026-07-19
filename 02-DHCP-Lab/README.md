# DHCP Server Configuration Lab

## Objective
Configure a DHCP server to automatically assign IP addresses to devices across multiple VLANs (10, 20, and 30).



##  Network Design

### VLAN Configuration

| VLAN | Network | Gateway | Purpose |
|------|---------|---------|---------|
| VLAN 10 | 192.168.10.0/24 | 192.168.10.1 | User VLAN 1 |
| VLAN 20 | 192.168.20.0/24 | 192.168.20.1 | User VLAN 2 |
| VLAN 30 | 192.168.30.0/24 | 192.168.30.1 | Server/Management VLAN |


##  Device Inventory

### Router0 (2911)

| Interface | IP Address | Connected To |
|-----------|------------|--------------|
| Gig0/0 | 192.168.10.1 | Switch1 (VLAN 10) |
| Gig0/1 | 192.168.20.1 | Switch2 (VLAN 20) |
| Gig0/2 | 192.168.30.1 | Switch3 (VLAN 30) |

### DHCP Server0

| Interface | IP Address | VLAN |
|-----------|------------|------|
| 192.168.30.2 | VLAN 30 |

### Switches

| Switch | VLAN | Gateway | Connected PCs |
|--------|------|---------|---------------|
| Switch1 | VLAN 10 | 192.168.10.1 | PC0, PC1, PC2, PC3, PC4, PC5, PC6, PC7 |
| Switch2 | VLAN 20 | 192.168.20.1 | PC8, PC9, PC10, PC11, PC12, PC13, PC14, PC15 |
| Switch3 | VLAN 30 | 192.168.30.1 | PC16, PC17, PC18, PC19 |

