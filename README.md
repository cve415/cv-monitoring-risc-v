# 🌐 The RISC-V Monitoring & Observability Landscape

Many fond memories of performance monitoring and observability innovation from my years at New Relic and AppDynamics working with developers, solving issues across front-end and server code. Usually, the culprit was memory bandwidth saturation, cache thrashing, or interconnect contention happening outside the core—things that used to be difficult to see until it was too late.

RISC-V's new Uncore PMU proposal (originating from the team at Alibaba, Hangzhou) tackles exactly this blind spot. It standardizes performance monitoring for last-level cache, memory controllers, coherent interconnects, and I/O subsystems—critical to modern AI, HPC, and data center workload stability + scalability.


| Audience | The Value Proposition |
| :--- | :--- |
| **🔧 For Developers** | Get the same uncore visibility Intel and ARM engineers already take for granted. Shift from "tuning the scheduler" to "fixing the data layout" by seeing real memory bandwidth limits. |
| **🐧 For Open-Source** | A shared standard integrated with Linux perf. RISC-V won't fragment into proprietary monitoring silos; ecosystem cohesion beats vendor lock-in. |
| **📈 For Business / GTM** | This is infrastructure table stakes for cloud adoption. When customers ask, "Can you debug our bottlenecks?" this proposal gets the ecosystem to "yes." |

---
## 🗺️ 10 companies (across 5 countries) shaping RISC-V observability.


### 🇨🇳 Alibaba (Hangzhou, China)
* **Category:** Uncore PMU / Observability
* **Focus:** Originator of the Zhou Song Uncore PMU proposal.

### 🇮🇱 proteanTecs (Haifa, Israel)
* **Category:** Uncore PMU / Observability
* **Focus:** Deep visibility IP for silicon health and performance monitoring.

### 🇹🇼 Andes Technology (Hsinchu, Taiwan)
* **Category:** IP / Silicon
* **Focus:** Major IP supplier integrating observability hooks into commercial cores.

### 🇵🇱 Antmicro (Gdańsk, Poland)
* **Category:** Tooling / Integration
* **Focus:** Open-source simulation and verification (Renode).

### 🇺🇸 SiFive (San Mateo, CA, USA)
* **Category:** IP / Silicon
* **Focus:** Benchmark for ecosystem maturity and high-performance monitoring.

### 🇨🇳 StarFive (Shanghai, China)
* **Category:** Uncore PMU / Observability
* **Focus:** Hardware event monitoring tools for the RISC-V ecosystem.

### 🇺🇸 Synopsys (Sunnyvale, CA, USA)
* **Category:** Tooling / Integration
* **Focus:** System-level verification and EDA stack essentials.

🇺🇸 Breker Verification Systems (San Jose, CA, USA)
Category: Tooling / Integration
Focus: Cache coherency verification and system-level pre-silicon validation.

🇺🇸 Akeana (San Jose, CA, USA)
Category: Uncore PMU / Observability
 
---

## 🏁 Summary
Modern performance problems aren't in the core. RISC-V is finally making the uncore observable—and these are the companies building that future.

I am actively building a RISC-V Recruiting Agent: https://github.com/cve415/risc-v-recruiting-agent
