📡 Call Center Network Switch Configuration – Cisco CBS350

**This project involves configuring a secure and efficient Layer 2 switching network for a call center environment using 13 Cisco CBS350 switches. It includes VLAN segmentation, trunking, SSH access, Spanning Tree optimization, port security, and more — all tailored for a high-availability voice/data infrastructure.**



🧱 Network Topology Overview
Core Switch: 1 Cisco CBS350 (named Core-SW)

Access Switches: 12 Cisco CBS350 switches (named Floor-1, Floor-2, HR, QU, IT, etc.)

Router: Cisco ISR connected to leased line for internet access

Management VLAN: VLAN 1

Production VLANs:

VLAN 10: Floor users

VLAN 20: Departments (HR, IT, QU)

Trunk Ports:

All uplinks (ports 1–5, 6–15, 20–21 on the core switch) are configured as trunk

Port Allocation (on Core Switch):

Ports 1–5: Servers

Ports 6–15: Trunks to access switches

Ports 20–21: Firewall

🔐 Security Features Implemented

| Feature                      | Description                                                                         |
| ---------------------------- | ----------------------------------------------------------------------------------- |
| **SSH Access**               | Enabled and secured with user authentication                                        |
| **Port Security**            | Sticky MAC address binding, limits per port, and violation handling                 |
| **BPDU Guard**               | Enabled on access ports to prevent rogue switch loops                               |
| **DHCP Snooping**            | Blocks rogue DHCP servers, allows trusted uplinks only                              |
| **Shutdown Unused Ports**    | All unused ports (Gi1/20–Gi1/24) are administratively shut down                     |
| **Spanning Tree RSTP**       | Rapid Spanning Tree Protocol with Core-SW as root bridge                            |
| **Trunk Ports**              | Port Gi1/1 on all switches is configured as trunk for inter-switch VLAN propagation |
| ** SNMP **                   | Supports centralized logging and monitoring integration                             |
| **QoS Ready **               | Prepared for voice QoS if IP phones are deployed                                    |


🔧 On the Cisco Router (WAN Gateway)

| Feature                            | Description                                                       |
| ---------------------------------- | ----------------------------------------------------------------- |
| **Static IP Configuration**        | Public IP assigned on WAN interface from ISP                      |
| **Default Route**                  | Configured toward ISP next hop                                    |
| **SSH Management**                 | Enabled with RSA encryption and local user login                  |
| **Access Control Lists (ACLs)**    | Prevent unwanted public access (e.g., Telnet, HTTP blocked)       |



📈 Benefits of This Design
✅ Segregated traffic for different departments and users

✅ Faster failover with Rapid STP and trunk optimization

✅ Strong port-level security against unauthorized device access

✅ Scalable and maintainable structure for future expansion

✅ Production-ready for VoIP, surveillance, or large-volume data handling
