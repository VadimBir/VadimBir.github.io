---
title: "Automated IOT-based performance assessments through activity recognition and semantic evaluation in Smart Learning Environments"
collection: publications
category: conferences
permalink: /publication/2024-02-17-iccad-paper
paperurl: "/files/2024-02-ICCAD-Smart_Learning_Environments.pdf"
excerpt: 'Gina Martinez, Jason Perry, <b>Vadim Biryukov</b>'
date: 2024-02-17
venue: 'International Conference on Control, Automation and Diagnosis <b>ICCAD 2024</b>'
---
Authors: Gina Martinez, Jason Perry, <b>Vadim Biryukov</b>

## Background

Engineering accreditation bodies (ABET) require assessment of socio-technical skills — ethics, safety awareness, teamwork — yet these behaviors are difficult to observe consistently and their manual evaluation suffers from subjectivity. Existing automated approaches target purely technical competencies or single scenarios, and none employ semantic reasoning, limiting extendibility and adaptability across assessment contexts.

## Design

SLEAAF (Smart Learning Environment Ambient Assessment Framework), deployed in an undergraduate circuits laboratory. The system fuses sensor-based and video-based activity recognition with a semantic evaluation layer. A Raspberry Pi interfaces with an antistatic continuous monitor (CM420), a current sensor (INA 219) for detecting live circuit modifications, and a Keysight 34461A auto-logging multimeter. A front-facing camera with CompreFace facial recognition localizes actors and associates detected events with specific students through temporal-spatial alignment. Recognized activities populate a Class Activity Ontology, and SPARQL queries reason over the data to evaluate six performance indicators spanning ethics, safety, and teamwork.

![System Architecture](/images/2024-SLEAAF.png)

**Core contributions:**
- **SLEAAF architecture**: Perception layer (sensors and video), data aggregation with actor association, and semantic query layer for automated assessment.
- **Class Activity Ontology**: Domain ontology modeling laboratory events, actors, timestamps, and spatial relationships — first of its kind for performance assessment in smart learning environments.
- **Six performance indicators**: Data fabrication detection (PI1), power-off-before-circuit-change (PI2), proactive wrist band (PI3) and mat usage (PI4), end-of-session power-off (PI5), and group contribution balance (PI6).

**Key results:**
- **100% hit rate** on 9 of 11 activity types; **96% hit rate** on circuit change detection.
- **88% accuracy** in associating detected events with correct actors via facial recognition.
- All safety and ethics violations (PI3–PI5) detected with **100% accuracy** across five experiments.
- System identifies assessment violations an instructor observing ~10% of class time would miss.

<a href="/files/2024-02-ICCAD-Smart_Learning_Environments.pdf" style="display:inline-block; padding:0.4rem 0.9rem; background:#Ad8eAd; color:white; border-radius:6px; text-decoration:none; font-size:0.9rem; vertical-align:middle; margin-left:0.5rem;"><b>PDF</b></a>