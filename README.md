Network Topology Documentation

Overview

This repository contains the network topology diagram for building network project . The network consists of multiple Cisco switches, two router, and multiple VLANs to simulate a corporate environment.

Network Components

Core Switch:

Device: CBS350-8G

IP Address: 192.*.*.*

Function: Acts as the central switch connecting multiple switches and network segments.

Access Switches:

The network includes multiple access switches, primarily Cisco CBS350-24T-4G models, which segment different floors and departments:

FLR1-1R: 192.*.*.*

FLR1-2C: 192.*.*.*

FLR2-R: 192.*.*.*

FLR2-LL: 192.*.*.*

FLR3-1R: 192.*.*.*

FLR3-3D: 192.*.*.*

FLR3-4L: 192.*.*.*

FLR3-2U: 192.*.*.*

ITSWITCH: 192.*.*.* (Dedicated switch for IT department)

HR: 192.*.*.* (HR Department switch)

QU: 192.*.*.* (Quality control switch)

Router:

Device: Cisco Router

IP Address: *.*.*.* (Configured as gateway for external connections)

Function: Handles routing between VLANs and internet connectivity.

Phones:

Several VoIP phones (GXP1615, GXP2135) are connected to the network:

GXP1615: 192.*.*.*, 192.*.*.*, 192.*.*.*, 192.*.*.*, 192.*.*.*, 192.*.*.*

GXP2135: 192.*.*.*

Additional Components:

FL2-CLOSER: CBS220-48T-4G (192.*.*.*)

Cloud Connection: ip4solution (*.*.*.*)

Additional Host: CC2D-E0-39-D2-96 (192.*.*.*)

VLANs

The network is segmented using VLANs for better traffic isolation and security.

VLAN 10: IT Department

VLAN 20: HR Department

VLAN 30: Floor 1 Devices

VLAN 40: Floor 2 Devices

VLAN 50: Floor 3 Devices

VLAN 99: Management VLAN
