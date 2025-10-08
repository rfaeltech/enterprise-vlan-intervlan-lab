# ✅ Verification Checklist – Enterprise VLAN Lab

This document provides evidence of successful VLAN configuration, trunking, inter-VLAN routing, and connectivity in an enterprise network setup.

---

## 📑 Table of Contents
1. [Switch Verification](#switch-verification)
2. [Router Verification](#router-verification)
3. [Connectivity Tests](#connectivity-tests)

---

## 🧩 Switch Verification
- [ ] `show vlan brief` → VLAN10, VLAN20, VLAN30 exist  
  **Expected Output:** VLANs listed with correct names and ports assigned  
  <img src="screenshots/vlan_table_verification.png" alt="VLAN table verification" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] `show interfaces trunk` → trunk ports up, allowed VLANs 10, 20, 30  
  **Expected Output:** Trunk interfaces active and passing VLANs  
  <img src="screenshots/trunk_port_status.png" alt="Trunk port status" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

---

## 🖥️ Router Verification
- [ ] `show ip interface brief` → subinterfaces G0/0.10, G0/0.20, G0/0.30 up  
  **Expected Output:** Subinterfaces with correct IP addresses and status up  
  <img src="screenshots/router_subinterfaces.png" alt="Router subinterfaces" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] `show ip route` → networks 192.168.10.0/24, 192.168.20.0/24, 192.168.30.0/24 appear  
  **Expected Output:** Routes for all VLAN networks listed  
  <img src="screenshots/router_ip_route.png" alt="Router IP routing table" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

---

## 🌐 Connectivity Tests
- [ ] Ping between PCs in the **same VLAN**  
  <img src="screenshots/ping_same_vlan.png" alt="Ping within same VLAN" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] Ping between PCs in **different VLANs**  
  <img src="screenshots/ping_different_vlan.png" alt="Ping between different VLANs" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] Ping **Server1 from Router R1** (VLAN 10)  
<img src="screenshots/vlan _10_ping_server.png" alt="Vlan10 to server" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">

- [ ] Ping **Server1 from another VLAN** (VLAN 30)  
  <img src="screenshots/vlan_30_ping_server.png" alt="Ping from VLAN 30 to server" style="border:1px solid #ddd; padding:5px; max-width:100%; height:auto;">
