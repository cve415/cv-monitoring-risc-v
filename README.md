🌐 The RISC-V Monitoring & Observability Landscape

RISC-V Ecosystem Analysis · Performance Monitoring · Uncore PMU · 2025

RISC-V is building the observability layer most people don't know they need—until their AI workload silently tanks.

🌅 The "Uncore" Thesis

Many fond memories in tech were during my years at New Relic and AppDynamics watching developers chase issues where the CPU looked fine, but latency spiked anyway. Usually, the culprit wasn't in the code the profiler could see—it was memory bandwidth saturation, cache thrashing, or interconnect contention happening outside the core.

RISC-V's new Uncore PMU proposal (originating from the team at Alibaba, Hangzhou) tackles exactly this blind spot. It standardizes performance monitoring for last-level cache, memory controllers, coherent interconnects, and I/O subsystems—the places where modern AI, HPC, and data center workloads actually live or die.

Why this matters:

Audience

The Value Proposition

🔧 For Developers

Get the same uncore visibility Intel and ARM engineers already take for granted. Shift from "tuning the scheduler" to "fixing the data layout" by seeing real memory bandwidth limits.

🐧 For Open-Source

A shared standard integrated with Linux perf. RISC-V won't fragment into proprietary monitoring silos; ecosystem cohesion beats vendor lock-in.

📈 For Business / GTM

This is infrastructure table stakes for cloud adoption. When customers ask, "Can you debug our bottlenecks?" this proposal gets the ecosystem to "yes."

🗺️ Leaders to Watch

Eight companies across five countries shaping the RISC-V observability stack.

🇨🇳 Alibaba (Hangzhou, China)

Category: Uncore PMU / Observability

Focus: The strongest signal for the Uncore PMU conversation. The Zhou Song proposal originates here. Alibaba remains a top-tier global RISC-V technical contributor.

🇮🇱 proteanTecs (Haifa, Israel)

Category: Uncore PMU / Observability

Focus: The clearest "observability" play. They embed hardware IP monitoring and analytics focused on visibility, power, performance, and reliability across the entire device lifecycle.

🇹🇼 Andes Technology (Hsinchu, Taiwan)

Category: IP / Silicon

Focus: A major RISC-V IP supplier. They have established key partnerships (e.g., with proteanTecs) to bake performance and reliability monitoring directly into their RISC-V cores.

🇵🇱 Antmicro (Gdańsk, Poland)

Category: Tooling / Integration

Focus: Deep in open hardware/software integration. They build the verification and simulation tooling (Renode, etc.) that makes hardware observability practical for software engineers.

🇺🇸 SiFive (San Mateo, CA, USA)

Category: IP / Silicon

Focus: The most recognized RISC-V processor IP brand. They set the benchmark for ecosystem maturity and platform-level monitoring integration.

🇨🇳 StarFive (Shanghai, China)

Category: Uncore PMU / Observability

Focus: Already shipping RISC-V performance tooling for hardware event monitoring, mapping directly to the uncore observability theme.

🇺🇸 Synopsys (Sunnyvale, CA, USA)

Category: Tooling / Integration

Focus: Verification and system-level tooling. Their EDA stack is essential for the "make RISC-V production-ready" movement.

🏁 Summary

Modern performance problems aren't in the core. RISC-V is finally making the uncore observable—and these are the companies building that future.

Analysis curated for the RISC-V Monitoring & Observability Landscape Project.


See https://github.com/cve415/risc-v-recruiting-agent
