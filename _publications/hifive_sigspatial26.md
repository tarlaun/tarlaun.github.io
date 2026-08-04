---
title: "HiFIVE: High-Fidelity Vector-Tile Reduction for Interactive Map Exploration"
collection: publications
category: conferences
permalink: /publication/2026-hifive
excerpt: "A data-management framework for scalable, high-fidelity client-side geospatial visualization that formalizes visualization-aware tile reduction and prunes tiles via triage and sparsification."
date: 2026-11-01
venue: "ACM SIGSPATIAL 2026 — Riverside, CA (to appear)"
authors: "**Tarlan Bahadori**, Ahmed Eldawy"
paperurl: "https://arxiv.org/abs/2603.10270"
---

**Authors:** **Tarlan Bahadori**, Ahmed Eldawy

*Accepted at ACM SIGSPATIAL 2026 (Riverside, CA) — camera-ready version forthcoming. A preprint is available on arXiv.*

**HiFIVE** is a **data-management framework for scalable, high-fidelity client-side geospatial visualization**. It formalizes the **visualization-aware tile reduction problem**—the trade-off between tile size and visualization distortion—proves it **NP-hard**, and introduces a practical two-stage solution that keeps interactive maps responsive at terabyte scale.

### Why HiFIVE
Many tools for large spatial data fall back on **server-side rendering**, shipping small images to the client. Users, however, prefer **client-side rendering**, which allows quick restyling of the data for a better exploration experience—but that requires sending the data itself, and full-fidelity vector tiles are far too large. HiFIVE closes this gap by reducing tiles in a way that is aware of how they will ultimately be drawn.

### Key Capabilities
- **Formal problem definition** of visualization-aware tile reduction, with an **NP-hardness proof**
- **Two-stage reduction**: *triage* followed by *sparsification*
- **Selective pruning of records, attributes, and values** using information-theoretic and spatial criteria
- **Substantial tile-size reductions** while preserving visual fidelity and interactive performance at **terabyte scale**

**Artifacts:**
- 📄 Preprint: [arxiv.org/abs/2603.10270](https://arxiv.org/abs/2603.10270)
