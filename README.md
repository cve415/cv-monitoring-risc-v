🌐 The RISC-V Monitoring & Observability Landscape

Many fond memories in performance, monitoring, and observability were during my years at New Relic and AppDynamics watching developers solve issues across front-end and server code. Usually, the culprit was memory bandwidth saturation, cache thrashing, or interconnect contention happening outside the core—things that used to be difficult to see until it was too late.

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

Focus: Originator of the Zhou Song Uncore PMU proposal.

🇮🇱 proteanTecs (Haifa, Israel)

Category: Uncore PMU / Observability

Focus: Deep visibility IP for silicon health and performance monitoring.

🇹🇼 Andes Technology (Hsinchu, Taiwan)

Category: IP / Silicon

Focus: Major IP supplier integrating observability hooks into commercial cores.

🇵🇱 Antmicro (Gdańsk, Poland)

Category: Tooling / Integration

Focus: Open-source simulation and verification (Renode).

🇺🇸 SiFive (San Mateo, CA, USA)

Category: IP / Silicon

Focus: Benchmark for ecosystem maturity and high-performance monitoring.

🇨🇳 StarFive (Shanghai, China)

Category: Uncore PMU / Observability

Focus: Hardware event monitoring tools for the RISC-V ecosystem.

🇺🇸 Synopsys (Sunnyvale, CA, USA)

Category: Tooling / Integration

Focus: System-level verification and EDA stack essentials.

🏁 Summary

Modern performance problems aren't in the core. RISC-V is finally making the uncore observable—and these are the companies building that future.

🚀 GitHub Pages Deployment Status

Current Status: Resolved ✅

The repository has been updated to use index.html as the primary entry point.

Primary Entry: index.html is now the root file, ensuring GitHub Pages renders the custom high-fidelity design.

Fallback: README.md (this file) serves as the technical documentation for developers browsing the repository directly.

NoJekyll: A .nojekyll file has been added to the root to ensure standard HTML/CSS assets are served without processing.

Analysis curated for the RISC-V Monitoring & Observability Landscape Project
