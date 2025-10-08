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
- Screenshots: `screenshots/vlan_table_verification.png`

- [ ] `show interfaces trunk` → trunk ports up, allowed VLANs 10, 20, 30  
  **Expected Output:** Trunk interfaces active and passing VLANs  
- Screenshots: `screenshots/trunk_port_status.png`

---

## 🖥️ Router Verification

- [ ] `show ip interface brief` → subinterfaces G0/0.10, G0/0.20, G0/0.30 up  
  **Expected Output:** Subinterfaces with correct IP addresses and status up  
- Screenshots: `screenshots/router_subinterfaces.png`

- [ ] `show ip route` → networks 192.168.10.0/24, 192.168.20.0/24, 192.168.30.0/24 appear  
  **Expected Output:** Routes for all VLAN networks listed  
- Screenshots: `screenshots/router_ip_route.png`

---

## 🌐 Connectivity Tests

- [ ] Ping between PCs in the **same VLAN**  
- Screenshots: `screenshots/ping_same_vlan.png`

- [ ] Ping between PCs in **different VLANs**  
- Screenshots: `screenshots/ping_different_vlan.png`

- [ ] Ping **Server1 from Router R1** (VLAN 10)  
- Screenshots: `screenshots/vlan _10_ping_server.png`

- [ ] Ping **Server1 from another VLAN** (VLAN 30)  
- Screenshots: `screenshots/vlan_30_ping_server.png`