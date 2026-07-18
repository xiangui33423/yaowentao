---
permalink: /zh/
title: "姚文涛"
lang: zh
alternate_url: /
author_profile: true
---

{% include language-switch.html %}

我是中国科学院计算技术研究所一年级硕士研究生，在华为进行联合培养。我的研究生导师是刘珂教授，华为导师是管紫轩。

我的研究兴趣集中在 computer systems and architecture，目前关注 CXL memory pooling、memory congestion、下一代互连系统、AI accelerators、computer networks 和 LLM KVCache 管理与优化。

[下载简历]({{ '/files/yaowentao-cv.pdf' | relative_url }})

## 代表项目

<div class="project-callout">
  <h3>LocWeave</h3>
  <p class="project-subtitle">Locality Isolation for CXL Memory Pooling</p>
  <p>CXL memory pooling 可以提升容量和带宽共享能力，但细粒度 interleaving 可能会把不兼容的 requester streams 混入共享内存设备，破坏 memory locality。LocWeave 探索 pattern-aware placement 和 remapping 机制，以降低 multi-host CXL systems 中的干扰。</p>
  <p class="tag-row"><span>CXL Memory Pooling</span><span>Memory Congestion</span><span>Memory Systems</span><span>gem5</span><span>DRAMSim3</span></p>
</div>

<div class="project-callout">
  <h3>HeteroSim</h3>
  <p class="project-subtitle">Memory-Space Design Exploration Simulator for Multi-Chiplet LLM Accelerators</p>
  <p>HeteroSim 是一个用于 multi-chiplet LLM accelerators 的 memory-space design exploration simulator。它支持研究 heterogeneous memory organization、chiplet-level resource allocation 和 accelerator data movement 如何影响大模型 inference 与 training 效率。</p>
  <p class="tag-row"><span>LLM Accelerators</span><span>Multi-Chiplet Systems</span><span>Memory Space Design</span><span>Architecture Simulation</span></p>
</div>

<div class="project-callout">
  <h3>Mooncake Master Snapshot Refactoring</h3>
  <p class="project-subtitle">KVCache-Centric Serving System Snapshot Subsystem Refactor</p>
  <p>围绕 Mooncake Store 的 RFC <a href="https://github.com/kvcache-ai/Mooncake/issues/2688">#2688</a>，我将 master snapshot 的 orchestration、repository、codec 和 restore path 从 monolithic <code>MasterService</code> 中拆分出来，并通过 4 个已合并 PR 渐进式落地：<a href="https://github.com/kvcache-ai/Mooncake/pull/2805">#2805</a>、<a href="https://github.com/kvcache-ai/Mooncake/pull/2831">#2831</a>、<a href="https://github.com/kvcache-ai/Mooncake/pull/2879">#2879</a>、<a href="https://github.com/kvcache-ai/Mooncake/pull/2943">#2943</a>。该工作保持 snapshot format、配置和外部行为兼容，同时改善模块边界、测试性和后续格式演进空间。</p>
  <p class="tag-row"><span>Mooncake</span><span>KVCache Serving</span><span>Snapshot/Restore</span><span>C++</span><span>System Refactoring</span></p>
</div>

<div class="project-callout">
  <h3>AI Coprocessor Accelerator for LLM Workloads</h3>
  <p class="project-subtitle">Transformer-Oriented Accelerator Design</p>
  <p>该项目面向 LLM-oriented Transformer workloads 设计 AI coprocessor accelerator，探索高效 matrix computation、data movement 和 memory access patterns 的硬件支持。</p>
  <p class="tag-row"><span>LLM Acceleration</span><span>AI Coprocessor</span><span>Transformer</span><span>Hardware Design</span></p>
</div>

<div class="project-callout">
  <h3>Programmable Switch Data-Plane Project</h3>
  <p class="project-subtitle">P4-Based Switch and Packet-Processing Design</p>
  <p>该项目基于 P4-style programmable data planes 探索 switch behavior 和 packet-processing logic，重点是在 programmable switch 环境中构建并实验网络 forwarding functions。</p>
  <p class="tag-row"><span>Programmable Switch</span><span>P4</span><span>Data Plane</span><span>Computer Networks</span></p>
</div>

## 当前方向

- CXL pooling 的 memory systems：理解 shared and disaggregated memory 中的 congestion、interference 和 resource placement。
- 面向 LLMs 的 accelerator architecture：探索 chiplet-level memory organization、data movement 和面向 Transformer workloads 的 AI coprocessor 支持。
- Programmable networking：基于 P4-style data planes 原型化 packet-processing 和 forwarding mechanisms。
- LLM KVCache 系统：研究 KVCache 传输、管理与优化，以及分布式 KVCache serving 系统。

## 开源贡献

我参与了 [Mooncake](https://github.com/kvcache-ai/Mooncake) 开源项目的贡献。Mooncake 是一个面向大模型推理的 KVCache-centric serving 系统，关注高性能 KV cache 传输与分布式 KV cache 管理。

我已向 Mooncake 主分支合并 6 个 Pull Request：[#2691](https://github.com/kvcache-ai/Mooncake/pull/2691)、[#2754](https://github.com/kvcache-ai/Mooncake/pull/2754)、[#2805](https://github.com/kvcache-ai/Mooncake/pull/2805)、[#2831](https://github.com/kvcache-ai/Mooncake/pull/2831)、[#2879](https://github.com/kvcache-ai/Mooncake/pull/2879) 和 [#2943](https://github.com/kvcache-ai/Mooncake/pull/2943)。早期工作主要集中在 Transfer Engine 中的 GPU device 管理与多 GPU NVLink/MNNVL 通信正确性。

近期我围绕 RFC [#2688](https://github.com/kvcache-ai/Mooncake/issues/2688) 完成了 Mooncake Store master snapshot 子系统重构，并拆分为四个已合并 PR：

- [#2805](https://github.com/kvcache-ai/Mooncake/pull/2805)：提取 `MasterSnapshotManager` 和 `MasterSnapshotRepository`，将 snapshot scheduling、child process lifecycle、storage/catalog operations 从 `MasterService` 中拆分。
- [#2831](https://github.com/kvcache-ai/Mooncake/pull/2831)：提取 `MasterSnapshotCodec`，集中管理 master snapshot 的 encode/decode 逻辑，并补充 codec 单元测试。
- [#2879](https://github.com/kvcache-ai/Mooncake/pull/2879)：将 snapshot restore path 重构为 repository、codec、service apply 三阶段架构，保持已有 snapshot format 与 restore behavior 兼容。
- [#2943](https://github.com/kvcache-ai/Mooncake/pull/2943)：清理重构后的遗留 wrapper methods，并为三阶段 restore 架构补充文档。
