---
title: "Starlet: An End-to-End Python Library for Scalable Geospatial Tiling and Vector-Tile Serving"
collection: publications
category: conferences
permalink: /publication/2026-starlet
excerpt: "A pip-installable Python library that takes GeoParquet and GeoJSON all the way to low-latency web map tiles—spatial partitioning, density-driven MVT generation, and a caching tile server in one workflow."
date: 2026-11-03
venue: "ACM SIGSPATIAL 2026 — Short Paper, Riverside, CA (to appear)"
authors: "**Tarlan Bahadori**, Rohan Bennur, Shaolin Xie, Ibrahim Sabek, Ahmed Eldawy"
paperurl: "/files/starlet_sigspatial26_short.pdf"
code: "https://github.com/ucr-bdlab/starlet"
---

**Authors:** **Tarlan Bahadori**, Rohan Bennur, Shaolin Xie, Ibrahim Sabek, Ahmed Eldawy

*Accepted at ACM SIGSPATIAL 2026 (Riverside, CA, Nov 3–6) — Short Paper.*

**Starlet** is a **pip-installable Python library for end-to-end geospatial tiling and vector-tile serving over GeoParquet**. It ingests GeoParquet or GeoJSON, partitions the data into balanced spatial shards, builds a Web Mercator density grid for fast tile-occupancy tests, and generates Mapbox Vector Tiles either **eagerly** into an on-disk pyramid or **lazily** on first request.

### Why Starlet
Web-scale geospatial visualization normally takes three stages—transform to a tile-friendly layout, construct or select a pyramid, and serve tiles to a renderer—and existing systems address these separately. Few offer an end-to-end path that is **native to modern columnar spatial data** and easy to embed in a Python workflow. Starlet packages ingestion, tile generation, serving, and prompt-based styling into a single library that runs on one machine.

### Key Capabilities
- **R\*-Grove-inspired partitioning** with a round-buffered streaming writer that bounds open files and per-round memory during ingestion
- **4096×4096 prefix-sum density grid** answering rectangular range counts in *O(1)*, so empty and low-density tiles are pruned before geometry decoding
- **Eager or lazy MVT generation**, with a serving layer combining memory caching, disk-backed tiles, and on-demand generation
- **PMTiles export** cutting on-disk storage by **47–64%** versus loose `.mvt` files
- **LLM-assisted style reuse and prompt sharing** over a repository of annotated visualization templates

### Evaluation Highlights
- Partitions and indexes a **17.6 GB OpenStreetMap extract** — 43M features, **one billion vertices** — in **38.5 minutes**, peak RSS below **9.6 GB**, on commodity laptop hardware
- Cached tile serving stays interactive under load: median latency **4.7 ms** at 20 concurrent clients, p95 below **5 ms**
- Runtime grows linearly with feature count (397 s → 6,397 s as input grows 17×), while peak memory grows sub-linearly

**Artifacts:**
- 📄 Paper: [/files/starlet_sigspatial26_short.pdf](/files/starlet_sigspatial26_short.pdf)
- 📦 Package: [pypi.org/project/starlet](https://pypi.org/project/starlet/) — `pip install starlet`
- 💻 Code: [github.com/ucr-bdlab/starlet](https://github.com/ucr-bdlab/starlet)
