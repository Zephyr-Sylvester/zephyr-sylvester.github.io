---
layout: page
title: Krill Larval Connectivity
description: Modeling how ocean currents, biology, and sea ice shape the early life of Antarctic krill
img: assets/img/projects/connectivity/PLACEHOLDER-hero-image.jpg
importance: 1
category: research
related_publications: true
tabs: true
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/PLACEHOLDER-hero-image.jpg" title="Western Antarctic Peninsula" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <!-- CAPTION: Replace with appropriate image of the wAP study region, larval krill, or ROMS model domain -->
</div>

## Where do krill larvae go?
#### Using ocean models and particle tracking to understand connectivity along the Western Antarctic Peninsula

Antarctic krill (*Euphausia superba*) underpin the Southern Ocean food web. But before a krill can join the population, it has to survive one of the most precarious journeys in the ocean: sinking as an embryo toward the deep seafloor, hatching, swimming back to the surface, and then drifting for months through some of the most dynamic waters on Earth.

This research program uses ocean modeling and Lagrangian particle tracking to understand how physical oceanography and larval biology interact to shape connectivity in early life stages.

The goal is to build a mechanistic understanding of *how larvae get from where they're spawned to where they grow up*. I want to know how that process changes across years, under different biological assumptions, and as the ocean and sea ice evolve under climate change.

---

## Pick your interest

{% tabs connectivity_project %}

{% tab connectivity_project The Science %}

### How ocean physics and larval biology shape krill connectivity

Krill eggs don't just float. After spawning, embryos sink — sometimes hundreds of meters — before hatching into larvae that swim back toward the surface. This descent–ascent cycle means that the depth of the water column, the speed of the currents at different depths, and the size of the embryo all interact to determine where a larva ends up when it reaches the surface and begins its months-long drift.

<!-- FIGURE: Schematic of the descent-ascent cycle -->

We use the **Regional Ocean Modeling System (ROMS)** at high resolution (~1.5 km) to simulate ocean circulation along the wAP, coupled with offline Lagrangian particle tracking to follow hundreds of thousands of virtual larvae through their early development.

#### What we've found so far

Our first paper from this work ([Sylvester et al. 2026, MEPS](https://doi.org/10.3354/meps15059)) simulated larval transport over three austral summers (2016–2019) and revealed several key dynamics:

**Bathymetry controls nursery function.** Deeper regions like Bransfield Strait and Marguerite Bay retain larvae for long periods (>50 days), functioning as primary nursery habitat. Shallower areas like the Gerlache Strait and Grandidier Passage serve as secondary nurseries — important, but more dependent on conditions.

<!-- FIGURE: Map of the four nursery regions (BS, GERL, GP, MB) with bathymetry -->

**Embryo size reshapes connectivity.** Larger embryos hatch at shallower depths, which means they enter different current regimes and connect to nursery grounds more reliably. This biological parameter — which varies with maternal condition — has outsized effects on the physical connectivity picture.

**Wind drives interannual variability.** The pathways between spawning areas and nursery grounds are relatively stable in structure, but their strength shifts year to year with the wind field. This means connectivity is somewhat predictable in its geography but variable in its magnitude.

**Biology and physics are inseparable.** Passive particle simulations miss the descent–ascent dynamics that fundamentally shape where larvae end up. Getting the biology right isn't a refinement — it changes the answer.

<!-- FIGURE: Connectivity matrix or transport pathway visualization -->

| Region | Abbreviation | Depth Character | Nursery Role |
|---|---|---|---|
| Bransfield Strait | BS | Deep basin | Primary — high retention |
| Gerlache Strait | GERL | Moderate | Secondary — condition-dependent |
| Grandidier Passage | GP | Moderate–shallow | Secondary — condition-dependent |
| Marguerite Bay | MB | Deep embayment | Primary — high retention |

{% endtab %}

{% tab connectivity_project The Modeling %}

### Technical approach: ROMS + Lagrangian particle tracking

This work builds on an existing high-resolution ROMS configuration for the western Antarctic Peninsula, developed by Mike Dinniman and colleagues. The model resolves mesoscale and some submesoscale circulation features critical for larval transport in this complex coastal environment.

#### Model configuration

- **Model:** Regional Ocean Modeling System (ROMS)
- **Domain:** Western Antarctic Peninsula coastal region
- **Resolution:** ~1.5 km horizontal grid spacing
- **Forcing:** Atmospheric (ERA5), oceanic boundary conditions, tidal forcing
- **Existing runs:** 2006–2012, 2016–2019, 2020
- **Particle tracking:** Offline Lagrangian tracking with biological behavior (descent–ascent cycle, stage-dependent vertical migration)

#### What makes this approach different

Most larval dispersal studies treat particles as passive tracers. Our simulations incorporate the **descent–ascent developmental cycle** — embryos sink at empirically derived rates, hatch at depth, and larvae swim upward at stage-appropriate speeds. This means particles interact with different current regimes at different depths during their early life, producing fundamentally different connectivity patterns than passive simulations would predict.

We also vary **initial embryo size**, which controls sinking rate and therefore hatching depth. This parameterization captures real biological variability (embryo size depends on maternal condition and environmental factors) and has turned out to be one of the most influential parameters in the system.

<!-- FIGURE: Model domain map showing grid resolution and bathymetry -->

#### Data processing pipeline

The raw model output consists of trajectory files tracking hundreds of thousands of virtual drifters at hourly resolution over 180-day simulations. Processing involves:

1. **Extraction and subsampling** — daily positions from hourly output
2. **Classification** — identifying larvae that are retained within nursery regions vs. exported from the model domain vs. lost to bottom strikes
3. **Regional presence analysis** — point-in-polygon testing against nursery region boundaries for each larva at each timestep
4. **Connectivity matrices** — source-destination relationships between spawning areas and nursery grounds, resolved by developmental stage and release timing

The analysis framework separates data processing from visualization to allow flexible exploration of the ~1.2 million row trajectory datasets on a laptop.

#### Extending the time series

The existing ROMS runs cover select years. A major ongoing effort is to **fill gaps in the time series** by running the model for additional years, which requires:

- Acquiring and building atmospheric forcing files
- Preparing ocean boundary conditions
- Generating tidal forcing data
- Substantial computational resources (target: Alpine supercomputing cluster at CU Boulder)

Each new model year adds another realization of wind-driven variability, strengthening our ability to characterize the range of connectivity patterns larvae experience.

{% endtab %}

{% tab connectivity_project What's Next %}

### Research roadmap

This work is actively developing. Here's where it's headed.

#### Completed
- ✅ High-resolution ROMS simulations for 2016–2019 austral summers
- ✅ Particle tracking experiments with descent–ascent biology and varying embryo sizes
- ✅ Connectivity analysis between four nursery regions (BS, GERL, GP, MB)
- ✅ First paper published: [Sylvester et al. 2026, MEPS](https://doi.org/10.3354/meps15059)

#### In progress
- 🔨 **Regional boundary refinement** — moving from simple box-based nursery definitions to oceanographically meaningful boundaries that follow natural features (bathymetric contours, shelf breaks, coastlines)
- 🔨 **Connectivity matrix development** — building source-destination matrices resolved by larval developmental stage and seasonal release timing
- 🔨 **Export vs. retention analysis** — distinguishing larvae that exit the model domain (true exports) from those completing full simulations (retained populations), with attention to early mortality events (bottom strikes before hatching)

#### Planned
- 📋 **Sea ice advection** — incorporating sea ice data to model how near-surface larvae may be transported by ice during winter. Recent analysis has revealed strong seasonal patterns in near-surface behavior: late-season releases (February–March) spend substantially more time near the surface, making them prime candidates for ice-mediated transport.
- 📋 **Extended time series** — running ROMS for additional years to fill gaps in coverage and strengthen interannual variability analysis. This requires access to the Alpine supercomputing cluster at CU Boulder.
- 📋 **Multi-year connectivity synthesis** — combining all available years into a comprehensive picture of connectivity reliability and variability across the wAP.

#### Future directions
- 🔭 **Climate scenario projections** — using the validated connectivity framework to explore how projected changes in circulation, wind patterns, and sea ice affect larval supply pathways
- 🔭 **Integration with recruitment dynamics** — connecting physical connectivity to biological survival (linking to the overwintering survival work in [Sylvester et al. 2025, ICES JMS](/blog/2025/untangling-krill-overwintering/))
- 🔭 **Management applications** — translating connectivity patterns into spatially explicit information relevant for CCAMLR MPA planning in Domain 1

{% endtab %}

{% endtabs %}

---

### Publications

**Sylvester, Z.T.**, Dinniman, M.S., Thorpe, S.E., Bernard, K.S., Brooks, C.M. (2026). Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula. *Marine Ecology Progress Series*, 779, meps15059. [https://doi.org/10.3354/meps15059](https://doi.org/10.3354/meps15059)

### Related work

**Sylvester, Z.**, et al. (2025). Untangling larval Antarctic krill overwinter survival under climate change using a qualitative network model. *ICES Journal of Marine Science*. [https://doi.org/10.1093/icesjms/fsaf049](https://doi.org/10.1093/icesjms/fsaf049)

---
