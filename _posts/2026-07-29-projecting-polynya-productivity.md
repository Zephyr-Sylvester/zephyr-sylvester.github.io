---
layout: post
title: "Research Note: Sea Ice, Polynyas, and Productivity"
date: 2026-07-29
description: "Companion notes for my SCAR OSC 2026 conference poster."
tags: [antarctica, sea ice, polynyas, productivity, climate]
categories: logbook
related_posts: true
featured: true
thumbnail: assets/img/logbook/scarosc2026-thumb.png
---

This page accompanies my poster, “Sea Ice, Polynyas, and Productivity”, presented at the 2026 SCAR Open Science Conference in Oslo in the Life Sciences Session 25, Poster 467 on Thursday August 13, 2026.

The poster presents the main results. This page provides additional context, expanded methods, and discussion that could not fit within the space available on the poster. As the work progresses through manuscript preparation, I will continue updating this page.

---

## Poster


View the poster below, or download the full-resolution PDF.

[Download Poster (PDF)](/assets/pdfs/ZSylvester-2026-SCAR-OSC-Poster467-LifeSciences-S25.pdf)

<iframe
  src="/assets/pdfs/ZSylvester-2026-SCAR-OSC-Poster467-LifeSciences-S25.pdf"
  width="100%"
  height="900"
  style="border: 1px solid #ddd;"
  loading="lazy">
</iframe>


---

## Background

This work forms part of the Antarctic Ecosystem Value (AEV) project, a NASA Applied Sciences collaboration examining how Antarctic coastal ecosystems may respond to future climate change. One component of that project is understanding how the ecological role of coastal polynyas may change over the coming century.

Polynyas are persistent regions of open water within the seasonal sea ice. They receive light earlier than the surrounding sea ice zone and consequently support some of the highest rates of primary production in the Southern Ocean. Because of this, they are frequently described as biological hotspots. Most studies stop at that observation. Here I instead ask how the role of these hotspots changes under future climate conditions.

This analysis focuses on the Amundsen Sea, where rapid changes in sea ice coincide with one of Antarctica's most productive polynya systems.

---

## Research Question

Rather than asking whether primary productivity increases or decreases, this work asks whether polynyas continue to function as biological hotspots throughout the food web.

Primary productivity and mesozooplankton do not necessarily respond in the same way to changing sea ice conditions. If their responses diverge, then the ecological significance of polynyas may also change.

---

## Methods

### Model

The analysis uses output from the Community Earth System Model version 2 (CESM2) coupled with the Marine Biogeochemistry Library (MARBL). Results are drawn from the five-member ensemble forced under SSP3-7.0.

The analysis compares present-day conditions with end-of-century projections (2090s).

### Defining polynyas

Polynya locations were identified using October sea ice conditions. Cells with at least 10% polynya occurrence were classified as polynya habitat. The surrounding seasonal ice zone (SIZ) was defined using a mean winter ice fraction of at least 15%.

These definitions follow the broader AEV framework and allow equivalent regions to be compared through time.

*[Cryosphere methods paper](https://tc.copernicus.org/articles/20/1815/2026/tc-20-1815-2026.pdf)*

### Analysis

For each region I extracted seasonal cycles of:

- net primary productivity (NPP)
- mesozooplankton biomass (MZP)

The objective was not simply to compare annual production, but to examine how seasonal timing changes between present-day and future conditions.

*(Workflow figure here.)*

---

## Results

### Primary productivity

Net primary productivity within polynyas decreases by the end of the century but remains higher than the surrounding seasonal ice zone until winter.

*(Expanded Figure 1.)*

### Mesozooplankton

The response of mesozooplankton differs from primary productivity.

Although the difference in NPP between polynyas and the surrounding sea ice zone becomes smaller, the difference in mesozooplankton biomass increases. By February, projected MZP within historical polynya footprints exceeds that of the surrounding seasonal ice zone, and this difference persists through winter.

*(Expanded Figure 2.)*

### Interpreting the seasonal shift

The projected changes appear to reflect differences in phytoplankton community composition.

Where diatoms remain dominant within polynyas, mesozooplankton biomass is maintained later into the year. Outside the polynyas, increasing dominance of smaller phytoplankton corresponds with reduced mesozooplankton biomass.

The result is that future polynyas become less distinct as regions of exceptionally high primary production while becoming more distinct as regions supporting overwintering mesozooplankton biomass.

*(Conceptual figure.)*

---

## Discussion

One implication is that the ecological importance of polynyas may become increasingly disconnected from their physical definition.

If future food availability becomes concentrated within historical polynya footprints during winter, these regions may continue to function as biological hotspots even as their surface expression weakens.

For the Amundsen Sea, this suggests that ecological importance may increase despite declining physical contrast between polynyas and the surrounding seasonal ice zone.

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