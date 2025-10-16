# Nqobile-Msiza-CMPG-325-PROJECT Part 1

# Overview

This report contains the design, implementation, and analysis of five network topologies which are: (Bus, Mesh, Star, Ring, and Extended Star) and one hybrid topology (bus topology) integrating elements from all basic types. Each topology was implemented with using IPv4/IPv6 addressing, VLAN segmentation, essential network services which were these two (HTTP, DNS), and basic security measures such as a password for each server was configured. The simulations illustrate the network device configurations, IP addressing and data packet transmission.

# 1. Methodology & Tools
   
1.1 Simulation Environment
•	Primary Tool: Cisco Packet Tracer
•	Simulation Focus: Network connectivity, protocol behaviour, service integration, and basic security implementation.
•	Topologies Implemented:
o	5 Basic Topologies: Bus, Mesh, Star, Ring, Extended Star.
o	Hybrid Topology: Bus topology serving as the backbone connecting all other topologies.
-Network Devices: Switches only (no routers implemented).

# 1.2 Consistent Addressing Scheme

An integrated IP addressing plan was implemented across all topologies:
IPv4 Scheme: 192.168.1.X (where X = different value for each PC)
-Topology Assignments:
o	Bus/Hybrid Backbone: 192.168.1.X (Contains central server)
o	Star: 192.168.1.X
o	Ring: 192.168.1.X
o	Mesh: 192.168.1.X
o	Extended Star: 192.168.1.X
-Central Server: 192.168.1.X (Located on Bus/Hybrid topology
-End Devices: 192.168.1.X
     IPv6 Scheme: 2003:DB8:X: :/64
-Central Server: 2003:DB8:X: :/64(Located on Bus/Hybrid topology)
-End Devices: 2003:DB8:X: :/64 - 2003:DB8:X: :/64

# 1.3 Cable Implementation

•	Bus/Hybrid Topology: Coaxial cables with terminators (central backbone)
•	Other Topologies:
-Copper Straight-Through: PC to Switch connections
-Copper Crossover: Switch to Switch connections
-Connection to Bus: Each topology connected to the central bus backbone.

# 1.4 Service Implementation

Centralized Server Approach: A single server located on the Bus/Hybrid backbone provided services to all connected topologies:
•	DNS Service: Centralized name resolution accessible from all topologies
•	HTTP Service: Web hosting available network-wide
     -Server Location: Bus/Hybrid backbone (192.168.1.48)

# 1.5 Basic Security Implementation

Manual Password Configuration: Every switch in all topologies was secured with individual password configuration:
-Enable Secret Passwords: Configured for privileged EXEC mode access
-Console Passwords: Set for physical console access security
-CLI Configuration: All security implemented through command-line interface
-Individual Switch Setup: Each switch configured manually via CLI



# IP ADDRESS TABLE

| **Device** | **IPv4 Address** | **Subnet Mask** | **IPv6 Address** | **Gateway** |
|-------------|------------------|------------------|------------------|-------------|
| PC9        | 192.168.1.1      | 255.255.255.0    | 2003:DB8:1::1/64  | 192.168.1.254 |
| PC11       | 192.168.1.2      | 255.255.255.0    | 2003:DB8:1::2/64  | 192.168.1.254 |
| PC12       | 192.168.1.3      | 255.255.255.0    | 2003:DB8:1::3/64  | 192.168.1.254 |
| PC13       | 192.168.1.4      | 255.255.255.0    | 2003:DB8:1::4/64  | 192.168.1.254 |
| PC25       | 192.168.1.5      | 255.255.255.0    | 2003:DB8:1::5/64  | 192.168.1.254 |
| PC15       | 192.168.1.6      | 255.255.255.0    | 2003:DB8:1::6/64  | 192.168.1.254 |
| PC16       | 192.168.1.7      | 255.255.255.0    | 2003:DB8:1::7/64  | 192.168.1.254 |
| PC17       | 192.168.1.8      | 255.255.255.0    | 2003:DB8:1::8/64  | 192.168.1.254 |
| PC18       | 192.168.1.9      | 255.255.255.0    | 2003:DB8:1::9/64  | 192.168.1.254 |
| Laptop4    | 192.168.1.10     | 255.255.255.0    | 2003:DB8:1::10/64 | 192.168.1.254 |
| PC22       | 192.168.1.11     | 255.255.255.0    | 2003:DB8:1::11/64 | 192.168.1.254 |
| PC20       | 192.168.1.12     | 255.255.255.0    | 2003:DB8:1::12/64 | 192.168.1.254 |
| Laptop3    | 192.168.1.13     | 255.255.255.0    | 2003:DB8:1::13/64 | 192.168.1.254 *(ORGAN)* |
| PC23       | 192.168.1.14     | 255.255.255.0    | 2003:DB8:1::14/64 | 192.168.1.254 |
| PC24       | 192.168.1.15     | 255.255.255.0    | 2003:DB8:1::15/64 | 192.168.1.254 |
| Laptop5    | 192.168.1.16     | 255.255.255.0    | 2003:DB8:1::16/64 | 192.168.1.254 |
| Laptop6    | 192.168.1.17     | 255.255.255.0    | 2003:DB8:1::17/64 | 192.168.1.254 |
| PC26       | 192.168.1.18     | 255.255.255.0    | 2003:DB8:1::18/64 | 192.168.1.254 |
| PC27       | 192.168.1.19     | 255.255.255.0    | 2003:DB8:1::19/64 | 192.168.1.254 |
| Laptop7    | 192.168.1.20     | 255.255.255.0    | 2003:DB8:1::20/64 | 192.168.1.254 |
| PC28       | 192.168.1.21     | 255.255.255.0    | 2003:DB8:1::21/64 | 192.168.1.254 |
| PC29       | 192.168.1.22     | 255.255.255.0    | 2003:DB8:1::22/64 | 192.168.1.254 |
| PC30       | 192.168.1.23     | 255.255.255.0    | 2003:DB8:1::23/64 | 192.168.1.254 |
| PC31       | 192.168.1.24     | 255.255.255.0    | 2003:DB8:1::24/64 | 192.168.1.254 |
| PC32       | 192.168.1.25     | 255.255.255.0    | 2003:DB8:1::25/64 | 192.168.1.254 |
| PC33       | 192.168.1.26     | 255.255.255.0    | 2003:DB8:1::26/64 | 192.168.1.254 |
| Server0    | 192.168.1.48     | 255.255.255.0    | *Not Configured*  | 192.168.1.254 |

# Configuration Notes

# For VLAN segmentation:
>>enable
>>configure terminal
>>interface vlan1
>>ip address 192.168.1.X 255.255.255.0
>>no shutdown
>>exit until conf is gone

# For basic security (on each switch under CLI):
Switch>enable
Switch#configure terminal
Switch(config)#enable password @123Nqobile
Switch(config)# exit

# Nqobile-Msiza-CMPG-325-PROJECT Part 2

# Project Overview

Successfully implemented and demonstrated Border Gateway Protocol (BGP) for inter-domain routing between two autonomous systems (AS 65001 and AS 65002) using a physical lab setup consisting of 4 PCs, 2 switches, and 2 routers.

# IP Address Table

| **End Device** | **IPv4 Address** | **IPv6 Address** |
|-----------------|------------------|------------------|
| PC0 | 198.168.1.2 | 2003:DB8:1::2/64 |
| PC1 | 198.168.1.3 | 2003:DB8:1::3/64 |
| PC2 | 198.168.2.2 | 2003:DB8:2::2/64 |
| PC3 | 198.168.2.3 | 2003:DB8:2::3/64 |
| Router1 | 198.168.1.1 | — |
| Router2 | 198.168.2.1 | — |

# Configuration Notes:

# 1. Basic Router Configuration
Router A (AS 65001)

enable
configure terminal
hostname RouterA

! Configure Interfaces
interface gigabitethernet0/0
 description Internal Network AS65001
 ip address 192.168.10.1 255.255.255.0
 no shutdown
 exit

interface gigabitethernet0/1
 description eBGP Link to AS65002
 ip address 10.0.0.1 255.255.255.252
 no shutdown
 exit

interface loopback0
 ip address 1.1.1.1 255.255.255.255
 exit
 
 Router B (AS 65002)
 enable
configure terminal
hostname RouterB

! Configure Interfaces
interface gigabitethernet0/0
 description Internal Network AS65002
 ip address 192.168.20.1 255.255.255.0
 no shutdown
 exit

interface gigabitethernet0/1
 description eBGP Link to AS65001
 ip address 10.0.0.2 255.255.255.252
 no shutdown
 exit

interface loopback0
 ip address 2.2.2.2 255.255.255.255
 exit

# 2. BGP Configuration
Router A BGP Setup
router bgp 65001
 bgp router-id 1.1.1.1
 bgp log-neighbor-changes
 network 192.168.10.0 mask 255.255.255.0
 neighbor 10.0.0.2 remote-as 65002
 neighbor 10.0.0.2 description eBGP_Peer_RouterB_AS65002
 no auto-summary
 exit

! Static route for network advertisement
ip route 192.168.10.0 255.255.255.0 null0

router bgp 65002
 bgp router-id 2.2.2.2
 bgp log-neighbor-changes
 network 192.168.20.0 mask 255.255.255.0
 neighbor 10.0.0.1 remote-as 65001
 neighbor 10.0.0.1 description eBGP_Peer_RouterA_AS65001
 no auto-summary
 exit

! Static route for network advertisement
ip route 192.168.20.0 255.255.255.0 null0

# 3. Switch Configuration
Switch A (for AS 65001)

enable
configure terminal
hostname SwitchA
Switch B (for AS 65002)
vlan 10
 name AS65001_USERS
 exit

interface range fastethernet0/1-2
 switchport mode access
 switchport access vlan 10
 no shutdown
 exit

interface gigabitethernet0/1
 switchport mode trunk
 no shutdown
 exit

 Switch B (for AS 65002)
enable
configure terminal
hostname SwitchB

vlan 20
 name AS65002_USERS
 exit

interface range fastethernet0/1-2
 switchport mode access
 switchport access vlan 20
 no shutdown
 exit

interface gigabitethernet0/1
 switchport mode trunk
 no shutdown
 exit

 # 4. Verification Commands
BGP Verification
! Check BGP neighbors
show ip bgp summary
show ip bgp neighbors

! Check BGP routing table
show ip bgp
show ip route bgp

! Detailed BGP information
show ip bgp 192.168.20.0
show ip bgp paths

Connectivity Testing
! Basic ping tests
ping 10.0.0.2
ping 192.168.20.1

! Extended ping with source
ping
Protocol [ip]:
Target IP address: 192.168.20.20
Repeat count: 5
Datagram size: 1000
Timeout in seconds: 2
Extended commands [n]: y
Source address or interface: 192.168.10.1

Interface & Routing Verification

! Check interface status
show ip interface brief
show interfaces description

! Check routing table
show ip route
show ip route connected

! Check protocol status
show ip protocols

# 5. Troubleshooting Commands
BGP Troubleshooting

! Debug BGP events (use cautiously)
debug ip bgp
debug ip bgp events
debug ip bgp updates

! Clear BGP sessions if needed
clear ip bgp *
clear ip bgp 10.0.0.2

Connectivity Issues

! Trace the path
traceroute 192.168.20.20

! Check ARP tables
show arp
show ip arp

! Check MAC address tables on switches
show mac address-table
show vlan brief
 
