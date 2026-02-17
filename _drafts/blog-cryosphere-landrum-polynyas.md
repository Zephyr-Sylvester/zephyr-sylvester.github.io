---
layout: post
title: "How do you define a polynya? It's more complicated than it sounds"
date: 2026-02-17
description: "A companion methods paper on identifying Antarctic coastal polynyas in satellite and model data — and why the choices you make matter enormously for the ecology."
tags: [antarctica, polynyas, remote-sensing, earth-system-models, methods]
categories: publications
related_posts: false
---

When we set out to build the [Antarctic Ecosystem Value Index](/projects/hotspots-in-the-ice), one of the first things we had to do was answer a question that sounds simple: **where are the polynyas?**

It turned out to be anything but simple. And that challenge — of identifying Antarctic coastal polynyas consistently across satellite observations and Earth System Model output — is the subject of a companion paper now in press in *The Cryosphere*:

> Landrum, L.L., DuVivier, A.K., Holland, M.M., Krumhardt, K., and Sylvester, Z. Defining Antarctic polynyas in satellite observations and climate model output to support ecological climate change research. *The Cryosphere* (in press). [https://doi.org/10.5194/egusphere-2024-3490](https://doi.org/10.5194/egusphere-2024-3490)

This is a methods paper at heart — but the methodological choices it addresses have direct consequences for the ecological conclusions you can draw. That's why it matters, and that's the lens I want to use to explain it here.

---

### Why Defining a Polynya Is a Real Problem

A polynya is, conceptually, a patch of open water surrounded by sea ice. But when you're working with gridded data — whether from satellites or climate models — translating that concept into a reproducible, quantitative definition involves a cascade of decisions:

- What **metric** do you use to identify open water? Sea ice concentration (how much of a grid cell is covered by ice) and sea ice thickness (how thick the ice is) don't always agree, especially in winter.
- What **threshold** do you apply? Is a grid cell with 15% sea ice concentration "open water"? 30%? The choice changes the size and location of every polynya you identify.
- What **grid type and resolution** are you working on? Satellite products and Earth System Models use different grids with different spatial resolutions — and regridding data between them can significantly change polynya statistics before you've made a single ecological interpretation.
- What **season** are you focused on? The optimal metric for identifying polynyas in winter months is different from spring, when the ice is actively breaking up and biological productivity is ramping up.

The paper works through each of these systematically, using both satellite observational products and the Community Earth System Model (CESM), to understand how these choices interact and what the consequences are.

---

### What They Found — and Why It Matters for Ecology

The results are both practically useful and genuinely sobering for anyone building ecosystem analyses on top of polynya data.

**Grid type and resolution matter — a lot.** When the same underlying data is regridded to a different spatial or temporal resolution, identified polynya statistics can change substantially. This means comparisons between studies using different data products are inherently fraught unless the grid issue is explicitly addressed.

**The right metric depends on context.** Sea ice thickness turns out to be more suitable for identifying polynyas in model data during winter months, while both thickness and concentration can work in spring. For satellite data, concentration is typically the only option — but the choice of concentration threshold still matters enormously.

**Models capture polynyas, but imperfectly.** The Earth System Model used in this study does produce coastal polynya-like features — they occupy roughly 3% of the winter sea ice zone area and contribute an estimated 17–21% of total sea ice zone marine net primary productivity. That disproportionate biological contribution is a key reason why getting the polynya definition right matters: a small area doing a lot of ecological work is exactly the kind of feature that's sensitive to methodological choices.

**Trends are not robust.** This is perhaps the most important finding for climate change research: trends in polynya areas are not consistent across different thresholds, grids, and observational products. They change in significance, magnitude, and even direction depending on the choices made. This doesn't mean change isn't happening — it means we need to be careful about the specific claims we make, and honest about the uncertainty in polynya trend detection.

---

### The Connection to the AEV Index

This paper is the physical foundation of the [AEV Index work](https://doi.org/10.1038/s41467-026-69011-0). Before we could say that polynyas have Index values 31–72% higher than surrounding areas, we had to have a defensible, internally consistent method for identifying those polynyas in both the observational and model data we were using.

The Landrum et al. analysis gave us that foundation — and more importantly, it gave us a clear-eyed understanding of where the uncertainty lies. When the AEV Index projects future ecosystem value using Earth System Model output, the polynya identification underpinning those projections is grounded in this methodological work.

Science is often presented as a linear march from question to answer. In practice, a project like this one requires building the methodological scaffolding at the same time as the science it supports. This paper is part of that scaffolding — and it's rigorous, careful work that deserves to be read on its own terms, not just as a footnote to the Index.

---

### For Researchers Working with Polynya Data

If you're building analyses that depend on polynya identification — whether for ecology, physical oceanography, or climate modeling — the practical takeaways from this paper are:

- Always identify polynyas on grids of the same type and resolution when comparing across data products
- Be explicit about your metric and threshold choices, and test sensitivity where possible
- Be cautious about trend claims; they are particularly sensitive to these choices
- If comparing satellite observations with model output, the mismatch in grid type is a first-order issue, not a footnote

The paper provides comprehensive, quantifiable guidance on polynya identification that is directly applicable to future work on Antarctic marine ecosystem dynamics.

---

*Both papers are products of a NASA Applied Sciences project (Grant 80NSSC21K1132) focused on improving ecological forecasting for Antarctic marine ecosystems. For the full project context, see the [Hot Spots in the Ice project page](/projects/hotspots-in-the-ice).*
