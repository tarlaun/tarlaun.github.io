---
title: "Circle Quasi-Cartograms for Scalable Spatial Aggregation"
collection: publications
category: conferences
permalink: /publication/2025-cqc
excerpt: "A fast and scalable technique for generating circle-based quasi-cartograms that preserve topology while supporting large geospatial datasets."
date: 2025-11-01
venue: "ACM SIGSPATIAL 2025 — Minneapolis, MN"
paperurl: "/files/circle_quasi_cartograms_sigspatial25.pdf"
code: "https://github.com/tarlaun/circle-quasicartograms"
videourl: "https://drive.google.com/your_cqc_video"   # update link
---

**Authors:** **Tarlan Bahadori**, Alvin Chiu, Ahmed Eldawy, Michael Goodrich

**Circle Quasi-Cartograms** introduce a **lightweight, scalable alternative** to classical cartograms. Instead of deforming polygonal regions, our method assigns each region a circle with area proportional to its attribute of interest while preserving **adjacency** and **relative spatial layout**. The technique is designed for large geospatial datasets where traditional cartogram algorithms are too slow or produce excessive distortion.

### Why Circle Quasi-Cartograms
Full cartogram generation is often computationally expensive and difficult to interpret. Our circle-based approach offers a **clearer, more stable representation** that highlights attribute magnitudes while maintaining geographic intuition. The method easily integrates into modern vector-tile pipelines and supports **interactive visualization at scale**.

### Key Capabilities
- **Topology-preserving circle arrangement** retaining neighborhood relations  
- **Area-proportional encoding** for intuitive comparisons  
- **Fast convergence** suitable for large datasets and web-mapping workflows  
- **Compatible with MVT pipelines** and tiled rendering systems  

**Artifacts:**  
- 📄 Paper: [/files/circle_quasi_cartograms_sigspatial25.pdf](/files/circle_quasi_cartograms_sigspatial25.pdf)
