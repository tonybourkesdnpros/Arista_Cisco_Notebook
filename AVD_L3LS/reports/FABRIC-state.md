
# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed |
| ----------- | ------------------ | ------------------ |
| 411 | 359 | 52 |

### Summary Totals Devices Under Tests

| DUT | Total Tests | Tests Passed | Tests Failed | Categories Failed |
| --- | ----------- | ------------ | ------------ | ----------------- |
| borderleaf1 |  44 | 30 | 14 | Interface State, LLDP Topology, IP Reachability, BGP, Routing Table, Loopback0 Reachability |
| borderleaf2 |  44 | 30 | 14 | Interface State, LLDP Topology, IP Reachability, BGP, Routing Table, Loopback0 Reachability |
| leaf1 |  56 | 55 | 1 | Interface State |
| leaf2 |  56 | 55 | 1 | Interface State |
| leaf3 |  56 | 55 | 1 | Interface State |
| leaf4 |  56 | 55 | 1 | Interface State |
| spine1 |  33 | 23 | 10 | Interface State, LLDP Topology, IP Reachability, BGP |
| spine2 |  33 | 23 | 10 | Interface State, LLDP Topology, IP Reachability, BGP |
| spine3 |  33 | 33 | 0 | - |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed |
| ------------- | ----------- | ------------ | ------------ |
| NTP |  9 | 9 | 0 |
| Interface State |  101 | 89 | 12 |
| LLDP Topology |  44 | 36 | 8 |
| MLAG |  4 | 4 | 0 |
| IP Reachability |  36 | 28 | 8 |
| BGP |  85 | 69 | 16 |
| Routing Table |  78 | 74 | 4 |
| Loopback0 Reachability |  54 | 50 | 4 |

## Failed Test Results Summary

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 10 | borderleaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet7 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 11 | borderleaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet7 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 13 | borderleaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet8 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 14 | borderleaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet8 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 44 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - P2P_LINK_TO_BORDERLEAF1_Ethernet3 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 45 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - P2P_LINK_TO_BORDERLEAF2_Ethernet3 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 50 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - P2P_LINK_TO_BORDERLEAF1_Ethernet4 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 51 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - P2P_LINK_TO_BORDERLEAF2_Ethernet4 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 59 | leaf1 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host1_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 61 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host1_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 63 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host2_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 65 | leaf4 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host2_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 111 | borderleaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet7 | FAIL | Interface Down - N/A |
| 112 | borderleaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet7 | FAIL | Interface Down - N/A |
| 114 | borderleaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet8 | FAIL | Interface Down - N/A |
| 115 | borderleaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet8 | FAIL | Interface Down - N/A |
| 141 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet7 - remote: borderleaf1_Ethernet3 | FAIL | Interface Down - N/A |
| 142 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet8 - remote: borderleaf2_Ethernet3 | FAIL | Interface Down - N/A |
| 147 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet7 - remote: borderleaf1_Ethernet4 | FAIL | Interface Down - N/A |
| 148 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet8 - remote: borderleaf2_Ethernet4 | FAIL | Interface Down - N/A |
| 159 | borderleaf1 | IP Reachability | ip reachability test p2p links | Source: borderleaf1_Ethernet3 - Destination: spine1_Ethernet7 | FAIL | 100% packet loss |
| 160 | borderleaf1 | IP Reachability | ip reachability test p2p links | Source: borderleaf1_Ethernet4 - Destination: spine2_Ethernet7 | FAIL | 100% packet loss |
| 162 | borderleaf2 | IP Reachability | ip reachability test p2p links | Source: borderleaf2_Ethernet3 - Destination: spine1_Ethernet8 | FAIL | 100% packet loss |
| 163 | borderleaf2 | IP Reachability | ip reachability test p2p links | Source: borderleaf2_Ethernet4 - Destination: spine2_Ethernet8 | FAIL | 100% packet loss |
| 181 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet7 - Destination: borderleaf1_Ethernet3 | FAIL | 100% packet loss |
| 182 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet8 - Destination: borderleaf2_Ethernet3 | FAIL | 100% packet loss |
| 187 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet7 - Destination: borderleaf1_Ethernet4 | FAIL | 100% packet loss |
| 188 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet8 - Destination: borderleaf2_Ethernet4 | FAIL | 100% packet loss |
| 204 | borderleaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.24 | FAIL | Session state Idle |
| 205 | borderleaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.26 | FAIL | Session state Idle |
| 207 | borderleaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.30 | FAIL | Session state Idle |
| 208 | borderleaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.32 | FAIL | Session state Idle |
| 230 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.25 | FAIL | Session state Idle |
| 231 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.31 | FAIL | Session state Idle |
| 236 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.27 | FAIL | Session state Idle |
| 237 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.33 | FAIL | Session state Idle |
| 244 | borderleaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | FAIL | Session state: Active |
| 245 | borderleaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | FAIL | Session state: Active |
| 247 | borderleaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | FAIL | Session state: Active |
| 248 | borderleaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | FAIL | Session state: Active |
| 262 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.5 | FAIL | Session state: Active |
| 263 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.6 | FAIL | Session state: Active |
| 268 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.5 | FAIL | Session state: Active |
| 269 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.6 | FAIL | Session state: Active |
| 310 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.11 | FAIL | Lo0 192.168.101.11 is not in the routing table |
| 311 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.12 | FAIL | Lo0 192.168.101.12 is not in the routing table |
| 319 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.11 | FAIL | Lo0 192.168.101.11 is not in the routing table |
| 320 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.12 | FAIL | Lo0 192.168.101.12 is not in the routing table |
| 364 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.11 | FAIL | 100% packet loss |
| 365 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.12 | FAIL | 100% packet loss |
| 373 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.11 | FAIL | 100% packet loss |
| 374 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.12 | FAIL | 100% packet loss |

## All Test Results

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | borderleaf1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 2 | borderleaf2 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 3 | leaf1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 4 | leaf2 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 5 | leaf3 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 6 | leaf4 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 7 | spine1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 8 | spine2 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 9 | spine3 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 10 | borderleaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet7 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 11 | borderleaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet7 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 12 | borderleaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet7 | PASS | - |
| 13 | borderleaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet8 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 14 | borderleaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet8 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 15 | borderleaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet8 | PASS | - |
| 16 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf2_Ethernet1 | PASS | - |
| 17 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf2_Ethernet2 | PASS | - |
| 18 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet3 | PASS | - |
| 19 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet3 | PASS | - |
| 20 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet3 | PASS | - |
| 21 | leaf1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host1_Ethernet1 | PASS | - |
| 22 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf1_Ethernet1 | PASS | - |
| 23 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf1_Ethernet2 | PASS | - |
| 24 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet4 | PASS | - |
| 25 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet4 | PASS | - |
| 26 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet4 | PASS | - |
| 27 | leaf2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host1_Ethernet2 | PASS | - |
| 28 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf4_Ethernet1 | PASS | - |
| 29 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf4_Ethernet2 | PASS | - |
| 30 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet5 | PASS | - |
| 31 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet5 | PASS | - |
| 32 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet5 | PASS | - |
| 33 | leaf3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host2_Ethernet1 | PASS | - |
| 34 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - MLAG_PEER_leaf3_Ethernet1 | PASS | - |
| 35 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - MLAG_PEER_leaf3_Ethernet2 | PASS | - |
| 36 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_SPINE1_Ethernet6 | PASS | - |
| 37 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_SPINE2_Ethernet6 | PASS | - |
| 38 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_SPINE3_Ethernet6 | PASS | - |
| 39 | leaf4 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - host2_Ethernet2 | PASS | - |
| 40 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_LEAF1_Ethernet3 | PASS | - |
| 41 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_LEAF2_Ethernet3 | PASS | - |
| 42 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_LEAF3_Ethernet3 | PASS | - |
| 43 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - P2P_LINK_TO_LEAF4_Ethernet3 | PASS | - |
| 44 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - P2P_LINK_TO_BORDERLEAF1_Ethernet3 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 45 | spine1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - P2P_LINK_TO_BORDERLEAF2_Ethernet3 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 46 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_LEAF1_Ethernet4 | PASS | - |
| 47 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_LEAF2_Ethernet4 | PASS | - |
| 48 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_LEAF3_Ethernet4 | PASS | - |
| 49 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - P2P_LINK_TO_LEAF4_Ethernet4 | PASS | - |
| 50 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - P2P_LINK_TO_BORDERLEAF1_Ethernet4 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 51 | spine2 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - P2P_LINK_TO_BORDERLEAF2_Ethernet4 | FAIL | Interface shutdown: False - interface status: down - line protocol status: down |
| 52 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_LEAF1_Ethernet5 | PASS | - |
| 53 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_LEAF2_Ethernet5 | PASS | - |
| 54 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_LEAF3_Ethernet5 | PASS | - |
| 55 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - P2P_LINK_TO_LEAF4_Ethernet5 | PASS | - |
| 56 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - P2P_LINK_TO_BORDERLEAF1_Ethernet5 | PASS | - |
| 57 | spine3 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - P2P_LINK_TO_BORDERLEAF2_Ethernet5 | PASS | - |
| 58 | leaf1 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf2_Po1 | PASS | - |
| 59 | leaf1 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host1_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 60 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf1_Po1 | PASS | - |
| 61 | leaf2 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host1_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 62 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf4_Po1 | PASS | - |
| 63 | leaf3 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host2_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 64 | leaf4 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel1 - MLAG_PEER_leaf3_Po1 | PASS | - |
| 65 | leaf4 | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - host2_PortChannel host1 | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 66 | borderleaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 67 | borderleaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 68 | borderleaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 69 | borderleaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 70 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 71 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 72 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 73 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 74 | leaf1 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf VRF_A | PASS | - |
| 75 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 76 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 77 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 78 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 79 | leaf2 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf VRF_A | PASS | - |
| 80 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 81 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 82 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 83 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 84 | leaf3 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf VRF_A | PASS | - |
| 85 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 86 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 87 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - DMZ | PASS | - |
| 88 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - DMZ | PASS | - |
| 89 | leaf4 | Interface State | Vlan Interface & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf VRF_A | PASS | - |
| 90 | borderleaf1 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 91 | borderleaf2 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 92 | leaf1 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 93 | leaf2 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 94 | leaf3 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 95 | leaf4 | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 96 | borderleaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 97 | borderleaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 98 | borderleaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 99 | borderleaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 100 | leaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 101 | leaf1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 102 | leaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 103 | leaf2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 104 | leaf3 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 105 | leaf3 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 106 | leaf4 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 107 | leaf4 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 108 | spine1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 109 | spine2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 110 | spine3 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 111 | borderleaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet7 | FAIL | Interface Down - N/A |
| 112 | borderleaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet7 | FAIL | Interface Down - N/A |
| 113 | borderleaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet7 | PASS | - |
| 114 | borderleaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet8 | FAIL | Interface Down - N/A |
| 115 | borderleaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet8 | FAIL | Interface Down - N/A |
| 116 | borderleaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet8 | PASS | - |
| 117 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf2_Ethernet1 | PASS | - |
| 118 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf2_Ethernet2 | PASS | - |
| 119 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet3 | PASS | - |
| 120 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet3 | PASS | - |
| 121 | leaf1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet3 | PASS | - |
| 122 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf1_Ethernet1 | PASS | - |
| 123 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf1_Ethernet2 | PASS | - |
| 124 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet4 | PASS | - |
| 125 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet4 | PASS | - |
| 126 | leaf2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet4 | PASS | - |
| 127 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf4_Ethernet1 | PASS | - |
| 128 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf4_Ethernet2 | PASS | - |
| 129 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet5 | PASS | - |
| 130 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet5 | PASS | - |
| 131 | leaf3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet5 | PASS | - |
| 132 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: leaf3_Ethernet1 | PASS | - |
| 133 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: leaf3_Ethernet2 | PASS | - |
| 134 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: spine1_Ethernet6 | PASS | - |
| 135 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: spine2_Ethernet6 | PASS | - |
| 136 | leaf4 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: spine3_Ethernet6 | PASS | - |
| 137 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: leaf1_Ethernet3 | PASS | - |
| 138 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: leaf2_Ethernet3 | PASS | - |
| 139 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: leaf3_Ethernet3 | PASS | - |
| 140 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet6 - remote: leaf4_Ethernet3 | PASS | - |
| 141 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet7 - remote: borderleaf1_Ethernet3 | FAIL | Interface Down - N/A |
| 142 | spine1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet8 - remote: borderleaf2_Ethernet3 | FAIL | Interface Down - N/A |
| 143 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: leaf1_Ethernet4 | PASS | - |
| 144 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: leaf2_Ethernet4 | PASS | - |
| 145 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: leaf3_Ethernet4 | PASS | - |
| 146 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet6 - remote: leaf4_Ethernet4 | PASS | - |
| 147 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet7 - remote: borderleaf1_Ethernet4 | FAIL | Interface Down - N/A |
| 148 | spine2 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet8 - remote: borderleaf2_Ethernet4 | FAIL | Interface Down - N/A |
| 149 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: leaf1_Ethernet5 | PASS | - |
| 150 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: leaf2_Ethernet5 | PASS | - |
| 151 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: leaf3_Ethernet5 | PASS | - |
| 152 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet6 - remote: leaf4_Ethernet5 | PASS | - |
| 153 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet7 - remote: borderleaf1_Ethernet5 | PASS | - |
| 154 | spine3 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet8 - remote: borderleaf2_Ethernet5 | PASS | - |
| 155 | leaf1 | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 156 | leaf2 | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 157 | leaf3 | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 158 | leaf4 | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 159 | borderleaf1 | IP Reachability | ip reachability test p2p links | Source: borderleaf1_Ethernet3 - Destination: spine1_Ethernet7 | FAIL | 100% packet loss |
| 160 | borderleaf1 | IP Reachability | ip reachability test p2p links | Source: borderleaf1_Ethernet4 - Destination: spine2_Ethernet7 | FAIL | 100% packet loss |
| 161 | borderleaf1 | IP Reachability | ip reachability test p2p links | Source: borderleaf1_Ethernet5 - Destination: spine3_Ethernet7 | PASS | - |
| 162 | borderleaf2 | IP Reachability | ip reachability test p2p links | Source: borderleaf2_Ethernet3 - Destination: spine1_Ethernet8 | FAIL | 100% packet loss |
| 163 | borderleaf2 | IP Reachability | ip reachability test p2p links | Source: borderleaf2_Ethernet4 - Destination: spine2_Ethernet8 | FAIL | 100% packet loss |
| 164 | borderleaf2 | IP Reachability | ip reachability test p2p links | Source: borderleaf2_Ethernet5 - Destination: spine3_Ethernet8 | PASS | - |
| 165 | leaf1 | IP Reachability | ip reachability test p2p links | Source: leaf1_Ethernet3 - Destination: spine1_Ethernet3 | PASS | - |
| 166 | leaf1 | IP Reachability | ip reachability test p2p links | Source: leaf1_Ethernet4 - Destination: spine2_Ethernet3 | PASS | - |
| 167 | leaf1 | IP Reachability | ip reachability test p2p links | Source: leaf1_Ethernet5 - Destination: spine3_Ethernet3 | PASS | - |
| 168 | leaf2 | IP Reachability | ip reachability test p2p links | Source: leaf2_Ethernet3 - Destination: spine1_Ethernet4 | PASS | - |
| 169 | leaf2 | IP Reachability | ip reachability test p2p links | Source: leaf2_Ethernet4 - Destination: spine2_Ethernet4 | PASS | - |
| 170 | leaf2 | IP Reachability | ip reachability test p2p links | Source: leaf2_Ethernet5 - Destination: spine3_Ethernet4 | PASS | - |
| 171 | leaf3 | IP Reachability | ip reachability test p2p links | Source: leaf3_Ethernet3 - Destination: spine1_Ethernet5 | PASS | - |
| 172 | leaf3 | IP Reachability | ip reachability test p2p links | Source: leaf3_Ethernet4 - Destination: spine2_Ethernet5 | PASS | - |
| 173 | leaf3 | IP Reachability | ip reachability test p2p links | Source: leaf3_Ethernet5 - Destination: spine3_Ethernet5 | PASS | - |
| 174 | leaf4 | IP Reachability | ip reachability test p2p links | Source: leaf4_Ethernet3 - Destination: spine1_Ethernet6 | PASS | - |
| 175 | leaf4 | IP Reachability | ip reachability test p2p links | Source: leaf4_Ethernet4 - Destination: spine2_Ethernet6 | PASS | - |
| 176 | leaf4 | IP Reachability | ip reachability test p2p links | Source: leaf4_Ethernet5 - Destination: spine3_Ethernet6 | PASS | - |
| 177 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet3 - Destination: leaf1_Ethernet3 | PASS | - |
| 178 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet4 - Destination: leaf2_Ethernet3 | PASS | - |
| 179 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet5 - Destination: leaf3_Ethernet3 | PASS | - |
| 180 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet6 - Destination: leaf4_Ethernet3 | PASS | - |
| 181 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet7 - Destination: borderleaf1_Ethernet3 | FAIL | 100% packet loss |
| 182 | spine1 | IP Reachability | ip reachability test p2p links | Source: spine1_Ethernet8 - Destination: borderleaf2_Ethernet3 | FAIL | 100% packet loss |
| 183 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet3 - Destination: leaf1_Ethernet4 | PASS | - |
| 184 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet4 - Destination: leaf2_Ethernet4 | PASS | - |
| 185 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet5 - Destination: leaf3_Ethernet4 | PASS | - |
| 186 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet6 - Destination: leaf4_Ethernet4 | PASS | - |
| 187 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet7 - Destination: borderleaf1_Ethernet4 | FAIL | 100% packet loss |
| 188 | spine2 | IP Reachability | ip reachability test p2p links | Source: spine2_Ethernet8 - Destination: borderleaf2_Ethernet4 | FAIL | 100% packet loss |
| 189 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet3 - Destination: leaf1_Ethernet5 | PASS | - |
| 190 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet4 - Destination: leaf2_Ethernet5 | PASS | - |
| 191 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet5 - Destination: leaf3_Ethernet5 | PASS | - |
| 192 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet6 - Destination: leaf4_Ethernet5 | PASS | - |
| 193 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet7 - Destination: borderleaf1_Ethernet5 | PASS | - |
| 194 | spine3 | IP Reachability | ip reachability test p2p links | Source: spine3_Ethernet8 - Destination: borderleaf2_Ethernet5 | PASS | - |
| 195 | borderleaf1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 196 | borderleaf2 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 197 | leaf1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 198 | leaf2 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 199 | leaf3 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 200 | leaf4 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 201 | spine1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 202 | spine2 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 203 | spine3 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 204 | borderleaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.24 | FAIL | Session state Idle |
| 205 | borderleaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.26 | FAIL | Session state Idle |
| 206 | borderleaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.28 | PASS | - |
| 207 | borderleaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.30 | FAIL | Session state Idle |
| 208 | borderleaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.32 | FAIL | Session state Idle |
| 209 | borderleaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.34 | PASS | - |
| 210 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.1 | PASS | - |
| 211 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.0 | PASS | - |
| 212 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.2 | PASS | - |
| 213 | leaf1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.4 | PASS | - |
| 214 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.0 | PASS | - |
| 215 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.6 | PASS | - |
| 216 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.8 | PASS | - |
| 217 | leaf2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.10 | PASS | - |
| 218 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.5 | PASS | - |
| 219 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.12 | PASS | - |
| 220 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.14 | PASS | - |
| 221 | leaf3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.16 | PASS | - |
| 222 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.4 | PASS | - |
| 223 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.18 | PASS | - |
| 224 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.20 | PASS | - |
| 225 | leaf4 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.22 | PASS | - |
| 226 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.1 | PASS | - |
| 227 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.7 | PASS | - |
| 228 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.13 | PASS | - |
| 229 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.19 | PASS | - |
| 230 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.25 | FAIL | Session state Idle |
| 231 | spine1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.31 | FAIL | Session state Idle |
| 232 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.3 | PASS | - |
| 233 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.9 | PASS | - |
| 234 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.15 | PASS | - |
| 235 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.21 | PASS | - |
| 236 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.27 | FAIL | Session state Idle |
| 237 | spine2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.33 | FAIL | Session state Idle |
| 238 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.5 | PASS | - |
| 239 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.11 | PASS | - |
| 240 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.17 | PASS | - |
| 241 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.23 | PASS | - |
| 242 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.29 | PASS | - |
| 243 | spine3 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 192.168.103.35 | PASS | - |
| 244 | borderleaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | FAIL | Session state: Active |
| 245 | borderleaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | FAIL | Session state: Active |
| 246 | borderleaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 247 | borderleaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | FAIL | Session state: Active |
| 248 | borderleaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | FAIL | Session state: Active |
| 249 | borderleaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 250 | leaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | PASS | - |
| 251 | leaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | PASS | - |
| 252 | leaf1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 253 | leaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | PASS | - |
| 254 | leaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | PASS | - |
| 255 | leaf2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 256 | leaf3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | PASS | - |
| 257 | leaf3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | PASS | - |
| 258 | leaf3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 259 | leaf4 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.11 | PASS | - |
| 260 | leaf4 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.12 | PASS | - |
| 261 | leaf4 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.13 | PASS | - |
| 262 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.5 | FAIL | Session state: Active |
| 263 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.6 | FAIL | Session state: Active |
| 264 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.1 | PASS | - |
| 265 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.2 | PASS | - |
| 266 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.3 | PASS | - |
| 267 | spine1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.4 | PASS | - |
| 268 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.5 | FAIL | Session state: Active |
| 269 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.6 | FAIL | Session state: Active |
| 270 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.1 | PASS | - |
| 271 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.2 | PASS | - |
| 272 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.3 | PASS | - |
| 273 | spine2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.4 | PASS | - |
| 274 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.5 | PASS | - |
| 275 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.6 | PASS | - |
| 276 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.1 | PASS | - |
| 277 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.2 | PASS | - |
| 278 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.3 | PASS | - |
| 279 | spine3 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.101.4 | PASS | - |
| 280 | borderleaf1 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 281 | borderleaf1 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 282 | borderleaf1 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 283 | borderleaf1 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 284 | borderleaf2 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 285 | borderleaf2 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 286 | borderleaf2 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 287 | borderleaf2 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 288 | leaf1 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 289 | leaf1 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 290 | leaf1 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 291 | leaf1 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 292 | leaf2 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 293 | leaf2 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 294 | leaf2 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 295 | leaf2 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 296 | leaf3 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 297 | leaf3 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 298 | leaf3 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 299 | leaf3 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 300 | leaf4 | Routing Table | Remote VTEP address | 192.168.102.5 | PASS | - |
| 301 | leaf4 | Routing Table | Remote VTEP address | 192.168.102.6 | PASS | - |
| 302 | leaf4 | Routing Table | Remote VTEP address | 192.168.102.1 | PASS | - |
| 303 | leaf4 | Routing Table | Remote VTEP address | 192.168.102.3 | PASS | - |
| 304 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 305 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 306 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 307 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 308 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 309 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 310 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.11 | FAIL | Lo0 192.168.101.11 is not in the routing table |
| 311 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.12 | FAIL | Lo0 192.168.101.12 is not in the routing table |
| 312 | borderleaf1 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 313 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 314 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 315 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 316 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 317 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 318 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 319 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.11 | FAIL | Lo0 192.168.101.11 is not in the routing table |
| 320 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.12 | FAIL | Lo0 192.168.101.12 is not in the routing table |
| 321 | borderleaf2 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 322 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 323 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 324 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 325 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 326 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 327 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 328 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.11 | PASS | - |
| 329 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.12 | PASS | - |
| 330 | leaf1 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 331 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 332 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 333 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 334 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 335 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 336 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 337 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.11 | PASS | - |
| 338 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.12 | PASS | - |
| 339 | leaf2 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 340 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 341 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 342 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 343 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 344 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 345 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 346 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.11 | PASS | - |
| 347 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.12 | PASS | - |
| 348 | leaf3 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 349 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.5 | PASS | - |
| 350 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.6 | PASS | - |
| 351 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.1 | PASS | - |
| 352 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.2 | PASS | - |
| 353 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.3 | PASS | - |
| 354 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.4 | PASS | - |
| 355 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.11 | PASS | - |
| 356 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.12 | PASS | - |
| 357 | leaf4 | Routing Table | Remote Lo0 address | 192.168.101.13 | PASS | - |
| 358 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.5 | PASS | - |
| 359 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.6 | PASS | - |
| 360 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.1 | PASS | - |
| 361 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.2 | PASS | - |
| 362 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.3 | PASS | - |
| 363 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.4 | PASS | - |
| 364 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.11 | FAIL | 100% packet loss |
| 365 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.12 | FAIL | 100% packet loss |
| 366 | borderleaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf1 - 192.168.101.5 Destination: 192.168.101.13 | PASS | - |
| 367 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.5 | PASS | - |
| 368 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.6 | PASS | - |
| 369 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.1 | PASS | - |
| 370 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.2 | PASS | - |
| 371 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.3 | PASS | - |
| 372 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.4 | PASS | - |
| 373 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.11 | FAIL | 100% packet loss |
| 374 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.12 | FAIL | 100% packet loss |
| 375 | borderleaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: borderleaf2 - 192.168.101.6 Destination: 192.168.101.13 | PASS | - |
| 376 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.5 | PASS | - |
| 377 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.6 | PASS | - |
| 378 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.1 | PASS | - |
| 379 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.2 | PASS | - |
| 380 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.3 | PASS | - |
| 381 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.4 | PASS | - |
| 382 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.11 | PASS | - |
| 383 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.12 | PASS | - |
| 384 | leaf1 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf1 - 192.168.101.1 Destination: 192.168.101.13 | PASS | - |
| 385 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.5 | PASS | - |
| 386 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.6 | PASS | - |
| 387 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.1 | PASS | - |
| 388 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.2 | PASS | - |
| 389 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.3 | PASS | - |
| 390 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.4 | PASS | - |
| 391 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.11 | PASS | - |
| 392 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.12 | PASS | - |
| 393 | leaf2 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf2 - 192.168.101.2 Destination: 192.168.101.13 | PASS | - |
| 394 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.5 | PASS | - |
| 395 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.6 | PASS | - |
| 396 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.1 | PASS | - |
| 397 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.2 | PASS | - |
| 398 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.3 | PASS | - |
| 399 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.4 | PASS | - |
| 400 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.11 | PASS | - |
| 401 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.12 | PASS | - |
| 402 | leaf3 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf3 - 192.168.101.3 Destination: 192.168.101.13 | PASS | - |
| 403 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.5 | PASS | - |
| 404 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.6 | PASS | - |
| 405 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.1 | PASS | - |
| 406 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.2 | PASS | - |
| 407 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.3 | PASS | - |
| 408 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.4 | PASS | - |
| 409 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.11 | PASS | - |
| 410 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.12 | PASS | - |
| 411 | leaf4 | Loopback0 Reachability | Loopback0 Reachability | Source: leaf4 - 192.168.101.4 Destination: 192.168.101.13 | PASS | - |
