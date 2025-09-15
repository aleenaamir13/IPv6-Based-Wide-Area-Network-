# IPv6-Based-Wide-Area-Network-
This project implements IPv6 addressing with OSPF routing in a network of core/edge routers, switches, and end devices. It evaluates OSPF’s efficiency, scalability, and simplicity in IPv6, analyzing routing performance, address configuration, and topology design, with detailed explanations of concepts and hardware setup.
# IPv6-Based Wide Area Network with OSPF Routing

## Abstract  
This project explores the implementation of **IPv6 addressing** and **Open Shortest Path First (OSPFv3)** routing in a hierarchical network topology. The topology consists of **core and edge routers**, switches, and end devices. The goal is to evaluate the **efficiency, scalability, and simplicity** of OSPF in an IPv6 environment while analyzing **routing performance, address configuration, and topology structure**. Both **software simulation (Cisco Packet Tracer)** and **hardware implementation** were tested.

---

## Introduction  
Due to the **depletion of IPv4 addresses**, IPv6 has become essential for modern networking. IPv6 provides:  
- Vast address space  
- Improved scalability  
- Enhanced security features  
- Support for IoT and mobile ecosystems  

This project designs and implements an IPv6 WAN with **OSPFv3 routing**, using a **three-layer hierarchical topology (Core, Distribution, Access)** to ensure **structured design, scalability, and efficient management**.

---

## Tools & Resources  
### Software  
- Cisco Packet Tracer  

### Hardware  
- 2 IPv6 Routers  
- 2 Switches  
- 3 End Devices  

---

## Topology Design  
The topology follows a **three-layer hierarchical model**:  

1. **Core Layer**  
   - Routers (Router6 & Router8) interconnect network branches.  
   - Provides high-speed backbone communication.  
   - (Skipped in hardware due to limited devices).  

2. **Distribution Layer**  
   - Edge routers (Router7 & Router9).  
   - Aggregate subnets and apply policies (e.g., QoS, filtering).  

3. **Access Layer**  
   - Switches and end devices (PCs, Laptops).  
   - Provides user connectivity.  

This separation simplifies **management, scalability, troubleshooting, and fault tolerance**.

---

## IPv6 Addressing  
The project uses **Global Unicast Addressing (GUA)** for:  
- Global connectivity  
- Unique addressing (no conflicts)  
- End-to-end communication (no NAT required)  
- Scalability for future expansion  
- Efficient routing with OSPFv3 compatibility  
- Real-world implementation and secure communication with IPsec  

---

## Address Assignment  

### Software (Simulation)  
| Device | Interface | IPv6 Address |
|--------|-----------|--------------|
| Router6 | Gig0/0 | 2001:DAA:AAAA:A::1/64 |
| Router8 | Gig0/0 | 2001:DBB:BBBB:B::2/64 |
| Router7 | Gig0/0 | 2001:DAA:AAAA:A::1/64 |
| Router9 | Gig0/0 | 2001:DCC:CCCC:C::2/64 |

(Additional device and PC addresses included in report).  

### Hardware (Physical Implementation)  
| Device | Interface | IPv6 Address |
|--------|-----------|--------------|
| Router0 | Gig0/0 | 2001:DBB:BBBB:B::1/64 |
| Router1 | Gig0/0 | 2001:DBB:BBBB:B::2/64 |
| PC0 | NIC | 2001:DAA:AAAA:A::2/64 |
| PC1 | NIC | 2001:DCC:CCCC:C::3/64 |

---

## OSPFv3 Routing  
### Why OSPFv3?  
- Dynamic route updates  
- High scalability  
- Fast convergence  
- Native IPv6 support  

### Configuration Steps  
1. Assign IPv6 addresses to routers and end devices.  
2. Enable OSPFv3 on router interfaces.  
3. Verify using `show ipv6 route`.  
4. Test connectivity with `ping` between end devices.  

---

## Results & Observations  
- **Routing Performance**: OSPFv3 quickly converged with minimal downtime.  
- **Addressing**: IPv6 avoided conflicts and simplified configuration.  
- **Traffic Flow**: Hierarchical design optimized traffic handling.  
- **Scalability**: Additional devices integrated seamlessly.  
- **Hardware Limitation**: Full core layer could not be implemented physically due to lack of routers/cables.  

---

## Conclusion  
This project demonstrates that **IPv6 with OSPFv3** in a hierarchical topology ensures:  
- **Scalability**  
- **Reliability**  
- **Efficient routing**  
- **Enterprise-grade design**  

Despite hardware constraints, the **Cisco Packet Tracer simulation** fully validated the network design and routing functionality.

---

## Project Demo Video  
[Watch Here](https://drive.google.com/file/d/1hwTY4MHgHkA62UJiEDgyXkR-t4lGx9Sk/view?usp=drivesdk)

---

## Authors  
- Student Project on IPv6 WAN with OSPFv3  
