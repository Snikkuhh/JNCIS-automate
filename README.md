🧠 JNCIS-ENT Lab – Progress & Challenges

Auteur: Romano Blanker
Start: Juni 2025
Status: Actief ✅

🎯 Doelstelling

Verdieping in Juniper Enterprise Routing & Switching

Hands-on labben in EVE-NG

Minimaal 1 uur per dag zelfstudie

Examengericht toewerken naar JNCIS-ENT certificatie

Discipline: no excuses, no verslapping

✅ Challenge 1 – vSRX connectivity check (base test)

Doel: basisconnectiviteit tussen 2 vSRX firewalls controleren

Topo:

SRX-1 ge-0/0/2: 172.16.0.1/30

SRX-2 ge-0/0/2: 172.16.0.2/30

Verificatie:

Ping faalt initieel door security policies / forwarding mode

Oplossing: security config verwijderd + packet-based forwarding mode geactiveerd

Resultaat: Ping werkt ✅

✅ Challenge 2 – Switch IRB + VLAN connectivity

Doel: IRB-interface configureren op vQFX en connectiviteit testen

Topo:

vQFX1: irb.10 = 10.10.10.1/24, geassocieerd met VLAN 10

vQFX2: irb.20 = 10.10.20.1/24, VLAN 20

Verificatie:

IRB interfaces geconfigureerd ✅

VLAN-toewijzing via switchport_config-qfx1.yml en qfx2.yml

Devices in subnet kunnen gateway pingen

✅ Challenge 3 – Ansible Push + Dynamic Expand

Doel: Topologie uitbreiden met vMX’s, push via Ansible

Acties:

vMX-1 & vMX-2 toegevoegd aan bestaande topology

Full push via Ansible uitgevoerd op QFX’en

Nieuwe config getest via verify.yml

Resultaat: Works as expected ✅

✅ Challenge 4 – Static Routes + ECMP

Doel: Multipath routing testen met meerdere static routes

Config:

vMX1 → static naar 192.168.200.0/24 via 2 nexthops

ECMP toegestaan

Verificatie:

show route toont beide next-hops in RIB

show route forwarding-table toont slechts 1 → verklaard door vMX PFE-limitatie

Log: ECMP verified (RIB-only in vMX) ✅

✅ Challenge 5 – IBGP tussen loopbacks + route advertentie

Doel: IBGP opzetten tussen vMX1 en vMX2 en prefixes filteren

Acties:

IBGP opgezet via lo0 (1.1.1.1 ⇄ 2.2.2.2)

Static route ge-exporteerd via policy

verify_bgp.yml bevestigd: sessie Established, prefix zichtbaar met 2 nexthops

Resultaat: Challenge geslaagd ✅


