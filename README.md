# AI-Powered Drone System for Early Detection of Stampede and Crowd Panic Events

## 📌 Overview

This project presents an **AI-enabled autonomous drone system** designed to detect early signs of **stampede and crowd panic events** in real time. The system integrates a **dual-core SHAKTI RISC-V SoC** on an **Artix-7 FPGA**, combining **flight control** and **edge AI inference** in a tightly coupled architecture.

The solution targets **public safety, surveillance, and smart city deployments**, enabling **low-latency, on-device decision-making** without reliance on cloud infrastructure. 

---

## 🚀 Key Features

* 🧠 **Onboard Edge AI**

  * Real-time crowd anomaly detection using a lightweight CNN
  * No cloud dependency → reduced latency and enhanced privacy

* ⚙️ **Dual-Core SHAKTI Architecture**

  * Core 0 → Flight Control (FreeRTOS)
  * Core 1 → AI Inference (Bare-metal)

* 🔌 **FPGA-Based SoC (Artix-7)**

  * Reconfigurable hardware for multi-mission adaptability
  * AXI4-based modular interconnect

* ⚡ **Hardware Acceleration**

  * CNN accelerator leveraging DSP slices
  * ~5 ms inference latency

* 🔐 **Secure & Indigenous**

  * Built on open-source SHAKTI RISC-V ecosystem
  * Fully auditable and locally manufacturable

---

## 🏗️ System Architecture

### Hardware Components

* **Processor:** SHAKTI Yamuna Dual-Core (RV32IMAC)
* **FPGA Platform:** Xilinx Artix-7 100T
* **Memory:** 256 MB DDR3 (External)
* **Camera:** OV7670 (DVP Interface)
* **Sensors & Modules:**

  * IMU (I2C)
  * GPS (UART)
  * LoRa Communication (SPI)
  * Motors/ESCs (PWM/GPIO)

### Interconnect

* **AXI4 Crossbar**

  * Connects processors, memory, and peripherals
* **DDR3 Memory Controller (MIG)**
* **Camera DMA Engine**

(*Refer to block diagram on page 5 & 13 of the PPT*) 

---

## 🧠 Software Architecture

### Asymmetric Multiprocessing (AMP)

* **Core 0 (Flight Controller)**

  * Runs **FreeRTOS**
  * Handles:

    * PID control loops
    * Sensor fusion (Kalman Filter)
    * Motor control

* **Core 1 (AI Controller)**

  * Runs **bare-metal C application**
  * Handles:

    * Image processing
    * CNN inference
    * Event detection

### AI Model

* Lightweight **8-bit quantized CNN**
* Input: **64×64 grayscale video frames**
* Optimized for:

  * Low memory footprint
  * Fast inference

---

## 📊 Project Objectives

1. Design and implement a **custom SoC** on FPGA
2. Develop a **dual-core AMP system**
3. Enable **real-time onboard AI processing**
4. Build a **low-power surveillance drone for crowd safety** 

---

## 💡 Novel Contributions

* First **indigenous drone platform** based on SHAKTI RISC-V + FPGA
* Fully **edge-based AI inference system**
* Modular, **reprogrammable flight controller**
* Cost-effective alternative to GPU-based drones (~30–40% cheaper)
* Improved efficiency (~40–60% lower power consumption) 

---

## 📅 Development Roadmap

### Phase 1: Foundation (Month 1–3)

* Dataset preparation & CNN benchmarking
* RTL simulation of dual-core SoC
* Peripheral IP development (UART, PWM, I2C)
* FreeRTOS porting
* Camera interfacing & basic AI testing

### Phase 2: Integration (Month 4–6)

* Drone frame design & hardware integration
* Sensor fusion and PID tuning
* CNN accelerator deployment
* Real-time video streaming via DMA
* Autonomous flight testing & validation

(*Detailed milestones described on pages 7–8*) 

---

## 📈 Applications

* 🚓 Public safety & law enforcement
* 🏟️ Large event monitoring
* 🏗️ Industrial site surveillance
* ⚡ Critical infrastructure protection
* 🛡️ Defense & homeland security

---

## 💰 Business Potential

* Targeting **$5B+ global surveillance market**
* Scalable deployment:

  * 50–100 units/year initially
* Future model:

  * Drone-as-a-Service (DrAAS)
  * Real-time analytics dashboards

---

## 🛠️ Tools & Technologies

* **Hardware Design:** Vivado, Vitis
* **Processor:** SHAKTI (Yamuna)
* **RTOS:** FreeRTOS
* **AI Framework:** TensorFlow Lite (Quantized models)
* **Languages:** Verilog, C
* **Communication:** AXI4, UART, SPI, I2C

---

## 🏫 Institutional Support

* Vidya Pratishthan's K.B. Institute of Engineering & Technology
* Collaboration initiatives with:

  * NIT Goa
  * MKCL Maharashtra
* Potential deployment for **Kumbh Mela 2027**

---

## 👥 Team

**Team Name:** ASHKARA
**Team Lead:** Pratik Mhasawade
**Processor Platform:** SHAKTI RISC-V 

---

## 📷 Demo & GUI

The system includes a GUI for:

* Camera control
* Image preprocessing (grayscale/BW)
* Crowd detection visualization

(*Refer to GUI snapshot on page 12*) 

---

## 🔮 Future Scope

* Enhanced AI models (multi-class anomaly detection)
* Swarm drone coordination
* Integration with smart city infrastructure
* Real-time alert dashboards for authorities

---

## 📜 License

Open-source (aligned with SHAKTI ecosystem philosophy)

---

## 🙌 Acknowledgment

This project is developed under the **Chips to Startup (C2S) initiative**, promoting indigenous semiconductor innovation.

---

## 📬 Contact

For collaboration, research, or deployment inquiries:

* Team ASHKARA

---

⭐ *Building intelligent, secure, and indigenous surveillance systems for a safer future.*
