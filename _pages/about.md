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

I am a fourth-year undergraduate student at Nanjing University of Posts and Telecommunications. I will pursue a master's degree at the Institute of Computing Technology, Chinese Academy of Sciences, with joint training at Huawei. My graduate advisor is Prof. Ke Liu, and my Huawei mentor is Zixuan Guan.

My research interests are in computer systems and architecture, with a current focus on CXL memory pooling, memory congestion, next-generation interconnection systems, AI accelerators, computer networks, and quantum computing compilation.

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
- Quantum computing compilation: studying mapping and scheduling techniques for quantum circuits under hardware resource constraints.
