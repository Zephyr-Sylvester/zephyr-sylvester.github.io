---
layout: post
title: "Research Note: Sea Ice, Polynyas, and Productivity"
date: 2026-07-29
description: "Companion notes for my SCAR OSC 2026 conference poster."
tags: [antarctica, sea ice, polynyas, productivity, climate]
categories: logbook
related_posts: true
featured: true
thumbnail: assets/img/logbook/scarosc2026/scarosc2026-thumb.png
---

This page accompanies my poster, “Sea Ice, Polynyas, and Productivity”, presented at the 2026 SCAR Open Science Conference in Oslo in the Life Sciences Session 25, Poster 467 on Thursday August 13, 2026.

The poster presents the main results. This page provides additional context, expanded methods, and discussion that could not fit within the space available on the poster. As the work progresses through manuscript preparation, I will continue updating this page.

---

## Poster


View the poster below, or download the full-resolution PDF.

<object data="/assets/pdfs/ZSylvester-2026-SCAR-OSC-Poster467-LifeSciences-S25.pdf"
        type="application/pdf"
        width="100%"
        height="900">
  <p>
    Your browser does not support embedded PDFs.
    <a href="/assets/pdfs/ZSylvester-2026-SCAR-OSC-Poster467-LifeSciences-S25.pdf">
      Download the poster PDF.
    </a>
  </p>
</object>




---

## Background

This work is one component of the broader Antarctic Ecosystem Value (AEV) Project, a NASA Applied Sciences collaboration bringing together satellite observations, Earth System Models, biological models, and ecological datasets to understand how Antarctic ecosystems may change under future climate scenarios.

The broader project asks where ecological value is concentrated around Antarctica and how those patterns may change through the end of the century. This study focuses on one part of that problem by examining how changing sea ice alters the ecological role of coastal polynyas within the marine food web.

---

{% tabs sea_ice_polynyas %}

{% tab sea_ice_polynyas Southern Ocean Dynamics %}

The Southern Ocean is characterized by a long polar night followed by a brief period of intense biological production when light returns each spring. Sea ice plays a central role in this seasonal cycle by controlling when sunlight reaches the ocean surface. As sea ice retreats, primary productivity follows, creating the familiar band of high productivity along the receding ice edge.

This seasonal pattern provides the basic context for understanding where and when biological production occurs across Antarctica.

{% endtab %}

{% tab sea_ice_polynyas Polynyas %}

Within the seasonal sea ice zone, there are important exceptions to the normal seasonal cycle.

Coastal polynyas remain ice-free through much of the winter and spring. Because they receive light earlier than the surrounding sea ice zone, they support some of the earliest and largest phytoplankton blooms in Antarctica. These blooms fuel food webs that support krill, fish, seabirds, seals, and whales, making polynyas some of the most biologically important regions of the Southern Ocean.

The key question is whether that role changes as the climate warms and sea ice continues to shift.

{% endtab %}

{% tab sea_ice_polynyas Climate Change %}

As Antarctic sea ice changes, the timing, extent, and persistence of productive habitat are also likely to change.

This matters because sea ice is not only a physical boundary. It shapes light availability, productivity, and the seasonal structure of the marine food web. If the seasonal sea ice zone contracts and polynyas shift in space or function, the ecological importance of these regions may also shift.

This work asks whether polynyas remain biological hotspots in a warmer climate, or whether their ecological role changes.

{% endtab %}

{% endtabs %}

## Why the Amundsen Sea?

To answer this question I examined productivity at several spatial scales, beginning with a circumpolar assessment before focusing on the Amundsen Sea as a regional case study.

The Amundsen Sea is one of the most rapidly changing regions of Antarctica. It is experiencing substantial sea ice loss, rapid glacial change, and contains two highly productive coastal polynyas: the Pine Island Polynya and the Amundsen Sea Polynya. Climate projections also suggest that the region may become increasingly favourable habitat for Antarctic krill.

Together, these characteristics make it an ideal region for exploring how changes in sea ice may alter the ecological role of polynyas.

## Methods

To investigate future changes, I used output from the Community Earth System Model version 2 (CESM2) coupled to the Marine Biogeochemistry Library (MARBL).

Earth system models simulate the coupled atmosphere, ocean, sea ice, and land surface, allowing biological responses to emerge from changing climate conditions rather than being imposed externally.

Within MARBL I focused on three complementary measures of ecosystem function:

- Net primary production (NPP), representing the rate of phytoplankton production.
- Mesozooplankton production (MZP), representing secondary production relevant to Antarctic krill and higher trophic levels.
- Mesozooplankton biomass, representing the accumulated impact of production on ecosystem structure and energy flow.

Comparing these variables allows us to distinguish between changes in productivity and changes in the biological consequences of that productivity.

## More detail on the methods

{% tabs sea_ice_methods %}

{% tab sea_ice_methods Earth System Model Simulations %}

To investigate how Southern Ocean productivity may change in the future, I used output from the Community Earth System Model version 2 (CESM2), a fully coupled Earth System Model that simulates interactions between the atmosphere, ocean, sea ice, and land surface. The marine ecosystem is represented using the Marine Biogeochemistry Library (MARBL), allowing biological responses to emerge from changing physical conditions rather than being imposed externally.

A particular strength of this model configuration is its representation of polar ecosystems. MARBL explicitly accounts for light transmission through sea ice and represents multiple plankton functional types, making it well suited for examining how changing sea ice influences Southern Ocean productivity.

To account for natural climate variability, I analyzed a five-member ensemble forced with historical conditions followed by the SSP3-7.0 emissions scenario. Throughout this study I compare present-day conditions (2010s) with end-of-century projections (2090s).

{% endtab %}

{% tab sea_ice_methods MARBL and the Planktonic Ecosystem %}

The marine ecosystem within CESM2 is represented by MARBL, which simulates four phytoplankton and two zooplankton functional types. Rather than representing individual species, these functional groups capture organisms with similar ecological roles.

For this study I focused on three complementary metrics:

- **Net Primary Production (NPP)**, representing the rate of phytoplankton production.
- **Mesozooplankton Production (MZP)**, representing secondary production available to higher trophic levels.
- **Mesozooplankton Biomass**, representing the accumulated effect of production on ecosystem structure and energy flow.

Together these variables distinguish between the ecosystem's functional state (production) and the biological consequences of that production (biomass). Mesozooplankton are of particular interest because they occupy an important position in the Southern Ocean food web, transferring energy from primary producers toward krill, fish, seabirds, and marine mammals.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/assets/img/logbook/scarosc2026/MARBL-trophics.png" title="4P2Z Ecosystem" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Trophic relationships within the 4P2Z MARBL Ecosystem
</div>


{% endtab %}

{% tab sea_ice_methods Defining Regions: SIZ and Polynya Criteria %}

The analysis compares productivity within two environments: coastal polynyas and the surrounding Seasonal Sea Ice Zone (SIZ).

The SIZ was defined as regions where the mean winter sea ice fraction (July–September) exceeded 15%. Using a winter average rather than a single month captures the broader seasonal extent of Antarctic sea ice while remaining consistent with previous studies.

Polynyas were identified using an automated detection algorithm applied to model sea ice concentration. Rather than analysing individual polynya events, I defined persistent **polynya footprints** as locations where a polynya was detected during at least 10% of ensemble members in October.

October was chosen because it represents the transition between winter and spring, when newly opened water begins receiving sunlight and initiates the seasonal phytoplankton bloom. Even when polynyas later merge with surrounding open water, these October footprints continue to represent the regions where biological production first develops each year.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/assets/img/logbook/scarosc2026/Figure-ASR-Reference-2010to2090.png" title="Amundsen Sea Projected Sea Ice" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    CESM2-ME projected SIZ and polynya boundaries in the 2010's vs the 2090's
</div>


{% endtab %}

{% tab sea_ice_methods Analysis %}

The analysis progresses from broad circumpolar patterns to a regional case study.

First, I quantified changes in sea ice, polynya extent, and biological production across the Southern Ocean to identify large-scale patterns of change.

I then focused on the Amundsen Sea, comparing seasonal cycles within coastal polynyas and the surrounding seasonal sea ice zone under present-day and projected future conditions. By examining NPP, mesozooplankton production, and mesozooplankton biomass together, the analysis distinguishes changes in primary production from changes in the transfer of energy through the food web.


{% endtab %}

{% endtabs %}

## Results

At the circumpolar scale, the seasonal sea ice zone decreases in area across much of Antarctica, while changes in polynya extent vary among regions. Productivity also changes differently among regions, motivating a closer look at individual systems.

In the Amundsen Sea, net primary productivity changes in both environments. Productivity increases within the seasonal sea ice zone, while productivity within polynyas declines relative to present-day conditions. Even so, polynyas remain more productive than the surrounding sea ice zone throughout much of the growing season.

The response of mesozooplankton is different.

Although the difference in primary productivity between polynyas and the seasonal sea ice zone becomes smaller, the difference in mesozooplankton production becomes larger. Production within the seasonal sea ice zone increases later in summer before declining rapidly in autumn, whereas production within polynyas remains elevated for longer.

Because biomass integrates production through time, this seasonal persistence results in substantially higher mesozooplankton biomass entering winter within polynya regions.

## Discussion

These results suggest that the ecological role of polynyas changes rather than disappears.

Today, polynyas are recognised primarily because they initiate production early in the growing season. Under projected future conditions, they continue to support enhanced production, but their greatest ecological importance may instead lie in maintaining higher mesozooplankton biomass later in the year.

Rather than functioning primarily as spring hotspots, polynyas may increasingly become overwintering hotspots that maintain food availability after production in the surrounding seasonal sea ice zone has declined.

This shift has important implications for Antarctic krill and the predators that depend upon them.


---

## Relation to the Antarctic Ecosystem Value project

This analysis represents one component of the broader Antarctic Ecosystem Value project.

The AEV Index integrates physical, biological, and predator datasets to identify regions of high ecological value around Antarctica and project how those regions may change under future climate scenarios. Understanding how polynyas influence lower trophic levels provides part of the ecological foundation for that broader assessment.

Further information is available on the project page:

- Hot Spots in the Ice
- Antarctic Ecosystem Value interactive map
- Index Comparison Tool

---

## Current Status

Analysis completed: 2025

Presented at SCAR Open Science Conference 2026.

Manuscript in preparation.

---

## Acknowledgements

This work was supported by NASA Applied Sciences, Biodiversity and Ecological Forecasting (Grant 80NSSC21K1132).

Collaborators:

Kristen Krumhardt

Alice DuVivier

Laura Landrum

National Center for Atmospheric Research

University of Colorado Boulder