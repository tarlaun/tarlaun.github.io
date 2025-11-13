---
title: "SGV: Spatial Graph Visualization"
collection: publications
category: conferences
permalink: /publication/2025-sgv
excerpt: "A scalable force-directed framework that integrates geographic anchoring to produce clearer, more spatially faithful graph layouts."
date: 2025-11-01
venue: "ACM SIGSPATIAL 2025 — Minneapolis, MN"
authors: "**Tarlan Bahadori**, Alvin Chiu, Ahmed Eldawy, Michael Goodrich"
paperurl: "/files/sgv_sigspatial25.pdf"
code: "https://github.com/tarlaun/fdgv"
videourl: "https://drive.google.com/your_sgv_video"   # update link
posterurl: "/files/sgv_poster.pdf"
---

**Authors:** **Tarlan Bahadori**, Alvin Chiu, Ahmed Eldawy, Michael Goodrich

**SGV** is a **scalable spatial graph visualization framework** that retains the **geographic meaning** of networks while producing clean, uncluttered layouts. It integrates classical force-directed forces with **novel spatial anchoring**—a gravity-based pull toward real-world regions or points—yielding layouts that respect both topology and geography.

### Why SGV
Traditional force-directed layouts disregard spatial context, while purely geographic maps ignore graph structure. SGV introduces a **unified anchored force model** that preserves both, reducing clutter and improving readability in large, dense networks. The system is implemented on **Apache Spark**, enabling layouts at massive scale.

### Key Capabilities
- **Anchored force model** combining attraction, repulsion, and spatial gravity  
- **Region- and point-based anchors** for flexible geographic constraints  
- **Scalable Spark implementation** for graphs with millions of vertices  
- **Improved readability** (shorter anchor distances, fewer crossings, lower HEL)  

**Artifacts:**  
- 📄 Paper: [/files/sgv_sigspatial25.pdf](/files/sgv_sigspatial25.pdf)  
- 🎥 Demo Video: [Watch on Google Drive](https://drive.google.com/file/d/13wklH3JzeOoYPIG67z549QgNLxTgwX-h/view?usp=share_link) 
- 💻 Code: [github.com/tarlaun/FDGV](https://github.com/tarlaun/FDGV)
- 🧾 Poster: [/files/sgv_poster.pdf](/files/sgv_poster.pdf)

