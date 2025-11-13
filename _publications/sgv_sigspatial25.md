---
title: "SGV: Spatial Graph Visualization"
collection: publications
category: conferences
permalink: /publication/2025-sgv
excerpt: "."
date: 2025-11-01
venue: "ACM SIGSPATIAL 2025 — Minneapolis, MN"
paperurl: "/files/sgv_sigspatial25.pdf"
# Optional extras (uncomment if available)
# slidesurl: "/files/lasek_demo_slides.pdf"
# posterurl: "/files/lasek_poster.pdf"
code: "https://github.com/tarlaun/fdgv"
---

**LASEK** is a system for **interactive exploration and styling of large geospatial datasets**.  
Users can **upload their own data**, get **LLM-generated style suggestions** (e.g., graduated ramps, categorical palettes, bivariate overlays), and **see results instantly** on a modern web map backed by **Mapbox Vector Tiles**.

### Why LASEK
Current tools make it hard to (i) iterate quickly on styles, (ii) keep maps responsive at scale, and (iii) share reproducible styling choices. LASEK addresses these gaps by coupling **LLM-assisted style generation** with a **scalable data-to-tiles pipeline** and a **lightweight web UI** for rapid “try–tweak–compare” workflows.

### Key Capabilities
- **LLM-guided styling**: natural-language prompts propose styles (e.g., “graduated color ramp on `population`,” “categorize by `continent`,” “highlight top 10% by `GDP`”).
- **Real-time iteration**: instant map updates, side-by-side comparisons, and saved presets.
- **Scale & performance**: Spark/Scala backend for preprocessing; efficient rendering at interactive zoom levels.
- **Reproducibility**: exportable style specs and dataset summaries for consistent sharing.

**Artifacts:**  
  - 📄 Paper: [/files/sgv_sigspatial25.pdf](/files/lasek_vldb25_demo.pdf)  
  - 🎥 Demo video: [Watch on Google Drive](https://drive.google.com/file/d/1PIyMbhM68kW05BCr5bXcANrpjmxO2FN_/view?usp=sharing)  
  - 💻 Code: [github.com/tarlaun/LASEK](https://github.com/tarlaun/FDGV)

