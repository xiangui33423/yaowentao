---
permalink: /
title: "wentao yao"
lang: en
alternate_url: /zh/
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% include language-switch.html %}

I am a first-year master's student at the Institute of Computing Technology, Chinese Academy of Sciences, with joint training at Huawei. My graduate advisor is Prof. Ke Liu, and my Huawei mentor is Zixuan Guan.

My research interests are in computer systems and architecture, with a current focus on CXL memory pooling, memory congestion, next-generation interconnection systems, AI accelerators, computer networks, and LLM KVCache management and optimization.

[Download CV]({{ '/files/yaowentao-cv.pdf' | relative_url }})

## Selected Projects

<div class="project-callout">
  <h3>LocWeave</h3>
  <p class="project-subtitle">Locality Isolation for CXL Memory Pooling</p>
  <p>CXL memory pooling improves capacity and bandwidth sharing, but fine-grained interleaving can destroy memory locality by mixing incompatible requester streams inside shared memory devices. LocWeave explores pattern-aware placement and remapping mechanisms to reduce interference in multi-host CXL systems.</p>
  <p class="tag-row"><span>CXL Memory Pooling</span><span>Memory Congestion</span><span>Memory Systems</span><span>gem5</span><span>DRAMSim3</span></p>
</div>

<div class="project-callout">
  <h3>HeteroSim</h3>
  <p class="project-subtitle">Memory-Space Design Exploration Simulator for Multi-Chiplet LLM Accelerators</p>
  <p>HeteroSim is a simulator for exploring memory-space design choices in multi-chiplet LLM accelerators. It supports architectural studies of how heterogeneous memory organization, chiplet-level resource allocation, and accelerator data movement affect large-model inference and training efficiency.</p>
  <p class="tag-row"><span>LLM Accelerators</span><span>Multi-Chiplet Systems</span><span>Memory Space Design</span><span>Architecture Simulation</span></p>
</div>

<div class="project-callout">
  <h3>Mooncake Master Snapshot Refactoring</h3>
  <p class="project-subtitle">KVCache-Centric Serving System Snapshot Subsystem Refactor</p>
  <p>Around Mooncake Store RFC <a href="https://github.com/kvcache-ai/Mooncake/issues/2688">#2688</a>, I split master snapshot orchestration, repository operations, codec logic, and restore flow out of the monolithic <code>MasterService</code> through 4 merged PRs: <a href="https://github.com/kvcache-ai/Mooncake/pull/2805">#2805</a>, <a href="https://github.com/kvcache-ai/Mooncake/pull/2831">#2831</a>, <a href="https://github.com/kvcache-ai/Mooncake/pull/2879">#2879</a>, and <a href="https://github.com/kvcache-ai/Mooncake/pull/2943">#2943</a>. The refactor preserves the snapshot format, configuration, and external behavior while improving module boundaries, testability, and future format evolution.</p>
  <p class="tag-row"><span>Mooncake</span><span>KVCache Serving</span><span>Snapshot/Restore</span><span>C++</span><span>System Refactoring</span></p>
</div>

<div class="project-callout">
  <h3>AI Coprocessor Accelerator for LLM Workloads</h3>
  <p class="project-subtitle">Transformer-Oriented Accelerator Design</p>
  <p>This project designs an AI coprocessor accelerator for LLM-oriented Transformer workloads. It explores hardware support for efficient matrix computation, data movement, and memory access patterns in neural-network inference acceleration.</p>
  <p class="tag-row"><span>LLM Acceleration</span><span>AI Coprocessor</span><span>Transformer</span><span>Hardware Design</span></p>
</div>

<div class="project-callout">
  <h3>Programmable Switch Data-Plane Project</h3>
  <p class="project-subtitle">P4-Based Switch and Packet-Processing Design</p>
  <p>This project explores switch behavior and packet-processing logic with P4-style programmable data planes. It focuses on building and experimenting with network forwarding functions in a programmable switch environment.</p>
  <p class="tag-row"><span>Programmable Switch</span><span>P4</span><span>Data Plane</span><span>Computer Networks</span></p>
</div>

## Current Directions

- Memory systems for CXL pooling: understanding congestion, interference, and resource placement in shared and disaggregated memory.
- Accelerator architecture for LLMs: exploring chiplet-level memory organization, data movement, and AI coprocessor support for Transformer workloads.
- Programmable networking: prototyping packet-processing and forwarding mechanisms with P4-style data planes.
- LLM KVCache systems: studying KVCache transfer, management, and optimization, as well as distributed KVCache serving systems.

## Open Source Contributions

I have contributed to the [Mooncake](https://github.com/kvcache-ai/Mooncake) open-source project. Mooncake is a KVCache-centric serving system for large language model inference, focusing on high-performance KV cache transfer and distributed KV cache management.

I have merged 6 Pull Requests into the main branch: [#2691](https://github.com/kvcache-ai/Mooncake/pull/2691), [#2754](https://github.com/kvcache-ai/Mooncake/pull/2754), [#2805](https://github.com/kvcache-ai/Mooncake/pull/2805), [#2831](https://github.com/kvcache-ai/Mooncake/pull/2831), [#2879](https://github.com/kvcache-ai/Mooncake/pull/2879), and [#2943](https://github.com/kvcache-ai/Mooncake/pull/2943). My earlier contributions focused on GPU device management in the Transfer Engine and correctness of multi-GPU NVLink/MNNVL communication.

Recently, I completed the Mooncake Store master snapshot subsystem refactor around RFC [#2688](https://github.com/kvcache-ai/Mooncake/issues/2688), split across four merged PRs:

- [#2805](https://github.com/kvcache-ai/Mooncake/pull/2805): extracted `MasterSnapshotManager` and `MasterSnapshotRepository`, separating snapshot scheduling, child process lifecycle, and storage/catalog operations from `MasterService`.
- [#2831](https://github.com/kvcache-ai/Mooncake/pull/2831): extracted `MasterSnapshotCodec` to own master snapshot encode/decode logic and added codec unit tests.
- [#2879](https://github.com/kvcache-ai/Mooncake/pull/2879): refactored the snapshot restore path into a repository, codec, and service-apply three-phase architecture while preserving snapshot format and restore behavior compatibility.
- [#2943](https://github.com/kvcache-ai/Mooncake/pull/2943): removed leftover wrapper methods after the refactor and documented the three-phase restore architecture.
