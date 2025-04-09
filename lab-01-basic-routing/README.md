# Lab 01 – Basic Small Office Network with Static Routing

## 🧠 Objective:
Simulate a small office setup with two routers and four PCs. Demonstrate static routing across two separate networks using Cisco Packet Tracer.

## 🛠️ Topology:
- 2 Routers (2911)
- 2 Switches
- 4 PCs (2 on each router)
- Router-to-Router connection

![Topology Screenshot](topology.png)

## 📋 IP Addressing Scheme:

| Device  | Interface    | IP Address     | Subnet Mask       |
|---------|--------------|----------------|-------------------|
| PC1     | FastEthernet0| 192.168.1.10   | 255.255.255.0     |
| PC2     | FastEthernet0| 192.168.1.11   | 255.255.255.0     |
| PC3     | FastEthernet0| 192.168.2.10   | 255.255.255.0     |
| PC4     | FastEthernet0| 192.168.2.11   | 255.255.255.0     |
| Router1 | Gig0/0       | 192.168.1.1    | 255.255.255.0     |
| Router1 | Gig0/1       | 10.0.0.1       | 255.255.255.0     |
| Router2 | Gig0/0       | 192.168.2.1    | 255.255.255.0     |
| Router2 | Gig0/1       | 10.0.0.2       | 255.255.255.0     |

## 🧪 What I Did:
- Connected all PCs and routers using switches
- Assigned IP addresses to all interfaces
- Configured `no shutdown` on router interfaces
- Verified that all connections turned green
- Configured static routing on both **Router1** and **Router2** to enable communication between the two networks:
    - **Router1**: Added a static route to reach **192.168.2.0/24** via **10.0.0.2**.
    - **Router2**: Added a static route to reach **192.168.1.0/24** via **10.0.0.1**.
- Verified static routing by pinging from **Router1** to **PC3** (192.168.2.10) and vice versa.

### Troubleshooting:
- Initially encountered a 50% packet loss when pinging across routers.
    - Double-checked the interface statuses with `show ip interface brief` to ensure interfaces were up.
    - Verified static routes on both routers using `show ip route`.
    - After resolving the issue, I was able to achieve 0% packet loss and full connectivity.

## ✅ Next Step:
Configure additional network services or test more advanced routing protocols.

**Status:** ✅ Network physically connected and functional, static routing successfully configured and tested.

