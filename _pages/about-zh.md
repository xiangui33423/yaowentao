---
permalink: /zh/
title: "姚文涛"
lang: zh
alternate_url: /
author_profile: true
---

{% include language-switch.html %}

我是南京邮电大学四年级本科生，即将前往中国科学院计算技术研究所攻读硕士学位，并在华为进行联合培养。我的研究生导师是刘珂教授，华为导师是管紫轩。

我的研究兴趣集中在 computer systems and architecture，目前关注 CXL memory pooling、memory congestion、下一代互连系统、AI accelerators、computer networks 和 quantum computing compilation。

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
- Quantum computing compilation：研究硬件资源约束下的 quantum circuit mapping 和 scheduling techniques。
