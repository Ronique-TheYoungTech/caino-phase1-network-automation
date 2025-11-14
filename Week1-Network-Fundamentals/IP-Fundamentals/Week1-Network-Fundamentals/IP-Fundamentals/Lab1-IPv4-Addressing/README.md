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
![R1 Hostname Configuration](screenshots/R1-hostname-config.jpg)
```bash
conf t
hostname R1
end
```
### *R3*
![R3 Hostname Configuration](screenshots/R3-hostname-config.png)
```bash
conf t
hostname R3
end
```

## 🛠 Step 2 — Configure Serial Interfaces
### *R1* – *Serial0/3/0*
![R1 Serial Configuration](screenshots/R1-serial-config.png)

```bash
conf t
interface se0/3/0
 ip address 172.16.1.1 255.255.255.192
 clock rate 800000! 
 no shutdown
end
```
### *R3* - *Serial0/3/1*
![R3 Serial Config](screenshots/R3-serial-config.png)

```bash
conf t
interface se0/3/1
 ip address 172.16.1.2 255.255.255.192
 no shutdown
end
```
## 🛠 Step 3 — Configure Loopback Interfaces (R3)
![R3 Loopback Configuration](screenshots/R3-loopback-config.png)
```bash
conf t
interface loopback10
 ip address 10.10.10.3 255.255.255.128

interface loopback20
 ip address 10.20.20.3 255.255.255.224

interface loopback30
 ip address 10.30.30.3 255.255.255.248
end
```







