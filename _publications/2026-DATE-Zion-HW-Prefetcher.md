---
title: "Zion: A Comprehensive, Adaptive, and Lightweight Hardware Prefetcher"
collection: publications
category: conferences
permalink: /publication/2026-zion-date
date: 2026-04-01
paperurl: '/files/2026-04-DATE-Zion-HW-Prefetcher.pdf'
# citation: 'Biryukov, V., Lu, X., Liu, Z., Zhou, K., & Sun, X.-H. (2026). &quot;Zion: A Comprehensive, Adaptive, and Lightweight Hardware Prefetcher.&quot; <i>Design, Automation and Test in Europe Conference (DATE 2026)</i>.'
excerpt: '<b>Vadim Biryukov</b>, Xiaoyang Lu, Zirui Liu, Kaixiong Zhou, Xian-He Sun'
venue: 'Design, Automation and Test in Europe Conference, <b>DATE 2026</b>'
---
<b>Vadim Biryukov</b>, Xiaoyang Lu, Zirui Liu, Kaixiong Zhou, Xian-He Sun

Zion is a comprehensive, adaptive L2 hardware prefetcher built around **Independent Temporal-Spatial Modules (ITSM)** — segmented delta and stride predictors that reduce inter-stream conflicts and improve coverage across diverse memory access patterns.

**Core mechanisms:**
- **ITSM**: Independent temporal and spatial prediction modules eliminate unified-table conflicts that degrade existing prefetchers under mixed workloads
- **Runtime adaptation**: Confidence-based filtering + periodic accuracy monitoring dynamically regulate prefetch aggressiveness
- **MSHR-aware control**: Adjusts prefetch insertion behavior based on L2 resource availability under memory pressure
- **Hardware cost**: ~9KB storage; integrates at L2 cache level

**Key results vs. IPCP, Bingo, SPP, Berti:**
- 4-core SPEC workloads: up to **43.2% speedup**
- Self-attention workloads: up to **43.0% speedup**
- LLC miss coverage on LLM attention (4-core): **90.5%**
- Heterogeneous 4-core mixes: **63.8% average improvement** over no prefetching

<a href="/files/2026-04-DATE-Zion-HW-Prefetcher.pdf" style="display:inline-block; padding:0.4rem 0.9rem; background:#Ad8eAd; color:white; border-radius:6px; text-decoration:none; font-size:0.9rem; vertical-align:middle; margin-left:0.5rem;"><b>PDF</b></a>

