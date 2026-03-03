---
title: "ChampSim Memory and Performance Optimization"
excerpt: "Redesigned core simulation architecture of ChampSim. Reduced simulation time up to <b>90%</b> in multi-core configurations and increased simulation concurrency by <b>30-40%</b> through algorithm complexity reduction, data layout optimization for cache locality, object lifecycle management to minimize memory operations, and XZ decompression overhead reduction via OS context-switch mitigation. <br><strong>Utilized Techniques:</strong> Algorithm redesign <i>(improved complexities)</i>, Data layout optimization <i>(better cache locality)</i>, Object orchestration <i>(reduced memory operations)</i>, XZ overhead reduction <i>(decreased OS context-switching)</i>."
technologies: "C++, Multi-threading, Memory Architecture, XZ Compression"
tags: ["research", "systems"]
---


