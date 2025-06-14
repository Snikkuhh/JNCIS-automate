# JNCIS-ENT Automation Lab

## Voltooide Challenges

### ✅ Challenge 1 – Basic IP Reachability
Ping-connectiviteit tussen alle betrokken interfaces succesvol geverifieerd.

### ✅ Challenge 2 – OSPF Neighbors + Loopbacks
Loopback-adressen succesvol via OSPF geadverteerd. OSPF-neighbor-ship confirmed via Ansible.

### ✅ Challenge 3 – OSPF ECMP + Static Fallback
- ECMP naar 192.168.100.0/24 zichtbaar in RIB (2x static route)
- Verificatie toont fallback-gedrag
- Opmerking: ECMP zichtbaar in RIB, niet in FIB (vMX-limitation)

### ✅ Challenge 4 – BGP tussen loopbacks + static redistribution
- BGP sessie tussen lo0’s van vMX routers
- Redistribution van static -> BGP
- ECMP actief in RIB
- Verificatie via Ansible

### ✅ Challenge 5 – BGP Filtering + Communities
- Community tagging (64512:100)
- Community blocking via inbound policy
- BGP route filtering succesvol
- Policy-verificatie en show output bevestigd

### ✅ Challenge 6 – STP/BPDU Behavior + L2 verification
- STP actief op vQFX-switches
- BPDU rollen zichtbaar (DESG/ROOT)
- Global STP verification via Ansible en CLI

### ✅ Challenge 7 – Redistribution + OSPF/BGP route manipulation
- BGP inbound filtering, community matching
- Redistribution van static in OSPF
- Ansible verifies tonen juiste output

### ✅ Challenge 8 – Routing Policy + OSPF Type Filtering
- Export policy REDIST-STATIC maakt gebruik van metric-type
- Type-1/Type-2 verschil aangetoond via verificatie (handmatig + automation)

### ✅ Challenge 9 – OSPF Interface Types & Design Impact
- ge-0/0/3.0 (p2p) en ge-0/0/2.0 (broadcast) correct geconfigureerd
- OSPF neighbors & DR/BDR gedrag zichtbaar
- Verificatie toont interface types & roles correct via Ansible

### ✅ Challenge 10 – IS-IS Basics & DIS Election
- Level 2 IS-IS adjacency actief tussen vMX-1 en vMX-2 via ge-0/0/2.0
- lo0.0 correct als passive interface ingesteld
- SPF-log toont adjacency-formation en LSP exchange
- DIS zichtbaar in interface database

### Challenge 11 – IS-IS Adjacencies & Multi-Level Design
✅ Lo0 passive + ge-0/0/2.0 IS-IS Level 1 ↔ Level 2 structuur getest.
✅ 3 routers in Level 1 & Level 2 domeinen geverifieerd.
✅ LSP database entries correct verspreid per level.

## Challenge 12 – IS-IS Overload Bit + SPF Trigger Events
✅ Overload bit set and seen in LSP
✅ SPF triggers (e.g. adjacency) verified via logs

## ✅ Challenge 13 - Advanced IS-IS Metrics + Wide/Narrow Toggle
**Focus:** Wide/narrow metrics manipuleren + LSP gedrag controleren.

## ✅ Challenge 14 – IS-IS Route Suppression & Interface Cost
- Suppress forwarding routes.
- Modify interface cost and observe path selection.
---
