Built a multi-site enterprise network from scratch in Cisco Packet Tracer — and troubleshot every broken hop myself.

The lab covers:
- VLAN segmentation (HR-VLAN10, Accounting-VLAN20) across two sites
- Router-on-a-Stick on a Cisco 2960 (Layer 2) side
- Layer 3 inter-VLAN routing on a Cisco 3560 multilayer switch
- Point-to-point WAN link between two 2901 routers (/30 subnet)
- Extended ACLs to block cross-VLAN traffic while allowing same-VLAN communication across sites

The hardest part wasn't configuring, it was troubleshooting. I diagnosed routing loops, duplicate SVIs, wrong next-hop addresses, and Packet Tracer routed-port quirks using show ip route, show ip interface brief, and hop-by-hop pings.

Full documentation and configs on GitHub. [link]

#Networking #Cisco #CCNA #CompTIA #NetworkPlus #HomeLab #ITCareer #PacketTracer
