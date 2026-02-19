---
layout: page
title: Krill Connectivity
description: Modeling how ocean currents, biology, and sea ice shape the early life of Antarctic krill
img: assets/img/projects/connectivity/Ascent-descent_Model copy.png
importance: 1
category: research
related_publications: true
tabs: true
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/Ascent-descent_Model copy.png" title="Larval Life Cycle" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
	Larval Krill Development Cycle
</div>

## Where do krill larvae go?
### Using ocean models and particle tracking to understand connectivity

Antarctic krill (*Euphausia superba*) underpin the Southern Ocean food web. But before a krill can join the population, it has to survive one of the most precarious journeys in the ocean: sinking as an embryo toward the deep seafloor, hatching, swimming back to the surface, and then drifting for months through some of the most dynamic waters on Earth.

This research program uses ocean modeling and Lagrangian particle tracking to understand how physical oceanography and larval biology interact to shape connectivity in early life stages.

The goal is to build a mechanistic understanding of *how larvae get from where they're spawned to where they grow up*. I want to know how that process changes across years, under different biological assumptions, and as the ocean and sea ice evolve under climate change.

### How ocean physics and larval biology shape krill connectivity

Krill eggs don't just float. After spawning, embryos sink, sometimes hundreds of meters, before hatching into larvae that swim back toward the surface. This descent-ascent cycle means that the depth of the water column, the speed of the currents at different depths, and the size of the embryo all interact to determine where a larva ends up when it reaches the surface and begins its months-long drift.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/ascent-descent-withtext.png" title="Lagrangian drifter simulation design" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Lagrangian drifter simulation design: The Primary movement of particles is determined by ocean and sea ice velocities depending on sea ice concentrations and particle depth. Additional vertical behavior is determined by the life stage representing how krill larvae move through the water column. This detail is crucial for understanding how they interact with physical ocean properties and the habitat they reach during development.

We use **Regional Ocean Modeling System (ROMS)** at high resolution (~1.5 km) to simulate ocean circulation along the wAP, coupled with offline Lagrangian particle tracking to follow hundreds of thousands of virtual larvae through their early development.

---

## The Research

{% tabs connectivity_project %}

{% tab connectivity_project Modeling Scope %}

#### Developing the Model

Our first paper from this research program ([Sylvester et al. 2026, MEPS](https://doi.org/10.3354/meps15059)) used a circumpolar Southern Ocean ROMS configuration (5 km grid, 25x25 km drifter spacing) to simulate larval krill transport over three austral summers (2016-2019). By focusing on four known nursery grounds along the western Antarctic Peninsula (Bransfield Strait, Gerlache Strait, Grandidier Passage, and Marguerite Bay), we established several key dynamics:

**Self-retention dominates.** In our simulations, the vast majority of larvae that used a nursery ground were spawned within it. Bransfield Strait and Marguerite Bay both function as spawning and nursery grounds simultaneously, with strong local retention.

**Wind drives interannual variability.** The pathways between spawning areas and nursery grounds are relatively stable in structure, but their strength shifts year to year with the wind field. In the Bransfield Strait, for example, seasonal wind patterns determined whether external larvae arrived via along-shelf transport or from the Weddell Sea.

**Marguerite Bay is isolated.** MB received larvae mainly from the south via the Marguerite Trough and did not export larvae northward. The two ends of the wAP are functionally separated when it comes to early life stage connectivity.

**Strengthening westerlies could disrupt connectivity.** Projected poleward intensification of westerly winds could reduce Weddell Sea inflows to the Bransfield Strait and alter the balance of larval supply to northern nursery grounds.

These results provided the proof of concept that motivated the next phase: taking these questions into a high-resolution regional model.

### #### Scaling up: high-resolution regional modeling

The circumpolar model established that connectivity between spawning and nursery grounds is real, structured, and sensitive to wind variability. But its 5 km resolution and coarse drifter spacing leave fine-scale dynamics unresolved. Mesoscale eddies, complex coastline interactions, and the detailed bathymetry of straits and embayments all matter for larval retention and exchange at the scale where nursery grounds actually function.

The current phase of this research uses a high-resolution ROMS configuration for the western Antarctic Peninsula (~1.5 km grid spacing) developed by Mike Dinniman and colleagues. This model resolves mesoscale and some submesoscale circulation features critical for larval transport in this complex coastal environment.

With this higher resolution, we are tracking hundreds of thousands of virtual larvae through their early development, incorporating the same descent-ascent biology but now resolving the circulation patterns that the circumpolar model could not. The result is a much richer picture of how larvae interact with local bathymetry, coastal currents, and retention features within and between nursery regions.

<!-- FIGURE: Model domain comparison showing circumpolar vs. regional resolution -->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/So-simple-ZTS.jpg" title="Circumpolar Scale" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/W Ap dark copy.jpg" title="wAP Scale" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The wAP is the most well studied area in the Southern Ocean for Antarctic krill and is where 70% of their population is located

</div>


{% endtab %}

{% tab connectivity_project Technical Approach %}

### Technical approach: ROMS + Lagrangian particle tracking

#### Two scales, one framework

This research program operates at two model resolutions, each serving a different purpose:

**Circumpolar model** (published in [Sylvester et al. 2026, MEPS](https://doi.org/10.3354/meps15059))
- Southern Ocean ROMS, 5 km grid, 32 vertical layers
- ERA5 atmospheric forcing from ECMWF
- Drifters released on a 25x25 km grid across the Southern Ocean
- Simulated 2016-2019 austral summers
- Established connectivity patterns and identified key dynamics

**High-resolution regional model** (in progress)
- Western Antarctic Peninsula ROMS, ~1.5 km grid spacing
- Resolves mesoscale and submesoscale circulation
- Atmospheric (ERA5), oceanic boundary conditions, tidal forcing
- Simulated 2016-2019 austral summers with additional existing runs from 2006-2012
- Hundreds of thousands of drifters per simulation

#### What makes this approach different

Most larval dispersal studies treat particles as passive tracers. Our simulations incorporate the descent-ascent developmental cycle: embryos sink at empirically derived rates, hatch at depth, and larvae swim upward at stage-appropriate speeds. This means particles interact with different current regimes at different depths during their early life, producing fundamentally different connectivity patterns than passive simulations would predict.

We also vary initial embryo size, which controls sinking rate and therefore hatching depth. This parameterization captures real biological variability (embryo size depends on maternal condition and environmental factors) and has turned out to be one of the most influential parameters in the system.

<!-- FIGURE: Model domain map showing grid resolution and bathymetry --> 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/connectivity/hi-res-example-startingpoint.png" title="Hi-res example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of analyzing the wAP Lagrangian drifter release locations
</div>

#### Data processing pipeline

The raw model output consists of trajectory files tracking hundreds of thousands of virtual drifters at hourly resolution over 180-day simulations. Processing involves:

1. **Extraction and subsampling:** daily positions from hourly output across multiple release cohorts
2. **Classification:** identifying larvae that are retained within nursery regions vs. exported from the model domain vs. lost to bottom strikes during the descent-ascent cycle
3. **Regional presence analysis:** point-in-polygon testing against nursery region boundaries for each larva at each timestep
4. **Connectivity matrices:** source-destination relationships between spawning areas and nursery grounds, resolved by developmental stage and release timing

The analysis framework separates data processing from visualization to allow flexible exploration of trajectory datasets (on the order of 1.2 million rows per simulation).


{% endtab %}

{% tab connectivity_project What's Next %}

### Research roadmap

This work is actively developing. Here's where it's headed.

#### Completed
- ✅ Circumpolar ROMS simulations establishing proof of concept (2016-2019)
- ✅ First paper published: [Sylvester et al. 2026, MEPS](https://doi.org/10.3354/meps15059)
- ✅ High-resolution regional ROMS simulations for select years
- ✅ Particle tracking experiments with descent-ascent biology and varying embryo sizes
- ✅ Connectivity analysis between four nursery regions (BS, GERL, GP, MB)

#### In progress
- 🔨 **Regional boundary refinement:** moving from simple box-based nursery definitions to oceanographically meaningful boundaries that follow natural features like bathymetric contours, shelf breaks, and coastlines
- 🔨 **Connectivity matrix development:** building source-destination matrices resolved by larval developmental stage and seasonal release timing
- 🔨 **Export vs. retention analysis:** distinguishing larvae that exit the model domain (true exports) from those completing full simulations (retained populations), with attention to early mortality events like bottom strikes before hatching

#### Planned
- 📋 **Sea ice advection:** incorporating sea ice data to model how near-surface larvae may be transported by ice during winter. Recent analysis has revealed strong seasonal patterns in near-surface behavior, with late-season releases (February through March) spending substantially more time near the surface, making them prime candidates for ice-mediated transport.
- 📋 **Extended time series:** running ROMS for additional years to fill gaps in coverage and strengthen interannual variability analysis.Each new model year adds another realization of wind-driven variability, strengthening our ability to characterize the range of connectivity patterns larvae experience.
- 📋 **Multi-year connectivity synthesis:** combining all available years into a comprehensive picture of connectivity reliability and variability across the wAP.

#### Future directions
- 🔭 **Climate scenario projections:** using the validated connectivity framework to explore how projected changes in circulation, wind patterns, and sea ice could affect larval supply pathways
- 🔭 **Integration with recruitment dynamics:** connecting physical connectivity to biological survival
- 🔭 **Management applications:** translating connectivity patterns into spatially explicit information relevant for CCAMLR MPA planning in Domain 1

{% endtab %}

{% endtabs %}

---

### Publications and Media

**Sylvester, Z.T.**, Dinniman, M.S., Thorpe, S.E., Bernard, K.S., Brooks, C.M. (2026). Modeled connectivity of Antarctic krill spawning and nursery grounds along the Western Antarctic Peninsula. *Marine Ecology Progress Series*, 779, meps15059. [https://doi.org/10.3354/meps15059](https://doi.org/10.3354/meps15059)


---
