---
title: "ChampSim Memory and Performance Optimization"
excerpt: "Redesigned core simulation code architecture of <a href=\"https://github.com/ChampSim/ChampSim\">ChampSim</a>. While maintaining program equivalency, <strong>reduced simulation time </strong>up to <strong>90%</strong> in multi-core configurations and <strong>increased simulation concurrency</strong> by <strong>30-40%</strong>."
technologies: "C++, Multi-threading, Memory Architecture, XZ Compression"
tags: ["research", "systems"]
---

Redesigned core simulation code architecture of <a href="https://github.com/ChampSim/ChampSim">ChampSim</a>. While maintaining program equivalency, <strong>reduced simulation time </strong>up to <strong>90%</strong> in multi-core configurations and <strong>increased simulation concurrency</strong> by <strong>30-40%</strong>.

<strong>Utilized Techniques:</strong> Algorithm redesign <i>(improved complexities)</i>, Data layout optimization <i>(better cache locality)</i>, Object orchestration <i>(reduced memory operations)</i>, XZ overhead reduction <i>(decreased OS context-switching)</i>.
