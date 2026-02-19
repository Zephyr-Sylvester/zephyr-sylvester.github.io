---
layout: post
title: "Mapping how krill larvae get from spawning grounds to nurseries along the Antarctic Peninsula"
date: 2026-02-19
description: "A new paper in MEPS uses ocean modeling and particle tracking to show how wind variability and bathymetry shape larval krill connectivity — and what strengthening westerlies could mean for the future."
tags: [antarctica, krill, larvae, connectivity, ocean-modeling, western-antarctic-peninsula]
categories: publications
related_posts: false
featured: true
---

Our paper **"Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula"** is out today in *Marine Ecology Progress Series*.

> Sylvester, Z.T., Dinniman, M.S., Thorpe, S.E., Bernard, K.S., Brooks, C.M. (2026). Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula. *Marine Ecology Progress Series*, 779, meps15059. [https://doi.org/10.3354/meps15059](https://doi.org/10.3354/meps15059)

This paper asks a question that sounds simple but turns out to be surprisingly hard to answer: **where do krill larvae need to be spawned in order to reach known nursery grounds, and how reliable are those pathways from year to year?**

---

### Why connectivity matters

Antarctic krill are the foundation of the Southern Ocean food web, and their populations depend on successful recruitment — larvae surviving long enough to join the adult population. But between spawning and recruitment lies a gauntlet: eggs sink, embryos develop through a descent–ascent cycle, and the resulting larvae are at the mercy of ocean currents for months.

The western Antarctic Peninsula (wAP) is one of the most important regions for krill globally, but we've had surprisingly little mechanistic understanding of how larvae move between spawning areas and the nursery grounds where they develop. Are nursery grounds self-sustaining, or do they depend on larval supply from elsewhere? How reliable are those supply pathways from year to year? And what happens when the winds change?

<!-- FIGURE: Reference map showing the four nursery grounds (BS, GS, GP, MB) along the wAP -->

---

### What we did

We used a circumpolar Southern Ocean ROMS (Regional Ocean Modeling System) configuration — 5 km grid, 32 vertical layers, ERA5 atmospheric forcing — to simulate ocean circulation across the entire continental shelf, including under ice shelves, for three austral summers (2016–2019).

Within this model, we released Lagrangian drifters on a 25×25 km grid across the Southern Ocean to simulate larval krill transport. These aren't passive particles — they follow a vertical behavior model that represents the krill life cycle: eggs descend for roughly 5 days and are removed if they reach the seafloor before hatching. Survivors ascend through larval stages, and after about 60 days adopt a diel vertical migration pattern. Their movement is driven by ocean and sea ice velocities, with the balance depending on sea ice concentration and particle depth.

This biological detail is crucial. Where a larva sits in the water column determines which currents carry it — and that changes over the course of development.

<!-- FIGURE: Schematic of the vertical behavior model — descent, ascent, DVM transition -->

We focused on the wAP as the most well-studied krill region, identifying four known nursery grounds — Bransfield Strait, Gerlache Strait, Grandidier Passage, and Marguerite Bay — and asked: where would larvae need to be spawned to end up in each of these nurseries?

---

### Key findings

#### Winds reshape connectivity year to year

The most striking result was how much interannual wind variability altered the pathways larvae take to reach nursery grounds. The Bransfield Strait is the clearest example.

The typical pattern is for larvae to be advected northeast along the continental shelf and into the Bransfield Strait. But local wind fields can enhance or completely redirect these inflows. In February 2017, strong northerlies near Boyd Strait created on-shelf Ekman transport that drew larvae in from a different direction. In February 2019, weaker westerlies at the tip of the Peninsula facilitated transport from the Weddell Sea instead.

Same nursery ground, same model, same biology — but the wind field determined *which larvae got there and where they came from*.

<!-- FIGURE: Spawning locations for BS nursery across years, showing interannual variability -->

<!-- FIGURE: Wind patterns for the contrasting BS connectivity years -->

#### Marguerite Bay is isolated

Marguerite Bay stood out as fundamentally different from the northern nursery grounds. It received larvae mainly from the south, via the Marguerite Trough, and did not export larvae northward. Krill spawned in or near Marguerite Bay stayed in the Marguerite Bay system.

This isolation has real implications. It means that the MB krill population is largely self-sustaining in terms of larval supply — it doesn't depend on transport from the north, but it also doesn't contribute larvae to the northern Peninsula nurseries. The two ends of the wAP, despite being part of the same continental shelf system, are functionally separated when it comes to early life stage connectivity.

<!-- FIGURE: MB spawning locations and/or transport pathways showing isolation -->

#### The general connectivity picture

Pulling across all years and nursery grounds, a consistent picture emerged: Bransfield Strait and Marguerite Bay functioned as both spawning and nursery grounds with substantial self-retention. Off-shelf spawning could contribute larvae to nursery grounds, but only when wind conditions permitted. Coastal larval transport generally moved north to south. And Marguerite Bay larvae remained isolated from the northern Antarctic Peninsula.

<!-- FIGURE: Summary connectivity schematic or matrix -->

---

### What strengthening westerlies could mean

This is where the results connect to the future. The wind-driven variability we documented isn't just historical noise — it's a preview of the kind of shifts that climate change is projected to amplify.

Westerly winds over the Southern Ocean are projected to strengthen and shift poleward through the end of the 21st century. Our results suggest this could have direct consequences for larval connectivity along the wAP. Enhanced westerlies could reduce the frequency of southerly wind-driven transport from the Weddell Sea into the Bransfield Strait, instead favoring stronger along-slope currents that bypass the strait entirely. The connectivity pathways we observed — particularly the wind-sensitive ones — could be disrupted, with cascading implications for krill recruitment in the northern Peninsula.

The wAP is already one of the fastest-warming regions on Earth. Understanding how the physical pathways that sustain krill nursery grounds will respond to changing winds is directly relevant to spatial management and MPA design — and it's the question that motivates the next phase of this research.

---

### Where this goes next

This circumpolar model gave us the proof of concept: connectivity between spawning and nursery grounds is real, structured, and sensitive to wind variability. But the 5 km resolution and 25×25 km drifter spacing leave a lot of fine-scale dynamics unresolved. The next step is to take these questions into a high-resolution regional model — resolving the mesoscale circulation features, complex coastline interactions, and bathymetric details that matter for larval retention and exchange at the scale where nursery grounds actually function.

For more on the broader research program, see the [project page](/projects/krill-larval-connectivity).

---

*This paper was produced as part of my dissertation research.*
