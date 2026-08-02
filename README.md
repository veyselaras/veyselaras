# Veysel Aras

**Digital Design & Verification Engineer** · Ankara, Türkiye

I build UVM verification environments in SystemVerilog and take RTL from design to timing closure on FPGA. Computer Engineering, Sakarya University (2026).

[![LinkedIn](https://img.shields.io/badge/LinkedIn-veysel--aras-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/veysel-aras-b40232230/)
[![Email](https://img.shields.io/badge/Email-arasveysel4@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:arasveysel4@gmail.com)

---

## What I work on

- **Functional verification** — UVM 1.2, SystemVerilog, constrained-random stimulus, RAL, functional coverage, SVA, self-checking scoreboards
- **RTL & FPGA** — SystemVerilog/VHDL, Static Timing Analysis, Clock Domain Crossing, Quartus & Vivado
- **Protocols** — AXI4-Lite, APB3, I2C, SPI, UART, SpaceWire, Gigabit Ethernet
- **Python-side verification** — cocotb, cocotb extensions, testbench automation

Currently going deeper into **formal verification** (Seligman et al.) and extending my **AXI4-Lite UVM environment** toward full-protocol coverage.

---

## Featured projects

### 🔐 [ascon-fpga-udp](https://github.com/veyselaras/ascon-fpga-udp) — Real-time FPGA encryption gateway
A transparent inline encryptor on a Terasic DE2-115 (Cyclone IV E). Dual Gigabit Ethernet: plaintext in on ENET0, ASCON-AEAD128 authenticated ciphertext out on ENET1, and the reverse path simultaneously. Fully implemented in hardware — no CPU, no software on the data path. ASCON is the NIST SP 800-232 lightweight AEAD standard.
`SystemVerilog` · `Quartus` · `cocotb`

### 📡 [I2C_UVM](https://github.com/veyselaras/I2C_UVM) — APB I2C Master verification environment
Full UVM testbench for the PULP Platform APB I2C master. Two coordinated agents: an **active APB master agent** programming the DUT registers and a **reactive I2C slave agent** built on the Verilab reactive-slave methodology. Includes a predictor-based RAL model, SVA assertions, dual-domain functional coverage, and a self-checking scoreboard that correlates data across both buses.
`SystemVerilog` · `UVM 1.2` · `Xcelium`

### 🚌 [AXI4L_UVM](https://github.com/veyselaras/AXI4L_UVM) — AXI4-Lite UVM agent & environment
A reusable AXI4-Lite agent written from the ground up — interface, sequence item, config, driver, monitor, sequencer, agent, env, scoreboard, coverage — plus an assertion layer derived from the ARM protocol assertion specification. Covers SLVERR responses, WSTRB byte-lane gating, and reset behaviour. Bugs found during bring-up are documented in the README.
`SystemVerilog` · `UVM 1.2` · `Xcelium`

### 🔗 [UVM_SPI_agent](https://github.com/veyselaras/UVM_SPI_agent) — SPI Master verification environment
UVM environment acting as an SPI slave in Mode 0: drives MISO on the trailing edge, samples MOSI on the leading edge, and checks the `i_TX_DV` / `o_TX_Ready` handshake with interface-embedded SVA. Constrained-random sequences with a configurable inter-transfer delay for setup/hold stress.
`SystemVerilog` · `UVM`

### 🛰️ [cocotbext-spacewire](https://github.com/veyselaras/cocotbext-spacewire) — SpaceWire VIP for cocotb
A SpaceWire verification IP implementing the ECSS-E-ST-50-12C standard: DS signal-layer codec, character layer with parity, the full link FSM (ErrorReset → Run with 6.4 µs / 12.8 µs timers), credit-based flow control, and a packet API. VIP↔VIP loopback verified in Icarus Verilog.
**Built entirely by vibe coding** — I read the ECSS / Parkes sections, wrote detailed phase-by-phase prompts against them and reviewed the output; none of the code was hand-written or manually edited by me.
`Python` · `cocotb`

### 🔄 [Asenkron-FIFO-Implementasyonu](https://github.com/veyselaras/Asenkron-FIFO-Implementasyonu) — Asynchronous FIFO
Clock-domain-crossing FIFO following Clifford Cummings' Gray-code pointer synchronization paper.
`VHDL`

---

## Toolbox

![SystemVerilog](https://img.shields.io/badge/SystemVerilog-1A5276?style=flat&logoColor=white)
![VHDL](https://img.shields.io/badge/VHDL-1F618D?style=flat&logoColor=white)
![UVM](https://img.shields.io/badge/UVM-2874A6?style=flat&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![cocotb](https://img.shields.io/badge/cocotb-306998?style=flat&logoColor=white)

**Simulation & synthesis:** Xcelium · ModelSim/Questa · Icarus Verilog · Quartus · Vivado · EDA Playground
**Also:** RISC-V, computer architecture, Zephyr RTOS, BLE (nRF52), Assembly, C#

---

## Experience

**Embedded Software Developer (Intern)** — ACRUX Digital Technology, Ankara · Aug–Sep 2025
Developed BLE firmware on nRF52820 with Zephyr RTOS: sleep-cycle power optimization, USB CDC-ACM dynamic configuration with NVS persistence, and a hash-based secure command mechanism. Shipped end to end as BTS v1.0.1 to series production.

**Software Intern** — MEFA Industry, Ankara · Jul–Aug 2025
Built a neural network from scratch in C++ — feedforward, loss computation and optimization implemented by hand — reaching 96.11% accuracy on MNIST.

---

## Get in touch

📫 **arasveysel4@gmail.com** · 💼 [LinkedIn](https://www.linkedin.com/in/veysel-aras-b40232230/)

Open to digital design & verification roles.
