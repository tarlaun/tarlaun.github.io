---
title: "CATALYST: CATalogue-driven LLM sYstem for Spatial Tiling"
collection: publications
category: conferences
permalink: /publication/2026-catalyst
excerpt: "A catalogue-driven, LLM-assisted system for interactive exploration of large geospatial repositories—semantic dataset search, bounded enriched-schema summaries, tile-based visualization, and generated map styles."
date: 2026-11-03
venue: "ACM SIGSPATIAL 2026 — Demo Track, Riverside, CA (to appear)"
authors: "**Tarlan Bahadori**, Ahmed Eldawy"
paperurl: "/files/catalyst_sigspatial26_demo.pdf"
code: "https://github.com/tarlaun/catalyst"
videourl: "https://drive.google.com/file/d/1NKF4xRW0QPrZaa-K_Prjb99AAaliyKBk/view?usp=sharing"
---

**Authors:** **Tarlan Bahadori**, Ahmed Eldawy

*Accepted at ACM SIGSPATIAL 2026 (Riverside, CA, Nov 3–6) — Demo Track.*

**CATALYST** is a **catalogue-driven, LLM-assisted system for interactive exploration of large geospatial repositories**. Given a natural-language prompt, it retrieves relevant datasets through **semantic search**, derives missing information through **joins or overlays** when needed, summarizes datasets with **bounded enriched-schema aggregates**, visualizes the resulting layers using a **tile-based index**, and generates cartographically meaningful styles through **declarative styling** or optional **sandboxed code generation**.

### Why CATALYST
Geospatial data is a large and growing fraction of public open data—Data.gov alone hosts nearly 300,000 geospatial datasets—yet it remains hard to discover, combine, visualize, and style at scale. Metadata is often incomplete or missing, datasets reach hundreds of gigabytes, and many questions require combining several layers rather than styling a single one. CATALYST addresses all three with a **search-then-reason** design: only compact enriched-schema summaries reach the LLM, so the payload stays bounded by **schema width rather than dataset size**.

### Key Capabilities
- **Semantic dataset discovery** over an enriched catalogue of attribute names, inferred types, and statistical summaries, embedded in a vector DBMS
- **Tile histogram index + multi-resolution pyramid** that precomputes dense tiles and generates sparse tiles on demand, enabling client-side MVT rendering
- **Multi-dataset queries with tile-aligned joins** — overlays, attribute joins, and spatial joins (`intersects`, `within`, `nearest`) without global re-partitioning
- **Declarative and executable styling**, with generated code running in a sandboxed cross-origin iframe behind user approval
- **Conversational refinement** — follow-up prompts like *"use a red palette"* or *"apply a log scale"* reuse session state

### Evaluation Highlights
- Near-linear preprocessing from **2.5M → 42.8M features** (118.7M → 1.16B vertices), at **18–20K rows/s** throughout
- Peak memory around **3 GB** through the 10M-feature scale, rising to **7.51 GB** at the largest input
- Tile-aligned joins finished a cross-dataset aggregation in **58.7 s** vs **2,417.6 s** for the full derive path — identical 3,879,476 output rows

**Artifacts:**
- 📄 Paper: [/files/catalyst_sigspatial26_demo.pdf](/files/catalyst_sigspatial26_demo.pdf)
- 🎥 Demo Video: [Watch on Google Drive](https://drive.google.com/file/d/1NKF4xRW0QPrZaa-K_Prjb99AAaliyKBk/view?usp=sharing)
- 💻 Code: [github.com/tarlaun/catalyst](https://github.com/tarlaun/catalyst)
- 🌐 Live Demo: [starmap.cs.ucr.edu/catalyst](https://starmap.cs.ucr.edu/catalyst)
