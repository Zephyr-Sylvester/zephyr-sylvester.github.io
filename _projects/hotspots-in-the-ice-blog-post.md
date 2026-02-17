# Hot Spots in the Ice: A Tool for Exploring Ecosystem Value

*By Cassandra Brooks and Zephyr Sylvester | [Month] 2026*

> 🎉 **Our paper is out!** "[Paper Title Here]" is now published in [Journal Name]. [Read it here →](https://doi.org/XXXX)

---

*What follows is the same story told three ways. Choose the tab that fits you best — or read all three.*

{% tabs hotspots %}

{% tab hotspots 🌊 Curious Explorer %}

## The Ocean Beneath the Ice Is Changing — and We Built a Map to Show It

Picture Antarctica not as a frozen wasteland, but as one of the most productive ecosystems on Earth. Hidden beneath the sea ice, in patches of open water called **polynyas**, entire food webs hinge on a few months of Antarctic summer sunlight. Microscopic algae bloom. Krill swarm. Penguins, seals, and whales follow.

Now picture all of that shifting — contracting toward the poles — as the climate warms.

That's the story we set out to tell. And we didn't just want to publish it in a scientific journal where it might collect digital dust. We wanted to put it on a map, hand you the controls, and let you explore it yourself.

<!-- 📸 IMAGE SUGGESTION: Hero image of Antarctic polynya from satellite or aerial — open water surrounded by sea ice -->

### What Is a Polynya, Anyway?

A polynya (pronounced *pol-IN-ya*, from the Russian word for "open water") is a persistent patch of open water surrounded by sea ice. They form when wind or upwelling ocean currents keep the surface clear, even in the depths of winter. Think of them as oases in the frozen desert — and like oases, life concentrates around them.

These aren't small features. Some polynyas span hundreds of kilometers and generate more biological productivity per square meter than almost anywhere else in the Southern Ocean.

<!-- 📸 IMAGE SUGGESTION: Diagram or satellite image labeling a polynya within sea ice -->

### We Asked: How Valuable Are These Places — and for How Long?

Our team of 12 scientists across 7 institutions spent several years pulling together data from satellites, biological models, and Earth system models to answer one question: **how ecologically valuable are Antarctica's coastal polynyas, today and into the future?**

We built something we call the **Antarctic Ecosystem Value (AEV) Index** — a way of scoring each part of the Southern Ocean based on how important it is for phytoplankton, krill, fish, penguins, and other wildlife. Then we projected it forward to the year 2090.

The results are striking. Some places — like the northern Antarctic Peninsula — are already losing their ecological value as sea ice retreats. Others, like the Ross Sea and parts of the Amundsen Sea, may remain productive refuges well into the next century. And some, counterintuitively, may even become *more* productive as warming reshapes ocean circulation.

<!-- 📸 IMAGE SUGGESTION: Side-by-side map comparison of AEV Index present vs. 2090 projection -->

### Explore It Yourself

We built an interactive website so you don't have to take our word for it. You can:

- Toggle between **different species layers** (phytoplankton, krill, fish, penguins) to see which places matter most for which wildlife
- Switch between **present-day and 2090 projections** to watch the map change before your eyes
- Read **narrative stories** about specific regions — the Antarctic Peninsula, the Amundsen Sea, the Ross Sea — that explain not just the *what*, but the *why*

**[🗺️ Explore the Antarctic Ecosystem Value Index →](https://PLACEHOLDER-TOOL-URL)**

<!-- 📸 IMAGE SUGGESTION: Screenshot of the interactive map homepage showing AEV Index in blue with polynya overlays in pink -->

### Why Does This Matter?

Antarctica may feel distant, but it's connected to everything. The Southern Ocean absorbs roughly **40% of the world's human-produced CO₂** and plays a critical role in regulating global climate. Antarctic krill — small shrimp-like crustaceans that swarm in the billions — support virtually every predator in the ecosystem, from penguins to blue whales. And krill are commercially fished, meaning there are real management decisions being made right now about how much can be harvested and where.

Knowing which places are most valuable — and which will remain so in a warming world — isn't just academically interesting. It's the kind of information that should be shaping where we protect, and what we preserve.

<!-- 📸 IMAGE SUGGESTION: Photo of krill swarm or a predator (e.g., penguin or whale) in Antarctic waters -->

---

*Want to dig deeper? The full dataset is freely available on [Zenodo](https://zenodo.org/records/16990591). And if you want to compare our index to other important area analyses, check out the [Index Comparison Tool →](https://saef-monash.shinyapps.io/antarctic_map/).*

{% endtab %}

{% tab hotspots 🔬 Fellow Researcher %}

## The AEV Index: What We Built, How It Works, and How You Can Use It

This post summarizes the methods, data products, and tools from our new paper ([citation + DOI here]), which formalizes the Antarctic Ecosystem Value (AEV) Index and its associated interactive platforms. We're sharing this as a practical overview for researchers who may want to use the data, reproduce the analysis, or build on the framework.

<!-- 📸 IMAGE SUGGESTION: Conceptual figure from the paper showing the AEV index construction workflow -->

### The Science Behind the Index

The AEV Index was developed as part of a NASA Applied Sciences grant focused on improving ecological forecasting capacity for decision-relevant Earth System Model (ESM) outputs. The core goal: create spatially explicit, present and future projections of ecosystem value for Antarctic coastal polynyas, integrating physical and biological data streams into a single composite metric.

**Data layers** were developed across three domains:

- **Physical:** Polynya extent and seasonality derived from satellite passive microwave data
- **Biological:** Primary productivity and krill distribution/abundance from satellite-derived and modeled data products
- **Predator:** Distribution and density data for key indicator species (penguins, seals, toothfish)

These layers were integrated with ESM experiments to generate present-day and end-of-century (2090) projections under climate forcing scenarios.

<!-- 📸 IMAGE SUGGESTION: Figure showing the three data layer categories and how they combine into the AEV Index -->

### Key Findings by Region

The index identified several regions of particularly high current and/or future value:

| Region | Present Value | 2090 Projection | Notable Feature |
|---|---|---|---|
| Antarctic Peninsula (North) | High | Declining | Sea ice loss driving krill habitat contraction |
| Antarctic Peninsula (South) | High | Relatively stable | Potential climate refugium for krill |
| Amundsen Sea | Very High | Increasing productivity | Most productive polynya per m²; no current MPA |
| Ross Sea | Very High | Stable to increasing | Strong overlap with existing RSRMPA |
| Prydz Bay | Moderate–High | Variable | Krill spawning aggregations |
| Weddell Sea | High | Variable | Complex circulation dynamics |
| D'Urville Sea | Moderate | Variable | Data-sparse region |

<!-- 📸 IMAGE SUGGESTION: Circumpolar map showing the 7 focal regions with AEV scores -->

### Iterative Co-Development with CCAMLR

One aspect of this project we want to highlight for the methods record: the index was developed iteratively, with formal and informal feedback loops through CCAMLR Working Group presentations over several years. This wasn't post-hoc stakeholder engagement — it shaped analytical choices, including which species layers to prioritize and how to communicate uncertainty in projections.

We'd encourage other research groups developing management-relevant indices to build this kind of feedback structure in from the start rather than retrofitting it later.

### The Interactive Tools

We built two platforms, both freely accessible:

**1. Antarctic Ecosystem Value Index Web Tool**
An interactive map designed for broad engagement — researchers, managers, and public audiences. Features include:
- Toggleable species-specific value layers
- Present vs. 2090 projection comparison
- Regional narrative stories integrating science and ecological context
- Links to open data

**[→ AEV Web Tool](https://PLACEHOLDER-TOOL-URL)**

**2. Index Comparison Shiny App**
Designed specifically to address a recurring question from CCAMLR delegations: *how does this new index compare to existing important area analyses?*

The app integrates the AEV Index alongside all major circumpolar-scale biodiversity analyses and bioregionalizations, including Key Biodiversity Areas (KBAs), Areas of Ecological Significance (AES), and benthic bioregionalizations. Key functionality:
- Visual layer toggle for spatial overlap assessment
- Quantitative overlap calculations for any CCAMLR MPA planning domain or existing/proposed MPA
- Downloadable summary tables
- Full data documentation

**[→ Index Comparison Shiny App](https://saef-monash.shinyapps.io/antarctic_map/)**

### Data Availability

All AEV Index data layers are archived and openly available on Zenodo:

📦 **[https://zenodo.org/records/16990591](https://zenodo.org/records/16990591)**

We welcome use of these data products in independent analyses. If you're working on something where the AEV data could be useful, feel free to reach out — we're interested in how the index performs in contexts beyond its original development.

<!-- 📸 IMAGE SUGGESTION: Screenshot of the Shiny app showing the layer comparison interface with AEV + KBA + AES layers toggled on -->

### What's Next

The index represents a snapshot in time in terms of the ESM scenarios used. We see several productive directions for future work: incorporating additional predator data layers (particularly for mesopelagic species), updating projections as next-generation ESMs become available, and expanding the framework to sub-regional scales where management decisions require finer resolution.

*Correspondence and collaboration inquiries welcome at [your email or lab contact].*

{% endtab %}

{% tab hotspots 🐧 Fishery Manager / Policy Audience %}

## A New Tool for Antarctic Marine Conservation Planning

*This post summarizes Paper SC-CAMLR-44-BG-26, presented at CCAMLR-44, and the associated publication now available in [Journal Name].*

Managing Antarctica's living marine resources requires making decisions under uncertainty — about where species are, where they'll be in a warming ocean, and which areas are most critical to protect. We've been working for several years to develop science that directly supports that challenge, and this post describes what we've built and how it can be used.

<!-- 📸 IMAGE SUGGESTION: Map of Antarctica with CCAMLR MPA boundaries overlaid on the AEV Index -->

### The Antarctic Ecosystem Value Index

The AEV Index provides spatially explicit assessments of ecosystem value for the coastal waters of Antarctica, with particular attention to the role of polynyas — the open-water systems that drive primary productivity and support krill, fish, and predator populations throughout the Southern Ocean food web.

Crucially, the Index includes **projections to the year 2090**, allowing conservation planners to assess not just where ecological value is concentrated today, but where it will remain, where it will decline, and where new refugia may emerge under climate forcing.

<!-- 📸 IMAGE SUGGESTION: Present vs. 2090 AEV comparison map with MPA boundaries overlaid -->

### Implications for the MPA Network

Three regions with direct relevance to current CCAMLR MPA discussions stand out:

**Antarctic Peninsula**
The northern and southern Peninsula are diverging ecologically. The north is experiencing sea ice loss, with associated declines in krill habitat suitability. The south — including the area encompassed by the proposed Domain 1 MPA — shows greater stability and potential as a climate refugium for krill through the end of the century. The AEV Index provides quantitative support for the ecological rationale underlying the D1MPA proposal.

**Amundsen Sea**
Among the most productive coastal systems in Antarctica — with polynyas generating exceptional primary productivity per square meter — and projected to *increase* in productivity by 2090. There is currently no proposed MPA for this region despite ongoing and increasing pressure from toothfish fisheries. The AEV Index identifies this as a significant gap in the current network.

**Ross Sea**
The AEV Index confirms the high ecological value of the Ross Sea polynya and projects that it will remain productive — or increase in productivity — through the end of the century. This provides independent evidence supporting the long-term effectiveness of the Ross Sea Region MPA ahead of future 10-year reviews.

### A Tool Built for Your Questions

We developed the **Index Comparison Tool** (a Shiny web application) specifically in response to questions raised by CCAMLR delegations over several years of presentations: *How does this index compare to KBAs? To AES? To existing bioregionalizations?*

The tool aggregates all major circumpolar-scale important area analyses and bioregionalizations in one place. You can:

- **Visually compare** any combination of layers — the AEV Index, KBAs, AES, benthic bioregions — on a circumpolar or regional map
- **Calculate quantitatively** how much of any important area or bioregion is captured within any CCAMLR MPA planning domain or existing/proposed MPA
- **Generate summary tables** for use in working group documents or reporting

**[→ Access the Index Comparison Tool](https://saef-monash.shinyapps.io/antarctic_map/)**

<!-- 📸 IMAGE SUGGESTION: Screenshot of the Shiny app summary table for the Ross Sea MPA domain -->

### Example: Ross Sea Planning Domain

When you select the Ross Sea Planning Domain in the tool, it calculates the overlap between all available important area layers and the domain boundary — allowing you to assess, for example, what percentage of the AEV high-value area, the KBA footprint, and the benthic bioregions fall within or outside MPA protection.

For the Ross Sea MPA specifically, the tool shows that the AEV Index is well-represented within the existing MPA boundary — while flagging other layers that are not, which may be relevant for ongoing review processes.

### Open Data

All underlying data are archived in open access repositories and can be downloaded for independent analysis. We encourage working groups to use these tools and data layers directly in their own assessments.

📦 **[Data on Zenodo →](https://zenodo.org/records/16990591)**
🗺️ **[AEV Interactive Map →](https://PLACEHOLDER-TOOL-URL)**
📊 **[Index Comparison Tool →](https://saef-monash.shinyapps.io/antarctic_map/)**

---

*This work was funded by NASA Applied Sciences, Biodiversity and Ecological Forecasting (Grant 80NSSC21K1132) and developed in collaboration with teams at CU Boulder, USGS, University of Canterbury, LOCEAN, and Woods Hole Oceanographic Institution.*

*Questions or requests for working group collaboration: [contact info]*

{% endtab %}

{% endtabs %}

---

### About This Project

The Antarctic Ecosystem Value Index was developed by a team of 12 scientists across 7 institutions as part of a NASA Applied Sciences grant. The work was presented at CCAMLR-44 (October 2025) as Paper SC-CAMLR-44-BG-26.

**Team institutions:** CU Boulder · USGS · University of Canterbury · LOCEAN · Woods Hole Oceanographic Institution · [+ additional institutions]

**Funding:** NASA Applied Sciences, Biodiversity and Ecological Forecasting · Grant 80NSSC21K1132

---

*Found this useful? Share it. The tools are free, the data are open, and the ocean needs all the advocates it can get.*
