---
title: "Zion: A Comprehensive, Adaptive, and Lightweight Hardware Prefetcher"
collection: publications
category: conferences
permalink: /publication/2026-zion-date
date: 2026-04-01
paperurl: '/files/2026-04-DATE-Zion-HW-Prefetcher.pdf'
# citation: 'Biryukov, V., Lu, X., Liu, Z., Zhou, K., & Sun, X.-H. (2026). &quot;Zion: A Comprehensive, Adaptive, and Lightweight Hardware Prefetcher.&quot; <i>Design, Automation and Test in Europe Conference (DATE 2026)</i>.'
excerpt: '<b>Vadim Biryukov</b>, Xiaoyang Lu, Zirui Liu, Kaixiong Zhou, Xian-He Sun'
venue: 'Design, Automation and Test in Europe Conference <b>DATE 2026</b>'
---
Authors: <b>Vadim Biryukov</b>, Xiaoyang Lu, Zirui Liu, Kaixiong Zhou, Xian-He Sun

## Background

The widening processor-memory performance gap makes data access optimization critical, especially for memory-intensive workloads where off-chip latency dominates execution time. Attention-based computations in LLMs intensify this bottleneck through quadratic growth in memory complexity, driving frequent traffic between caches and DRAM.

Existing hardware prefetchers rely on monolithic prediction tables that are prone to entry conflicts across multiple streams. Notably, count-based confidence mechanism undervalues locally frequent but globally rare patterns, causing inability to react to shifting system conditions, which limit prefetchers effectiveness under dynamic, multi-phase access patterns.

## Design

Zion is a comprehensive, adaptive L2 hardware prefetcher built around Independent Temporal-Spatial Modules (ITSM) - five range-segmented prediction modules that isolate delta and stride tracking to eliminate cross-stream interference present in unified-table designs. Runtime feedback through confidence filtering, periodic effectiveness evaluation, and MSHR-aware insertion control enables Zion to dynamically regulate prefetch aggressiveness and placement under varying memory pressure.

![Overview of Zion](/images/2026Zion_Paper/Zion_ITSM_SysView.png)

**Core mechanisms:**

- **Independent Temporal-Spatial Modules (ITSM)**: Range-segmented delta and stride predictors that avoid inter-stream conflicts and capture both frequent and rare access patterns.
- **Runtime Adaptation**: Per-module confidence thresholds and periodic accuracy evaluation dynamically enable or disable prediction modules.
- **MSHR-Aware Control**: Prefetch insertion destination shifts based on real-time L2 memory availability.
- **Lightweight Design**: ~9KB total storage - 12.6x and 2.2x lower overhead than Bingo and Berti, respectively.

**Key results vs. IPCP, Bingo, SPP, Berti:**
- 4-core SPEC workloads: up to **43.2% speedup**
- Self-attention workloads: up to **43.0% speedup**
- LLC miss coverage on LLM attention (4-core): **90.5%**
- Heterogeneous 4-core mixes: **63.8% average improvement** over no prefetching


![Weighted speedup on 500 heterogeneous 4-core workload mixes](/images/2026Zion_Paper/Hetero_4Cores_Per_Pf_Speedup_zi.png)


*Weighted speedup of prefetchers on 500 heterogeneous SPEC and self-attention workload mixes in a 4-core system, sorted by Zion performance.*

<a href="/files/2026-04-DATE-Zion-HW-Prefetcher.pdf" style="
display:inline-block; 
padding:0.5rem 0.5rem; 
background:#8899BB; 
border-radius:32px; 
text-decoration:none; 
font-size:0.9rem; 
vertical-align:middle; 
margin-left:0.5rem;"><b>PDF</b></a>

