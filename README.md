# Awesome-Robotics-Middleware-Platforms

## Top Robotics Middleware Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Publish-Subscribe Messaging, Data Distribution Service & Real-Time Robot Communication*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Robotics Middleware**. These tools provide the communication backbone for robot systems — enabling typed message exchange, discovery, quality-of-service management, and coordination between distributed software components across sensors, actuators, and compute nodes.



**Examples** include ROS (Robot Operating System), ROS 2, eProsima Fast DDS, RTI Connext DDS, Eclipse Cyclone DDS, Zenoh, YARP, OROCOS, LCM, and Cyber RT (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom transport layers, and transparent robot communication — ideal for robotics engineers prioritizing control, researchers building custom stacks, and teams avoiding vendor lock-in.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[RTI Connext DDS](https://www.rti.com/)**  

  The world's leading commercial implementation of the DDS standard, trusted in over 2,000 designs for real-time data distribution in autonomous systems, medical robotics, and aerospace. Free for prototyping, research, and academic use; commercial licenses available for production deployments. Integrates directly with ROS 2 as an alternative RMW implementation.



- **[GurumDDS](https://www.gurum.co.kr/)**  

  Commercial DDS implementation from GurumNetworks, supported as an RMW option in ROS 2 binary releases. Provides full DDS capabilities with vendor support for industrial robotics applications.



- **[MathWorks ROS Toolbox](https://www.mathworks.com/products/ros.html)**  

  MATLAB/Simulink integration with ROS and ROS 2 for algorithm development, simulation, and deployment. Commercial licensing required for production use.



- **[ZettaScale Zenoh (Commercial Support)](https://www.zettascale.tech/)**  

  Commercial support and services for the Eclipse Zenoh protocol, offering lightweight publish-subscribe and querying for robotics and edge computing.



- **[AWS IoT Greengrass](https://aws.amazon.com/greengrass/)**  

  Edge runtime that can bridge ROS 2 systems to AWS cloud services for fleet management, OTA updates, and data ingestion.



## Open-Source GitHub Projects



- **[ROS 2 (Robot Operating System 2)](https://github.com/ros2/ros2)**  

  **The dominant open-source robotics middleware**, built on a peer-to-peer DDS foundation. Provides publish-subscribe messaging, synchronous RPC, and action-based task execution for long-running goals with periodic feedback. Features an interface definition language for type-safe message/service/action generation, fine-grained Quality of Service profiles, and multi-vendor RMW support. Apache 2.0 licensed.



- **[eProsima Fast DDS](https://github.com/eProsima/Fast-DDS)**  

  **The default ROS 2 middleware** (rmw_fastrtps_cpp) since the beginning of ROS 2. Apache 2.0 licensed, packaged with ROS 2 binary releases. Claims ~30% lower inter-process latency than Cyclone DDS in benchmark comparisons, with delays below 20μs for packets up to 15kB and throughput in the order of 10^4 MB/s.



- **[Eclipse Cyclone DDS](https://github.com/eclipse-cyclonedds/cyclonedds)**  

  Free and open-source DDS implementation focused on **high throughput and low delay**. Eclipse Public License v2.0, supported as rmw_cyclonedds_cpp in ROS 2. One of the lighter DDS implementations, optimized for real-time deterministic communication.



- **[Eclipse Zenoh](https://github.com/eclipse-zenoh/zenoh)**  

  **Lightweight alternative to DDS** designed for IoT and edge computing with high throughput, low latency, and interoperability across heterogeneous environments. Provides **~97-99.9% reduction in discovery overhead** compared to typical DDS, making it well-suited for wireless networks where DDS discovery can cause network downtime. Packaged with ROS 2 binary releases starting with Kilted Kaiju (rmw_zenoh_cpp). Apache 2.0 / EPL 2.0 licensed.



- **[YARP (Yet Another Robot Platform)](https://github.com/robotology/yarp)**  

  Open-source middleware for robot communication and control, developed by the Italian Institute of Technology. Provides publish-subscribe and RPC mechanisms with bindings for C++, Python, and other languages. Used in iCub humanoid robot and humanoid robotics research.



- **[OROCOS (Open Robot Control Software)](https://github.com/orocos)**  

  Open-source framework for real-time robot control, with the **Orocos Real-Time Toolkit (RTT)** providing a C++ framework for building real-time control components. Emphasis on deterministic, hard real-time behavior.



- **[LCM (Lightweight Communications and Marshalling)](https://github.com/lcm-proj/lcm)**  

  **Low-latency message passing library** for real-time robotics research. Uses UDP multicast for push-based publish/subscribe without a centralized hub. Features a platform-independent type specification language with automatic marshalling code generation for C, Java, Python, and MATLAB. Notable for real-time deep traffic inspection tools that decode and display messages with minimal user effort and no performance penalty. LGPL licensed.



- **[Dora (dora-rs)](https://github.com/dora-rs/dora)**  

  Robotics dataflow framework and distributed orchestrator for building and managing processing pipelines. Supports multi-language nodes (Rust, Python, C, C++) with **zero-copy shared-memory transport** and columnar formats for minimal latency on large payloads. Includes bidirectional bridges to external ecosystems. Rust-based.



- **[Links and Nodes (LN)](https://gitlab.com/links_and_nodes/ln)**  

  Open-source middleware for distributed real-time robotic systems from DLR (German Aerospace Center). Combines process management with fast publish/subscribe messaging and request/response services, allowing complex multi-process systems to be reproduced from one text file. Developed since 2010, released as open source in 2015. Supports robotics applications requiring deterministic behavior and low-latency communication across hosts and programming languages.



- **[HORUS](https://pypi.org/project/horus-robotics/)**  

  Ultra-low latency robotics framework built in Rust with Python bindings. Claims **87ns IPC latency and 12M+ messages/second throughput** — described as 100x faster than ROS 2. Features zero-copy shared memory transport, type-safe message validation, cross-language interoperability (Rust/C++/Python), and real-time priority-based scheduling with deadline guarantees. Apache 2.0 licensed.



- **[Open-RAIL](https://github.com/CMCC-TAO/open-rail)**  

  Open-source middleware from China Mobile linking **Vision-Language-Action (VLA) and World-Action Models (WAM)** to real robot hardware. Lightweight server-client framework with three-thread asynchronous pipeline (observation, inference, control) and two-level online smoothing. Hardware abstraction layer standardizes control, state reading, and action execution — a new robot adapter reuses upper-layer logic after a thin driver step. Adapting a new VLA/WAM model requires ~50-100 lines of code. Apache 2.0 licensed.



- **[SONNY OS](https://github.com/JackTrainer/Sonny)**  

  Ultra-lightweight, agnostically unified open-source **microkernel for any robot** (arms, AMRs, drones, humanoids). Built in Rust and **Zenoh**, positioned as a ROS 2 replacement eliminating memory leaks and latency. Features JSON-based hardware abstraction layer, WASM sandbox for skill execution, and a real-time hard-watchdog monitoring sub-millisecond jitter. Supports KUKA, Comau, Universal Robots, Franka Emika, Luwu Dynamics XGO, and standard AMRs out of the box. AGPLv3 licensed.



- **[ZRM (Zenoh ROS-like Middleware)](https://pypi.org/project/zrm/)**  

  Minimal, single-file communication middleware built on Zenoh with a clean API inspired by ROS 2 patterns. Features protobuf-based serialization with runtime type checking, Pythonic API, and CLI tools (`zrm-topic list`, `zrm-topic echo`, `zrm-topic pub`, `zrm-topic hz`). Provides Publisher/Subscriber, Link (point-to-point), and service patterns.



- **[Wrapyfi](https://github.com/fabawi/wrapyfi)**  

  Python wrapper for message-oriented and robotics middleware, providing a unified API across ROS, ROS 2, YARP, ZeroMQ, and other transports. Reduces boilerplate when integrating heterogeneous middleware systems.



### Additional Strong Open-Source Options



- **GurumDDS** — Commercial DDS implementation with ROS 2 RMW support, available in ROS 2 binary releases.

- **Cyber RT** — Apollo's runtime framework for autonomous driving, built on a component-based architecture with high-performance communication.

- **YARP** — Yet Another Robot Platform for humanoid robotics middleware.

- **OROCOS RTT** — Real-Time Toolkit for deterministic robot control components.

- **pico Zenoh** — Microcontroller-compatible Zenoh variant for resource-constrained robotics applications.



**Frameworks for building custom systems**: Combine **ROS 2** for standardized robot communication, **Fast DDS** or **Cyclone DDS** for DDS-based transport, **Zenoh** for lightweight wireless-friendly messaging, **LCM** for minimal-latency research systems, and **Open-RAIL** or **SONNY OS** for VLA/model-to-hardware integration to build a complete robotics middleware stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Robotics middleware platforms must comply with safety regulations, real-time constraints, and network security requirements. Incorrect middleware configuration can cause communication failures in safety-critical systems.

- Self-hosted open-source solutions require proper network configuration, QoS tuning, and validation for real-time behavior.



---



**Made for robotics engineers, autonomous systems developers, middleware architects, and teams building robot communication platforms.**  

Let's make robotics middleware more open, performant, and robot-friendly.
