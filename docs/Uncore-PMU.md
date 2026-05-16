# 📑 RISC-V Architectural Standards Proposal: Uncore PMU

* **Proposer:** Jing Zhang  
* **Organization/Affiliation:** Alibaba Cloud Computing Co. Ltd  
* **Status:** Task Group Architecture Formulation  
* **Target Domain:** Datacenter, Cloud Infrastructure, & High-Performance Computing (HPC)

---

## 🚀 1. Introduction & Context

The **Uncore Performance Monitoring Unit (Uncore PMU)** extension defines a standardized, Memory-Mapped I/O (MMIO)-based interface for performance monitoring of system-level (non-core) components across RISC-V Silicon-on-Chips (SoCs). 

Unlike core-local execution metrics, this extension isolates tracking parameters across shared microarchitectural subsystems:
* **Last-Level Caches (LLC)** & Shared System Caches
* **Interconnect Fabrics** (Ring buses, Meshes, Crossbars)
* **Memory Controllers** (DDR, HBM queue depths/bank conflicts)
* **I/O Bridges & PCIe Controllers** (DMA and transactional throughput)

---

## ⚠️ 2. Architectural Gaps: Why Core-Local Extensions Are Insufficient

Existing performance monitoring layers on RISC-V are bound tightly to individual processor execution streams (`per-hart`) and cannot observe shared system resources:

| Existing Infrastructure Layer | Architectural Boundary / Paradigm | Telemetry Blind Spot |
| :--- | :--- | :--- |
| **`Zihpm`** *(Hardware Performance Monitor)* | Per-hart Control & Status Registers (CSRs: `mhpmcounter3-31`) | Inherently tied to a single hart; invisible to multi-tenant interconnect cross-traffic. |
| **`Sscofpmf`** *(Count Overflow & Filtering)* | Adds overflow interrupts & privilege filters to per-hart CSRs | Operates strictly within the isolated local hart execution paradigm. |
| **`SBI PMU Extension`** | Firmware abstraction layer for portable runtime counter access | Completely lacks definitions or interfaces for non-core, system-level uncore blocks. |

---

## 💥 3. The Datacenter & HPC Bottleneck

As enterprise workloads migrate to open silicon, the absence of a cross-platform uncore specification results in severe infrastructure constraints:
1. **Invisible System Bottlenecks:** Performance engineers cannot diagnose last-level cache contention, interconnect saturation, or real-time memory bandwidth limits.
2. **Telemetry Failure in Cloud Multi-Tenancy:** Cloud service providers cannot expose accurate hardware Quality-of-Service (QoS), billing analytics, or predictive capacity telemetry.
3. **Ecosystem & Tooling Fragmentation:** SoC vendors ship incompatible, proprietary register layouts and event encodings. This forces software developers to build and maintain bespoke, per-vendor Linux driver plugins.
4. **Virtualization Roadblocks:** Hypervisors have no common baseline to safely partition or expose uncore hardware performance metrics to guest virtual machines.

---

## 🛠️ 4. Core Design Principles

* **RISC-V Native Design:** Designed from first principles for multi-hart, multi-chiplet topologies; not clunky ports of legacy architectural concepts.
* **Backward Compatibility:** Zero modifications to existing hart-local structures (`Zihpm`, `Sscofpmf`, `SBI PMU`).
* **Vendor Extensibility:** Registers ample space for custom, implementation-specific microarchitectural events and filtering hooks while mandating standard baseline tracking.
* **Linux perf First-Class Integration:** Explicitly designed to leverage a generic Linux driver model with a vendor-extensible callback architecture out-of-the-box.
* **Virtualization Awareness:** Built with multi-tenant isolation, safe hypervisor pass-through control, and counter partitioning models in mind.

---

## 🎯 5. Core Specification Objectives

The Uncore PMU Task Group governs the standardization of five distinct implementation pillars:
