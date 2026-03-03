---
title: "Zion: Comprehensive, Adaptive, and Lightweight Hardware Prefetcher"
excerpt: "Designed and implemented Zion - a <strong>novel L2 hardware prefetcher</strong> built around <strong>Independent Temporal-Spatial Modules (ITSM)</strong>. Segmented delta and stride predictors eliminate inter-stream conflicts that degrade unified-table prefetchers under mixed workloads. <strong>Runtime feedback mechanisms</strong> - confidence-based filtering, periodic accuracy monitoring, and MSHR-aware control - dynamically regulate prefetch aggressiveness and insertion behavior under memory pressure. <strong>Hardware cost</strong>: ~9KB storage at L2 cache level."
technologies: "C++, ChampSim, Memory Architecture, Hardware Design"
tags: ["research", "published"]
venue: "Design, Automation and Test in Europe (DATE 2026)"
---

Designed and implemented Zion - a <strong>novel L2 hardware prefetcher</strong> built around <strong>Independent Temporal-Spatial Modules (ITSM)</strong>. Segmented delta and stride predictors eliminate inter-stream conflicts that degrade unified-table prefetchers under mixed workloads. <strong>Runtime feedback mechanisms</strong> - confidence-based filtering, periodic accuracy monitoring, and MSHR-aware control - dynamically regulate prefetch aggressiveness and insertion behavior under memory pressure. <strong>Hardware cost</strong>: ~9KB storage at L2 cache level.

Published: Design, Automation and Test in Europe (DATE 2026)
