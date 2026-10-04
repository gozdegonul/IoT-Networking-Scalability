# 🌐 IoT Networking Protocols & Scalability Analysis

> A research report on how IoT networking protocols, network topologies and security mechanisms behave as deployments grow from a handful of devices to billions.

![Topic](https://img.shields.io/badge/Topic-Internet%20of%20Things-0A66C2)
![Focus](https://img.shields.io/badge/Focus-Protocols%20%7C%20Scalability%20%7C%20Security-success)
![Type](https://img.shields.io/badge/Type-Research%20Report-orange)
![Format](https://img.shields.io/badge/Format-PDF%20%2F%20DOCX-lightgrey)

---

## 📖 Overview

Classic TCP/IP was not designed for tiny, battery-powered, memory-constrained devices. IoT-specific protocols such as **6LoWPAN, MQTT and CoAP** were created to close that gap, yet **scalability** remains the deciding factor for whether an IoT system succeeds at scale.

This report examines:

- how IoT protocols are classified by **layer and range**,
- how the main application-layer protocols compare on **bandwidth, energy, latency and data model**,
- how **Star vs. Mesh topologies** behave as the node count grows,
- which **security risks** are *caused* by scalability, and
- which **architectural approaches** (edge/fog computing, SDN, lightweight cryptography) help IoT networks keep growing.

## 📄 Read the Report

| Format | Link |
|---|---|
| PDF | [Internet of Things (IoT) Networking Protocols & Scalability Analysis.pdf](./Internet%20of%20Things%20%28IoT%29%20Networking%20Protocols%20%26%20Scalability%20Analysis.pdf) |
| Word | [Internet of Things (IoT) Networking Protocols & Scalability Analysis.docx](./Internet%20of%20Things%20%28IoT%29%20Networking%20Protocols%20%26%20Scalability%20Analysis.docx) |

## 🧭 Contents

1. **Introduction & IoT Architecture** – M2M origins, the three-layer model (Perception, Network, Application), short-range (Wi-Fi, Bluetooth, Zigbee) vs. long-range (LoRaWAN, NB-IoT) communication
2. **Protocol Classification** – communication, network, transport, application and security layer protocols
3. **Protocol Comparison** – MQTT, CoAP, HTTP, AMQP and DDS evaluated side by side
4. **Scalability Metrics** – throughput, latency and packet loss ratio (PLR)
5. **Network Topologies** – Star vs. Mesh in large-scale deployments
6. **Security Challenges of Scale** – key management, congestion & DDoS, protocol overhead, single points of failure
7. **Solutions for Scalable IoT** – edge/fog computing, SDN, lightweight encryption, adaptive networks
8. **Conclusion**

## 🔍 Key Findings

### Which protocol for which need?

| Protocol | Bandwidth | Energy | Latency | Model | Best suited for |
|---|---|---|---|---|---|
| **CoAP** | Very low | Very low | Very low | Request / Response | Fast, ultra-low-energy constrained nodes |
| **MQTT** | Low | Low | Low | Publish / Subscribe | A balanced, general-purpose choice |
| **DDS** | Medium | Medium | Very low | Publish / Subscribe | Real-time systems |
| **AMQP** | Medium | High | Medium | Message queue (broker) | Heavyweight, reliable messaging |
| **HTTP** | High | High | Medium–High | Request / Response | Heavy, web-integrated workloads |

### Star vs. Mesh at scale

| Criterion | Star | Mesh |
|---|---|---|
| Architecture | Centralized (hub/gateway) | Distributed (multi-link) |
| Scalability | Limited – gateway bottleneck | Very high |
| Reliability | Low – single point of failure | Very high – self-healing |
| Energy use | Low | High (routing cost) |
| Management | Simple | Complex |

### Scalability ⇄ Security

- **Key management** and **centralized authentication** become bottlenecks as device counts rise.
- More devices mean more **collisions and retransmissions**, which widens the attack surface for **DDoS / botnet** attacks.
- Security layers add **protocol overhead**, which drains batteries and enables **sleep-deprivation attacks**.
- **Broker-based designs** (e.g. standard MQTT) create a **single point of failure** that can cascade through an entire smart-city-scale system.

### What helps

- **Edge & fog computing** – process data near the source to save bandwidth, cut latency and avoid a single point of failure
- **Software-Defined Networking (SDN)** – separate control from data plane for real-time visibility and traffic management
- **Lightweight cryptography** – security that fits constrained hardware without draining the battery
- **Adaptive networks** – dynamically switch communication methods, power policies and channels under congestion

## 🛠️ Topics & Technologies Covered

`IoT` · `MQTT` · `CoAP` · `AMQP` · `DDS` · `HTTP` · `6LoWPAN` · `RPL` · `6TiSCH` · `Zigbee` · `LoRaWAN` · `NB-IoT` · `BLE` · `TLS/DTLS` · `Edge/Fog Computing` · `SDN` · `Star & Mesh Topology`

## 📚 References

The report draws on 14 sources, including Al-Fuqaha et al. (2015), Atzori et al. (2010), Lin et al. (2017), Mirani et al. (2022), as well as the OASIS MQTT and IETF CoAP / TLS 1.3 specifications. The full list is in the report.

## 👩‍💻 Author

**Gözde Gönül**
GitHub: [@gozdegonul](https://github.com/gozdegonul)

---

<sub>⭐ If you found this useful, feel free to star the repository.</sub>
