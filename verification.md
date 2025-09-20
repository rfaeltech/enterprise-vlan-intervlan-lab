# Verification Checklist – Enterprise VLAN Lab

## Switch Verification
- [ ] `show vlan brief` → VLAN10, VLAN20, VLAN30 exist
<img src="screenshots\vlan_table_verification.png" alt="show vlan" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] `show interfaces trunk` → trunk up, allowed VLANs 10,20,30
<img src="screenshots\trunk_port_status.png" alt="Trunk ports" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">


## Router Verification
- [ ] `show ip interface brief` → subinterfaces G0/0.10, .20, .30 up
<img src="screenshots\router_subinterfaces.png" alt="Sub interface" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] `show ip route` → networks 192.168.10.0/24, 192.168.20.0/24, 192.168.30.0/24 appear
<img src="screenshots\router_ip_route.png" alt="IP route" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

## Connectivity Tests
- [ ] Ping between PCs in same VLAN
<img src="screenshots\ping_same_vlan.png" alt="Ping within same vlan" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] Ping between PCs in different VLANs
<img src="screenshots\ping_different_vlan.png" alt="ping between vlans" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] Ping server from router R1 to Server1 (Vlan 10)
<img src="screenshots\vlan _10_ping_server.png" alt="Vlan10 to server" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] <img src="screenshots\vlan_30_ping_server.png" alt="Other vlan to server" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">


