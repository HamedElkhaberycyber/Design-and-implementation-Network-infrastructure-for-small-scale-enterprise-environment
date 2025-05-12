📡 Call Center Network Switch Configuration – Cisco CBS350

**This project involves configuring a secure and efficient Layer 2 switching network for a call center environment using 13 Cisco CBS350 switches. It includes VLAN segmentation, trunking, SSH access, Spanning Tree optimization, port security, and more — all tailored for a high-availability voice/data infrastructure.**

🏗️ Network Design Summary

Total Switches: 13 Cisco CBS350 switches
Topology: Star design with a Core Switch and 12 Access Switches
Naming Convention: Core-SW, Floor-1, Floor-2, Floor-3, QU, HR, IT, etc.
Management VLAN: VLAN 20
Voice VLAN : VLAN 10 agent on call users

🔐 Security Features Implemented

| Feature                      | Description                                                                         |
| ---------------------------- | ----------------------------------------------------------------------------------- |
| **SSH Access**               | Enabled and secured with user authentication                                        |
| **Port Security**            | Sticky MAC address binding, limits per port, and violation handling                 |
| **BPDU Guard**               | Enabled on access ports to prevent rogue switch loops                               |
| **DHCP Snooping**            | Blocks rogue DHCP servers, allows trusted uplinks only                              |
| **Shutdown Unused Ports**    | All unused ports (Gi1/20–Gi1/24) are administratively shut down                     |
| **Restricted SSH Access**    | SSH management access limited to specific IP addresses using ACLs                   |
| **Spanning Tree RSTP**       | Rapid Spanning Tree Protocol with Core-SW as root bridge                            |
| **Trunk Ports**              | Port Gi1/1 on all switches is configured as trunk for inter-switch VLAN propagation |
| ** SNMP **                   | Supports centralized logging and monitoring integration                             |
| **QoS Ready **               | Prepared for voice QoS if IP phones are deployed                                    |




📈 Benefits of This Design
✅ Segregated traffic for different departments and users

✅ Faster failover with Rapid STP and trunk optimization

✅ Strong port-level security against unauthorized device access

✅ Scalable and maintainable structure for future expansion

✅ Production-ready for VoIP, surveillance, or large-volume data handling
