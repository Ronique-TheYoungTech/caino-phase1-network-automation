# Lab 1 – Configure, Verify, and Troubleshoot IPv4 Addresses

This lab introduces foundational IPv4 interface configuration and verification on Cisco routers using Packet Tracer.  
All interface mappings use the Cisco 2901 platform with HWIC-2T modules, which results in the serial interfaces appearing as Serial0/3/0 and Serial0/3/1.

---

## 📡 Topology

![Lab 1 Topology](screenshots/lab1-topology.png)

*Devices Used*
- 2 × Cisco 2901 routers  
- Serial link between:
  - R1 → Serial0/3/0  
  - R3 → Serial0/3/1  

---

## 🎯 Objectives

- Configure hostnames  
- Configure IPv4 addresses on serial interfaces  
- Configure loopback interfaces  
- Verify interface states and IPv4 addressing  
- Troubleshoot Layer-1/Layer-2 connectivity  

---

## 🛠 Step 1 — Configure Hostnames

### *R1*
```bash
conf t
hostname R1
end

R3
conf t
hostname R3
end

🛠 Step 2 — Configure Serial Interfaces

R1 – Serial0/3/0




