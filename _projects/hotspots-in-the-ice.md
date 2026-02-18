---
layout: page
title: Hot Spots in the Ice
description: A tool for exploring Antarctic ecosystem value, now and into the future
img: assets/img/projects/aev/IMG_2623-ZTS-ice-edge-ice-wall.jpg
importance: 1
category: research
related_publications: true
tabs: true
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/IMG_2623-ZTS-ice-edge-ice-wall.jpg" title="Antarctic ice edge" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Antarctic ice edge. Photo: Zephyr Sylvester.
</div>

## Creating an Antarctic Ecosystem Value (AEV) Index 
#### Translating earth system science into a tool for decision makers, scientists and the general public 

In 2020, researchers at CU Boulder and NCAR researchers started wondering if it was possible to expand the capacity of Earth System Models to make future projections relevant for decision makers and scientists regarding the ecosystem value of polynyas. So they pulled together a proposal that would take an applied science approach and produce not just science, but science communication tools for decision makers and scientists determining conservation policy.

One NASA grant later and a team of 12 scientists across 7 institutions was assembled to bring together satellite data, biological models, and Earth System Model projections to ask: **which parts of Antarctica matter most ecologically — and which will still matter in a warming world?**

Our goal was to take science that is so rarely understood by those outside of academia and make it both applicable to management goals and approachable to decision makers and the public. 

To do so, we created an Antarctic Ecosystem Value index and [built an interactive tool](https://only.one/campaign/antarctica-ecoindex) to allow users to interact with it as either a science product or as a story telling tool. 

You can interact with our work as stories, visualize the data, or download it for your own research - whatever your interest, there's something for you.

---
## Pick your background

{% tabs aev_project %}

{% tab aev_project Casual Explorer %}

Antarctica isn't just ice. Hidden in the gaps are patches of open water called **polynyas**. A polynya (from the Russian word for "open water") is a persistent patch of open ocean surrounded by sea ice. They form when wind or upwelling currents keep the surface clear, even in the depths of winter. Think of them as oases in the frozen desert, and like oases, life concentrates around them. Some polynyas span hundreds of kilometers and generate more biological productivity per square meter than almost anywhere else in the Southern Ocean. 

Within polynyas, microscopic algae can start blooming as soon as the sun returns to the South. With an abundance of food in these areas, krill swarm, and penguins, seals, and whales follow.

Now imagine all of that shifting as the climate warms. That's the story we set out to tell. And rather than bury it in a scientific journal, we put it on a map and handed you the controls.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/DSC05926-ZTS_snowburg.JPG" title="Antarctic iceberg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/IMG_2116-ZTS_floating-ice-flake.jpg" title="ice forming on the surface, Antarctica" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/DSC05975-ZTS-building-like-ice.jpg" title="Tabular iceberg, Antarctica" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Southern Ocean in all its forms: never ending snow and ice, ice forming, and a towering tabular berg. Photos: Zephyr Sylvester.
</div>

#### We Built a Map — and Projected It to 2090

Our team spent several years pulling together data from satellites, biological models, and Earth System Models to build the **Antarctic Ecosystem Value (AEV) Index** — a way of scoring each part of the Southern Ocean based on how important it is for phytoplankton, krill, fish, penguins, and other wildlife. Then we projected it forward to the year 2090.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide6.png" title="AEV Index — present day" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide8.png" title="AEV Index — 2090 projection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The AEV Index present day (left) and projected to 2090 (right). Brighter blue = higher ecological value; pink = polynya extent; green = regions of exceptional value. Note the poleward contraction of high-value areas by end of century.
</div>

The results are striking. Some places — like the northern Antarctic Peninsula — are already losing ecological value as sea ice retreats. Others, like the Ross Sea and the Amundsen Sea, may remain productive refuges well into the next century. Some, counterintuitively, may even become *more* productive as warming reshapes ocean circulation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide10.png" title="Antarctic Peninsula story" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide11.png" title="Amundsen Sea story" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide12.png" title="Ross Sea story" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Three focal regions: the Antarctic Peninsula, the Amundsen Sea, and the Ross Sea. Photography: John B. Weller.
</div>

#### Explore It Yourself

On the interactive map you can toggle **species-specific layers** (phytoplankton, krill, fish, penguins), switch between **present-day and 2090 projections**, and read **narrative stories** about each focal region.

<a href="https://only.one/map/antarctica-ecoindex#3.7/-85/169" class="btn btn-sm z-depth-0" role="button" style="background-color: #1a6b8a; color: white;">🗺️ Explore the AEV Index</a>

{% endtab %}


{% tab aev_project Fellow Researcher %}

### Methods, Data, and Tools

This project formalizes the **Antarctic Ecosystem Value (AEV) Index** — a spatially explicit, present and future assessment of ecosystem value for Antarctic coastal polynyas, developed as part of a NASA Applied Sciences ecological forecasting grant.

#### Index Construction

Data layers were developed across three domains and integrated with Earth System Model experiments to generate present-day and 2090 projections:

| Layer Domain | Data Sources |
|---|---|
| **Physical** | Polynya extent and seasonality from satellite passive microwave |
| **Biological** | Primary productivity and krill distribution from satellite-derived and modeled products |
| **Predator** | Penguin, seal, and toothfish distribution and density data |

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide3.png" title="Applied science framework" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide4.png" title="Science goals and products" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide5.png" title="Data layer development timeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The applied science framework (left), science goals and decision support structure (center), and data layer development timeline with CCAMLR feedback integration (right).
</div>

#### Key Regional Findings

| Region | Present | 2090 | Key Dynamic |
|---|---|---|---|
| Peninsula (North) | High | Declining | Sea ice loss, krill contraction |
| Peninsula (South) | High | Stable | Potential krill climate refugium |
| Amundsen Sea | Very High | Increasing | Most productive polynya per m²; no MPA |
| Ross Sea | Very High | Stable–Increasing | Strong overlap with RSRMPA |
| Prydz Bay | Moderate–High | Variable | Krill spawning aggregations |
| Weddell Sea | High | Variable | Complex circulation dynamics |
| D'Urville Sea | Moderate | Variable | Data-sparse region |

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide13.png" title="Six focal regions" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide12.png" title="Regional navigation in web tool" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Six focal regions identified by the AEV Index (left) and the regional navigation interface in the web tool (right).
</div>

#### Iterative Co-Development with CCAMLR

The index was developed iteratively, with formal and informal feedback loops through CCAMLR Working Group presentations over multiple years — shaping analytical choices from the start rather than as post-hoc stakeholder engagement. We'd encourage other groups developing management-relevant indices to build this structure in early.

#### The Index Comparison Shiny App

Developed in direct response to a recurring question from CCAMLR delegations — *how does this compare to KBAs, AES, and existing bioregionalizations?* — the app integrates all major circumpolar-scale important area analyses in one place.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide18.png" title="Shiny app — AEV layer" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide19.png" title="Shiny app — AEV + KBA" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide20.png" title="Shiny app — AEV + KBA + AES" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Progressive layer toggling in the Index Comparison Tool: AEV Index alone (left), with Key Biodiversity Areas (center), and with Areas of Ecological Significance added (right).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide23.png" title="Summary table builder" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide25.png" title="Ross Sea MPA overlap table" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Quantitative overlap interface: configurable summary table builder (left) and example output for the Ross Sea MPA (right).
</div>

#### Data

All AEV Index data layers are openly archived on Zenodo: [https://zenodo.org/records/16990591](https://zenodo.org/records/16990591)

If you're working on something where the AEV data could be useful, reach out — we're interested in how the index performs in contexts beyond its original development.

<a href="https://only.one/map/antarctica-ecoindex#3.7/-85/169" class="btn btn-sm z-depth-0" role="button" style="background-color: #1a6b8a; color: white;">AEV Web Tool</a>
<a href="https://saef-monash.shinyapps.io/antarctic_map/" class="btn btn-sm z-depth-0" role="button" style="background-color: #2d6a4f; color: white;">Index Comparison App</a>
<a href="https://zenodo.org/records/16990591" class="btn btn-sm z-depth-0" role="button" style="background-color: #555555; color: white;">Data on Zenodo</a>

{% endtab %}

{% tab aev_project Fishery Manager %}

### Science in Support of Antarctic Conservation Planning

*This work was presented at CCAMLR-44 as Paper SC-CAMLR-44-BG-26 and is now published — see citation below.*

Managing Antarctica's living marine resources means making decisions under uncertainty — about where species are, where they'll be in a warming ocean, and which areas are most critical to protect. The AEV Index and Index Comparison Tool were built to directly support that challenge.

#### Present and Future Ecosystem Value

The AEV Index scores the ecological importance of Antarctic coastal waters based on phytoplankton, krill, fish, and predator data — with projections to **2090** to help assess which areas will remain valuable under climate change.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide7.png" title="AEV Index with CCAMLR MPA boundaries" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide8.png" title="AEV 2090 with MPA boundaries" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The AEV Index present day (left) and 2090 projection (right) with existing and proposed CCAMLR MPA boundaries overlaid.
</div>

#### Implications for the MPA Network

**Antarctic Peninsula — D1MPA**
The northern and southern Peninsula are diverging ecologically. The north is losing sea ice and krill habitat. The south — including the area encompassed by the proposed Domain 1 MPA — shows greater stability and potential as a **climate refugium for krill** through the end of the century. The AEV Index provides quantitative support for the D1MPA ecological rationale.

**Amundsen Sea — A Gap in the Network**
The Amundsen Sea hosts the most productive polynyas per square meter in Antarctica and is projected to *increase* in productivity by 2090. There is currently no proposed MPA for this region despite ongoing pressure from toothfish fisheries. The AEV Index identifies this as a significant gap in the current network.

**Ross Sea — Supporting the 10-Year Review**
The AEV Index confirms the high ecological value of the Ross Sea polynya and projects stable or increasing productivity through the century — providing independent evidence of the RSRMPA's long-term effectiveness ahead of future reviews.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide14.png" title="Antarctic Peninsula AEV results" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide15.png" title="Amundsen Sea AEV results" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide16.png" title="Ross Sea AEV results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    AEV Index results for three key MPA-relevant regions: the Antarctic Peninsula (left), Amundsen Sea (center), and Ross Sea (right).
</div>

#### The Index Comparison Tool

Built specifically in response to questions from CCAMLR delegations, the tool aggregates all major circumpolar important area analyses and bioregionalizations. Select any **CCAMLR MPA planning domain** or **existing/proposed MPA** to calculate overlap with all available layers and download results as summary tables for working group documents.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide24.png" title="Ross Sea domain overlap table" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/aev/hotspots-slide-pngs/Slide26.png" title="Benthic bioregions in Ross Sea MPA" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example outputs: important area overlap within the Ross Sea Planning Domain (left), and benthic bioregion representation within the Ross Sea MPA (right).
</div>

All data are open access and available for independent use in working group analyses.

<a href="https://only.one/map/antarctica-ecoindex#3.7/-85/169" class="btn btn-sm z-depth-0" role="button" style="background-color: #1a6b8a; color: white;">AEV Index Map</a>
<a href="https://saef-monash.shinyapps.io/antarctic_map/" class="btn btn-sm z-depth-0" role="button" style="background-color: #2d6a4f; color: white;">Index Comparison Tool</a>
<a href="https://zenodo.org/records/16990591" class="btn btn-sm z-depth-0" role="button" style="background-color: #555555; color: white;">Download Data</a>

{% endtab %}

{% endtabs %}

---

### The Team

This project was built by 12 scientists across 7 institutions over three years, funded by NASA Applied Sciences Biodiversity and Ecological Forecasting (Grant 80NSSC21K1132).

<div class="row align-items-center justify-content-center mt-3">
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/CUBoulder.png' | relative_url }}" alt="University of Colorado Boulder" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/USGS.png' | relative_url }}" alt="U.S. Geological Survey" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/UCCant.png' | relative_url }}" alt="University of Canterbury" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/LOCEAN.png' | relative_url }}" alt="LOCEAN" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/WHOI.png' | relative_url }}" alt="Woods Hole Oceanographic Institution" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/NCAR.png' | relative_url }}" alt="National Center for Atmospheric Research" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/IBED.png' | relative_url }}" alt="IBED, University of Amsterdam" style="max-height: 50px; width: auto;">
    </div>
    <div class="col-auto mt-2 mt-md-0 text-center px-2">
        <img src="{{ 'assets/img/projects/aev/logos/NASA.png' | relative_url }}" alt="NASA" style="max-height: 50px; width: auto;">
    </div>
</div>
<div class="caption mt-2">
    CU Boulder · USGS · University of Canterbury · LOCEAN · WHOI · NCAR · IBED (University of Amsterdam) · NASA
</div>

---

### Photography

Media produced and featured on the OnlyOne project page are the work of photographer **John B. Weller**, whose photography has taken him from the Arctic to the Antarctic in service of ocean conservation.

**[Explore his work at johnbweller.com →](https://www.johnbweller.com)**

---

### Publications from This Project

**Primary paper:**
DuVivier, A.K., Krumhardt, K., Landrum, L.L., Sylvester, Z. et al. (2026). An Antarctic ecosystem value index to quantify ecological value across trophic levels and over time. *Nature Communications.* [https://doi.org/10.1038/s41467-026-69011-0](https://doi.org/10.1038/s41467-026-69011-0)

**Companion methods paper:**

Landrum, L.L., DuVivier, A.K., Holland, M.M., Krumhardt, K., and Sylvester, Z. (in press). Defining Antarctic polynyas in satellite observations and climate model output to support ecological climate change research. *The Cryosphere.* [https://doi.org/10.5194/egusphere-2024-3490](https://doi.org/10.5194/egusphere-2024-3490)

**Related observational work:**

Bourreau, L., Pauthenet, E., Le Ster, L., Picard, B., Portela, E., Sallée, J-B., McMahon, C.R., Harcourt, R., Hindell, M., Guinet, C., Bestley, S., Charrassin, J-B., DuVivier, A., Sylvester, Z., Krumhardt, K., Jenouvrier, S., and Labrousse, S. (2023). First description of *in situ* chlorophyll fluorescence signal within East Antarctic coastal polynyas during fall and winter. *Frontiers in Marine Science.* [https://doi.org/10.3389/fmars.2023.1186403](https://doi.org/10.3389/fmars.2023.1186403)

