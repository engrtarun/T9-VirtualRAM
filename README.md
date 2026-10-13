# T9 VirtualRAM — Research & Distributed Memory Architecture

A centralized repository organizing core research papers, frameworks, and implementations referenced in the **T9 VirtualRAM Research** documentation.

This repository tracks cutting-edge projects across Distributed Shared Memory (DSM), Remote Memory Pooling, Memory Disaggregation & Swap Systems, Compute Express Link (CXL), RAM Disks, and Kernel-Level DMA Analysis.

---

## 📌 Submodules Overview

All external repositories are integrated as lightweight Git submodules. 

| Category | Repository | Description | Link |
| :--- | :--- | :--- | :--- |
| **Distributed Shared Memory & Pooling** | `r3map` | High-performance remote memory region mounts and migrations in user space using Go. | [pojntfx/r3map](https://github.com/pojntfx/r3map) |
| | `MemLiner` | Remote-memory-friendly runtime system for memory-disaggregated clusters. | [uclasystem/MemLiner](https://github.com/uclasystem/MemLiner) |
| | `canvas` | Isolated and adaptive swapping for multi-applications on remote memory. | [uclasystem/canvas](https://github.com/uclasystem/canvas) |
| | `Mako` | Low-pause, high-throughput garbage collector designed for memory-disaggregated datacenters. | [uclasystem/Mako](https://github.com/uclasystem/Mako) |
| | `rmpool` | C++ remote memory pooling mechanism across network-connected machines. | [dopecoder/rmpool](https://github.com/dopecoder/rmpool) |
| | `puma` | Kernel-level remote memory caching framework for datacenter VMs. | [mlorrillere/puma](https://github.com/mlorrillere/puma) |
| | `hclib` | Task-based parallel programming model supporting shared and distributed memory. | [habanero-rice/hclib](https://github.com/habanero-rice/hclib) |
| **Memory Disaggregation & Swap Systems** | `Infiniswap` | RDMA-based decentralized swap paging for efficient memory disaggregation. | [SymbioticLab/Infiniswap](https://github.com/SymbioticLab/Infiniswap) |
| | `fastswap` | Fast swap system for far memory over high-speed RDMA networks. | [clusterfarmem/fastswap](https://github.com/clusterfarmem/fastswap) |
| | `cfm` | Cluster far-memory framework complementing fastswap-driven disaggregation. | [clusterfarmem/cfm](https://github.com/clusterfarmem/cfm) |
| **CXL (Compute Express Link)** | `SimCXL` | Full-system cycle-level simulator based on gem5 supporting all CXL protocols and device types. | [TianheMICALab/SimCXL](https://github.com/TianheMICALab/SimCXL) |
| | `cxl-reskit` | CXL Memory Resource Kit (CMRK) with diagnostics, benchmarks, and management utilities. | [cxl-reskit/cxl-reskit](https://github.com/cxl-reskit/cxl-reskit) |
| **RAM Disk & Block-Level Caching** | `rapiddisk` | Advanced Linux RAM drive and caching kernel modules with RESTful API and NVMe Target support. | [pkoutoupis/rapiddisk](https://github.com/pkoutoupis/rapiddisk) |
| **Kernel Memory & DMA Analysis** | `rwMem` | Kernel module to read/write memory and set hardware breakpoints in remote processes. | [ri-char/rwMem](https://github.com/ri-char/rwMem) |
| | `LeechCore` | Physical memory acquisition library & remote acquisition agent. | [ufrisk/LeechCore](https://github.com/ufrisk/LeechCore) |
| | `pcileech` | Direct Memory Access (DMA) attack and memory acquisition framework over PCIe and network. | [ufrisk/pcileech](https://github.com/ufrisk/pcileech) |

---

## 🚀 Cloning & Working with Submodules

### 1. Shallow / Standard Clone (No submodules downloaded locally)
By default, cloning this repository does **NOT** download the submodules' contents, saving disk space and network bandwidth:
```bash
git clone https://github.com/engrtarun/T9-VirtualRAM.git
```

### 2. Selective Submodule Initialization
If you only need to inspect one specific repository without downloading the rest:
```bash
# Example: Initialize only r3map
git submodule update --init submodules/r3map
```

### 3. Full Clone (All submodules)
To fetch all submodules including their source files:
```bash
git clone --recurse-submodules https://github.com/engrtarun/T9-VirtualRAM.git
```
*(Warning: Repositories such as MemLiner exceed 300MB+).*

---

## 📄 Reference Document
- [Research PDF Document](./resarch%20__%20T9%20VirtualRAM.pdf)
