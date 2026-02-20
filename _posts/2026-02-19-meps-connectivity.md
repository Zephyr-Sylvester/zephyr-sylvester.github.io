---
layout: post
title: "Mapping how krill larvae get from spawning grounds to nurseries along the Antarctic Peninsula"
date: 2026-02-19
description: "A new paper in MEPS uses ocean modeling and particle tracking to show how bathymetry, embryo size, and wind variability shape larval krill connectivity."
tags: [antarctica, krill, larvae, connectivity, ocean-modeling, western-antarctic-peninsula]
categories: publications
related_posts: false
featured: true
---

Our paper **"Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula"** is out today in *Marine Ecology Progress Series*.

> Sylvester, Z.T., Dinniman, M.S., Thorpe, S.E., Bernard, K.S., Brooks, C.M. (2026). Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula. *Marine Ecology Progress Series*, 779, meps15059. [https://doi.org/10.3354/meps15059](https://doi.org/10.3354/meps15059)

Our goal was to model connectivity between spawning and nursery grounds of Antarctic krill and try to answer the question: **What areas are important for ontogenetic habitat partitioning in early life stages of krill and how does connectivity between regions influence broader population dynamics**

---

### Why connectivity matters

Antarctic krill are the foundation of the Southern Ocean food web, and their populations depend on successful recruitment, meaning larvae surviving long enough to join the adult population. But between spawning and recruitment lies a gauntlet: eggs sink, embryos develop through a descent–ascent cycle, and the resulting larvae are at the mercy of ocean currents for months.

The western Antarctic Peninsula (wAP) is one of the most important regions for krill globally, but we've had surprisingly little mechanistic understanding of how larvae move between spawning areas and the nursery grounds where they develop. Are nursery grounds self-sustaining, or do they depend on larval supply from elsewhere? How reliable are those supply pathways from year to year? And what happens when the winds change?

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/meps-reference-map.png" title="Reference Map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Nursery grounds: BS: Bransfield Strait; GS: Gerlache Strait; GP: Grandidier Passage; MB: Marguerite Bay (see Table S2 for coordinates). Geographic features are labeled (Mrg. Trough: Marguerite Trough).
</div>

---

### What we did

We used a circumpolar Southern Ocean ROMS (Regional Ocean Modeling System) configuration with a 5 km grid, 32 vertical layers, and ERA5 atmospheric forcing to simulate ocean circulation across the entire continental shelf, including under ice shelves, for three austral summers (2016–2019).

Within this model, we released Lagrangian drifters on a 25×25 km grid across the Southern Ocean to simulate larval krill transport. These aren't passive particles. They follow a vertical behavior model that represents the krill life cycle: eggs descend for roughly 5 days and are removed if they reach the seafloor before hatching. Survivors ascend through larval stages, and after about 60 days adopt a diel vertical migration pattern. Their movement is driven by ocean and sea ice velocities, with the balance depending on sea ice concentration and particle depth.

This biological detail is crucial. Where a larva sits in the water column determines which currents carry it, and that changes over the course of development.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/ascent-descent-withtext.png" title="Lagrangian drifter simulation design" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Lagrangian drifter simulation design: The Primary movement of particles is determined by ocean and sea ice velocities depending on sea ice concentrations and particle depth. Additional vertical behavior is determined by the life stage representing how krill larvae move through the water column. This detail is crucial for understanding how they interact with physical ocean properties and the habitat they reach during development.
</div>


---

### Key findings: Nursery by nursery

We focused on the wAP, identifying four known nursery grounds: Bransfield Strait, Gerlache Strait, Grandidier Passage, and Marguerite Bay. By tracking which simulated larvae spent more than 21 days in each nursery region during their first 6 months of life, we could trace back to where those larvae were spawned and map the connectivity between spawning and nursery habitat.

#### Bransfield Strait

The Bransfield Strait functions as both a spawning ground and a nursery ground. The vast majority of larvae that used BS as a nursery were spawned within it. Self-retention dominates. But the external supply pathways are what make this system interesting, because they shift dramatically from year to year depending on the winds.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/BS_migration_tracks_dual_panel_h_dvm_2016-2018_revised.png" title="Lagrangian drifter simulation design" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Larval krill trajectories for the Bransﬁeld Strait nursery ground (BS-NG) across 3 consecutive summers (2016–2019), showing particle trajectories (A) into BS-NG for larvae not spawned locally and (B) particles exiting from BS-NG. Pathways are colored by simulation start year: 2016 (blue), 2017 (magenta), and 2018 (gold). Background shading represents seaﬂoor bathymetry (IBCSO v.2)
</div>


The typical pattern is for larvae to be advected northeast along the continental shelf and into the Bransfield Strait. But local wind fields can enhance or completely redirect these inflows. In February 2017, strong northerlies near Boyd Strait created on-shelf Ekman transport that drew larvae in from a different direction entirely. In February 2019, weaker westerlies at the tip of the Peninsula facilitated transport from the Weddell Sea instead.

Same nursery ground, same model, same biology, but the wind field determined *which external larvae got there and where they came from*.

Larvae that left the Bransfield Strait were mainly advected north toward the South Scotia Ridge. But a subset was also carried south along the coastal current and into the two middle nursery grounds, the Gerlache Strait and Grandidier Passage. This makes BS not just a nursery in its own right, but a potential upstream source for nursery habitat further down the Peninsula.

#### Gerlache Strait and Grandidier Passage: secondary nurseries

The two middle nursery grounds acted as secondary nursery habitats, receiving larvae from both local spawning and from advection out of the Bransfield Strait. Their shallower bathymetry meant shorter retention times compared to the deeper basins at either end of the Peninsula.

#### Marguerite Bay: isolated and self-sustaining

Marguerite Bay stood out as fundamentally different from the northern nursery grounds. Like BS, it functions as both a spawning and nursery ground, with the majority of larvae that used MB as a nursery having been spawned within or near it. But unlike BS, Marguerite Bay's external supply came almost entirely from the south, via the Marguerite Trough, and it did not export larvae northward.

This isolation has real implications. The MB krill population is largely self-sustaining in terms of larval supply. It doesn't depend on transport from the north, but it also doesn't contribute larvae to the northern Peninsula nurseries. The two ends of the wAP, despite being part of the same continental shelf system, are functionally separated when it comes to early life stage connectivity.


---

### The connectivity picture

Pulling across all years and nursery grounds, a consistent picture emerged:

- **Bransfield Strait and Marguerite Bay** functioned as both spawning and nursery grounds, with strong self-retention. Most larvae that used these nurseries were spawned within them.
- **Off-shelf spawning** could contribute larvae to nursery grounds, but only when wind conditions permitted.
- **Coastal larval transport** generally moved north to south, with BS acting as a potential upstream source for the middle nursery grounds.
- **Marguerite Bay larvae remained isolated** from the northern Antarctic Peninsula. No northward export was observed.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/import-export-pathway-summary.png" title="Lagrangian drifter simulation design" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Primary trajectories of larvae (620 μm embryos) (A) into and (B) out of all nursery grounds
</div>

---

### What strengthening westerlies could mean

The wind-driven variability we simulated could be a preview of the kind of shifts that climate change is projected to amplify.

Westerly winds over the Southern Ocean are projected to strengthen and shift poleward through the end of the 21st century. Our results suggest this could have direct consequences for larval connectivity along the wAP. In the northern Antarctic Peninsula, seasonal winds modified larval transport pathways: when larvae weren't advected north, they were transported toward the southern end of the Peninsula instead. Enhanced westerlies could reduce the frequency of southerly wind-driven transport from the Weddell Sea into the Bransfield Strait, instead favoring stronger along-slope currents that bypass Boyd Strait entirely.

The connectivity pathways we observed, particularly the wind-sensitive ones supplying the Bransfield Strait, could be disrupted, with cascading implications for krill recruitment in the northern Peninsula.

---

### Where this goes next

This circumpolar model gave us the proof of concept: our model can simulate connectivity between spawning and nursery grounds within the bounds of observed patterns. But the 5 km resolution and 25×25 km drifter spacing leave fine-scale dynamics unresolved. The next step is to take these questions into a high-resolution regional model, resolving the mesoscale circulation, complex coastline interactions, and bathymetric details that matter for larval retention and exchange at the scale where nursery grounds actually function.

For more on the broader research program, see the [project page](/projects/krill-connectivity).

---


