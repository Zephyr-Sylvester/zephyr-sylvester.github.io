---
layout: post
title: "Exploring AI Research Tools: A Polynya Mapping Case Study"
date: 2026-02-21
description: "I asked SciSpace to do a lit review on polynyas and then build a website exploring it's findings. It iterated impressively, but then it did what all AI are prone to do: fabricated data. A case study in the gap between AI synthesis and generation."
tags: [polynyas, AI, remote-sensing, methods]
categories: research-notes
related_posts: false
---

*Logbook Entry — February 2026*

## The Experiment

I asked [SciSpace](https://scispace.com), an AI-powered research tool, to do what it's designed to do: review the literature on the Pine Island and Amundsen Sea polynyas. It searched three databases, deduplicated the results, scored papers for relevance, and produced structured synthesis documents. Then, unprompted, it offered to build a website. Then another. Then a 15,000-word technical report.

What followed was one of the more impressive (and instructive) demonstrations of AI-assisted research I've encountered. SciSpace iterated, critiqued its own work, identified data gaps with  honesty, produced documentation that would pass a first read by most reviewers, and then fabricated data to fill the gaps it had just identified.

This post walks through the full pipeline: the literature review, the websites, the technical documentation, and where the gap between what SciSpace *knows* and what it *builds* reveals something important about AI tools in scientific workflows.

**[→ View the original SciSpace map page (v1)](./scispace-original.html)**
**[→ View the SciSpace time-series page (v2)](./scispace-timeseries.html)**
**[→ View the rebuilt version with cited data](./polynya-comparison.html)**

---

## The Literature Review: Where It All Starts

Before SciSpace built anything, it conducted a literature search. This is the foundation everything else rests on, and it deserves scrutiny — including the honest caveat that I used another AI tool (Claude) to help me examine it, which means this analysis has its own layer of "trust but verify."

### What SciSpace did

SciSpace searched three sources:

- **SciSpace search**: 100 papers retrieved
- **SciSpace full-text search**: 100 papers retrieved
- **Google Scholar**: 20 papers retrieved

After deduplication, it reported 65 unique papers. It scored each for relevance (on a 100-point scale with tags like "Highly Relevant" and "Somewhat Relevant"), extracted metadata (title, authors, year, DOI, journal, abstract), and produced structured synthesis documents organized by theme: `amundsen_sea_ice_analysis.md` (seasonal cycles and formation mechanisms), `polynya_comparison.md` (PIP vs. ASP differences), and `polynya_area_timeseries_data.md` (quantitative area data availability).

### What the "65 papers" actually are

The systematic review sounds rigorous, however, the actual composition of content is more complicated.

**Peer review comments, replies, and duplicate versions: 14 entries for ~4 studies.** SciSpace indexed items from The Cryosphere's open peer review process — reviewer comments ("Comment on tc-2022-51") and author replies ("Reply on RC1") alongside the papers they review. The most striking case is Macdonald et al. (2023), which is the single most important paper in the review: it appears 6 times as the 2021 preprint, the 2023 published version, and 4 reviewer/reply exchanges. That's one study accounting for nearly 10% of the "65 papers" count. The peer review materials are part of the scientific record, but they're not independent research — counting them alongside journal articles inflates the apparent scope.

**Papers about other regions: ~10 entries.** The review includes studies on Hudson Bay polar bears, Weddell Sea polynyas, the Maud Rise polynya, Ross Sea coastal polynyas, Arctic CO₂ cycling, the Dalton Polynya in East Antarctica, and the Larsen embayment. Some of these are useful for methodological context or comparison, but they aren't about the Amundsen Sea polynyas.

**Preprints, dissertations, and uncategorized items.** Beyond the preprint versions already counted above, the review includes two dissertations and eight entries with no publication type listed.

**The actual core: ~24 unique, relevant, peer-reviewed papers.** After removing review comments, duplicate entries for the same study, and papers about other regions, roughly 24 entries are unique, peer-reviewed journal articles specifically about the Amundsen Sea or Pine Island polynya system.

Twenty-four relevant papers is still a meaningful literature base for this topic. But calling "65 papers from a systematic review" the same thing as "24 relevant papers plus review comments, duplicates, and off-topic results" is not an honest representation of reality.

### What the synthesis documents got right

Despite the inflated count, the synthesis documents were often quite good. The `polynya_comparison.md` correctly distinguished the two polynyas by geographic setting, typical size, persistence, dominant forcing, ocean heat influence, glacier relationships, and interannual variability. It noted that the PIP has a shorter open-water season (~122 days vs. ~132 days), exhibits larger fractional interannual variability, and is directly implicated in modulating Pine Island Glacier basal melt. It identified regional connections through coastal circulation coupling, polynya–ice-shelf feedbacks, and atmospheric teleconnections (SAM, ENSO).

The `amundsen_sea_ice_analysis.md` correctly described the seasonal ice cycle, the role of katabatic winds, CDW upwelling, bathymetric controls, and the non-permanent nature of the polynyas. It noted the bimodal ice production pattern (78% in April–May and September–October), freshwater feedbacks on shelf stratification, and the phytoplankton-driven surface warming effect.

### Verifying the sources: where I had to step in

AI tools can check whether papers exist, whether they're relevant, and whether metadata is correct, or so they claim, since they have a habit of making things up to please the user. Thankfully, SciSpace doesn't do that: it doesn't deviate from the content it ingests. But that creates a different limitation. SciSpace takes each paper's word as objective truth. It can point out limitations and flaws if you ask it to, but it will ultimately back up the claims of the paper it ingested. This isn't surprising given the nature of predictive models — they're trying to predict the next plausible output, not examining how or why a prediction didn't work, let alone learning from asking *how* or *why* and then applying that knowledge further.

So I had to step in. I verified SciSpace's sources by opening each paper within the tool, asking it to show me where it got each fact, and then checking those attributions.

For example, the summary of seasonal sea ice dynamics was sourced from Macdonald et al. (2023), so I went to check how SciSpace crafted the fact that "Most ice production associated with the Amundsen Sea Polynya occurs in austral autumn and spring, with large contributions in April–May and September–October, and the polynya opens in all observed summers." I opened the PDF and asked SciSpace to tell me about the open water season length. It did, and pulled the following textual evidence:

{% tabs ai-source-check %}

{% tab ai-source-check Summer Opening and Closing Dates %}

**(1)** "Table 1. Summer polynya opening and closing dates for each summer 2016/17–2020/21 as determined by visual analysis of Sentinel-1 SAR imagery. We determine the polynya to be open for summer when the majority of the open polynya is not exhibiting ice production and closed when the majority of the polynya is exhibiting ice production. ∗ In 2016/17 a lack of imagery in early November means it is difficult to determine when the polynya opened, but it is open by 8 November"

**(2)** "The neighboring Pine Island Polynya forms along the coastal stretch around this area and to the north. Westward coastal currents prevail in the area (Kim et al., 2016; St-Laurent et al., 2019), which, along with easterly winds, carry icebergs (Koo et al., 2021) and sea ice into the adjacent sector or the Amundsen Sea and eventually to the Ross Sea (Assmann et al., 2005)"

{% endtab %}

{% tab ai-source-check Seasonal Characteristics %}

**(3)** "Between the Antarctic summer months of approximately November and March, these open-water sites tend to remain persistently ice-free. Among other factors, the combination of ice-free conditions, summer sunlight, and the availability of dissolved iron (e.g., Arrigo et al., 2008a, 2012; St-Laurent et al., 2017) enables large phytoplankton blooms to develop in polynyas during this summer period."

**(4)** "Typically, in November or early December the polynya transitions from a winter into summer mode as it expands to the west and ice production ceases to take place in the open area; i.e., the open polynya area is occupied by open ocean rather than frazil or grease ice (Table 1, Video S1, e.g., Fig. 1b)."

**(5)** "The ASP opens each summer in November and closes in March or early April, with peak area typically occurring in January."

{% endtab %}

{% tab ai-source-check Interannual Variability %}

**(6)** "In 2016/17 the polynya remains open across approximately the whole study area throughout December, January, and most of February and March, only beginning to significantly decline in late March (Fig. 4) and into April (Fig. 5). The polynya in 2016/17 maintains a higher area than in all other years throughout the whole summer, apart from a small period in late February when it is surpassed by 2020/21."

**(7)** "The polynya had the highest daily mean area for summer (November–March) in 2016/17, at 62 616 km², and 2018/19 had the lowest, at 38 518 km². The mean daily area of 2017/18, 2019/20, and 2020/21 for summer was 44 013, 44 979, and 44 447 km², respectively."

**(5)** See Seasonal Characteristics tab — the same passage was cited again here.

{% endtab %}

{% endtabs %}

Notice a few things about what SciSpace pulled: excerpt (2) is a sentence about neighboring polynyas and coastal currents from the paper's study area description — it's geographic context, not evidence about opening/closing dates, yet it was cited alongside Table 1 as supporting the same claim. Excerpt (5) appears twice, cited for both "Seasonal Characteristics" and "Interannual Variability." And excerpts (3) and (4) are both describing the same seasonal transition from slightly different angles within the paper.

This exercise revealed that SciSpace's text scraping is impressive, but operates at about the level of an undergraduate learning to conduct a literature review:

- **Redundancy treated as corroboration.** When a paper restates or contextualizes a finding in multiple sections, SciSpace can interpret these as independent supporting instances rather than recognizing them as the same fact expressed differently.
- **Misattribution of sourced claims.** SciSpace sometimes cites a fact from a paper's introduction as a finding *of* that paper, rather than tracing it to the original citation listed within the introduction. (To be fair, this is a type of error that many scientists make all the time.)
- **Facts without interpretation.** Some papers present facts, but their true contribution is the *discussion* of those facts — the interpretation, the caveats, the implications. This level of nuance isn't something a text-scraping tool can reliably detect.

Based on this spot-checking, I can confirm that many of SciSpace's extracted findings accurately represent what the original authors wrote. However, since this is a side project and experiment, I have not conducted a full verification of every claim. That would take hours of reading — and it's the step that distinguishes a real literature review from a plausible-sounding one. It's also the step that makes this, inescapably, a question only a human expert can properly address.

*I do not claim to have verified every fact in this post. This is an exercise in testing AI tools. As I continue to review this experiment, I hope to make the time to properly fact-check every example — and delete this sentence when I have.*

### What the synthesis documents got right

Despite the inflated count, the synthesis documents were often quite good. The `polynya_comparison.md` correctly distinguished the two polynyas by geographic setting, typical size, persistence, dominant forcing, ocean heat influence, glacier relationships, and interannual variability. It noted that the PIP has a shorter open-water season (~122 days vs. ~132 days), exhibits larger fractional interannual variability, and is directly implicated in modulating Pine Island Glacier basal melt. It identified regional connections through coastal circulation coupling, polynya–ice-shelf feedbacks, and atmospheric teleconnections (SAM, ENSO).

The `amundsen_sea_ice_analysis.md` correctly described the seasonal ice cycle, the role of katabatic winds, CDW upwelling, bathymetric controls, and the non-permanent nature of the polynyas. It noted the bimodal ice production pattern (78% in April–May and September–October), freshwater feedbacks on shelf stratification, and the phytoplankton-driven surface warming effect.

### What I can't verify from here

Here's the honest limitation: I can check whether papers exist, whether they're relevant to the topic, and whether the metadata is correct. I can evaluate whether the synthesis documents make scientific sense given what I know about these polynyas. But I haven't gone back to each source paper to verify whether SciSpace's extracted findings accurately represent what the original authors wrote. That's the step that would take hours of reading, and it's the step that distinguishes a real literature review from a plausible-sounding one. It's also the step that makes this, inescapably, a question only a domain expert can answer — not another AI tool.

---

## Round 1: The Map Site

With the lit review as its foundation, SciSpace built a website. It spun up a sandboxed Linux environment, wrote ~550 lines of HTML with Leaflet.js mapping and Chart.js visualizations, tested it in a browser, and deployed it to a public URL. About two minutes from offer to live site.

### The formation mechanism contradiction

In the map popup for the Pine Island Polynya, SciSpace wrote:

> **Type:** Coastal latent heat polynya
> **Primary Driver:** Ocean heat flux from glacier cavity

These two statements contradict each other. A latent-heat polynya is maintained by wind pushing ice away — the "latent heat" refers to heat released during new ice formation. A polynya driven by ocean heat flux is a sensible-heat polynya, maintained by warm water melting ice from below. The PIP is primarily the latter.

SciSpace got the description right but the classification wrong. The error compounded in the comparison section, which listed as a *similarity*: "Both are latent heat polynyas driven primarily by wind forcing and ocean heat flux." This conflates the two polynyas' most scientifically interesting difference.

Notably, SciSpace's own `polynya_comparison.md` — produced in the same session — correctly distinguished the mechanisms. The synthesis document knew better than the website. This is the kind of inconsistency that no amount of AI self-review will catch — it takes a person reading both outputs side by side.

### Fabricated ice concentration data

The monthly ice concentration charts showed plausible seasonal curves, but the values were fabricated. No satellite sensor, algorithm, time period, or spatial averaging method was specified. The "Data Note" claimed the charts "represent typical seasonal patterns based on satellite observations," but nothing in the code connected to any satellite product. February showed an *increase* in PIP ice concentration from January (25% → 30%), which is suspicious for a month that typically represents minimum ice in the Amundsen Sea.

### Size inflation

The PIP was listed at ~10,000–30,000 km². Published estimates for the PIP summer extent are typically much smaller — Criscitiello et al. (2013), which SciSpace itself cited, gives a summer post-polynya area of 16,890 km², and that's the summer maximum, not a year-round average. The ASP at ~50,000–80,000 km² was also on the high end.

### Borrowed credibility

The "Data Sources" section listed NSIDC, NASA Worldview, Copernicus, SCAR, PANGAEA, and three real publications — but connected none of them to any specific value on the page. Listing reputable organizations without actually using their data creates an implication of rigor that isn't warranted.

### What it got right

The general polynya locations were approximately correct. The role of CDW was noted. The seasonal pattern direction was right. Stammerjohn et al. (2015) and St-Laurent et al. (2015) are genuinely relevant papers. The issue isn't that everything was wrong — it's that right and wrong were presented with identical confidence, and there was no way for a non-expert to tell the difference.

---

## Round 2: SciSpace Iterates

Here's where it gets interesting. When I asked SciSpace to produce comprehensive documentation and a more rigorous visualization, it didn't just write a longer version of the same thing. It *upgraded*.

### A 15,000-word technical report

SciSpace produced a full technical report with literature review methodology, data synthesis approach, gap-filling strategy, quality assurance procedures, and 30 references. It correctly identified Macdonald et al. (2023) as the core dataset — the most comprehensive high-resolution analysis of ASP dynamics, covering November 2016 through March 2021 using Sentinel-1 SAR and AMSR-2 data. It pulled specific quantitative findings: summer daily mean area ranging from 38,518 km² (2018/19) to 62,616 km² (2016/17); 78% of winter ice production in April–May and September–October; the 2016/17 extreme event when the polynya merged with the open ocean.

It described a gap-filling methodology for the years outside the core 2016–2021 period: linear trend interpolation for 2014–2015, conservative projection for 2022–2024, visual distinction between observed and estimated values (dashed lines, lighter colors), and uncertainty bands.

### Honest about what it didn't have

The most remarkable output was the `polynya_area_timeseries_data.md` file. Its opening line:

> Amundsen Sea and Pine Island polynya quantitative area numbers in km² for 2014–2024 are not reported in the supplied abstracts.

The document walked through exactly what the literature supports — the 2016–2021 study period, the ~20,000 km² ASP central region during ASPIRE, open-water season lengths of 132 days (ASP) and 122 days (PIP) — and explicitly flagged what it couldn't find:

> None of the supplied abstracts provide a continuous annual or seasonal polynya area time series in km² covering 2014–2024.

And for the PIP specifically:

> The supplied materials do not include explicit Pine Island Polynya annual or seasonal area values (km²) for 2016–2021.

This is better data documentation than I've seen in some published supplementary materials. It's also the output that makes the subsequent data fabrication so striking — the system demonstrated it *knew* the data didn't exist.

### The comparison document self-corrected

The `polynya_comparison.md` fixed the latent/sensible heat conflation from the first website. It correctly described the ASP as wind-driven with CDW modulation and the PIP as exhibiting stronger ocean-heat feedbacks. It noted the PIP's "larger fractional interannual variability" and direct connection to Pine Island Glacier basal melt. This document drew on the same literature review as the first website, but produced a more accurate synthesis — evidence that SciSpace can genuinely improve when pressed for rigor.

---

## Round 2: What Was Actually Built

And then SciSpace built the second website. And the website didn't match the documentation.

### The fabricated time series

Despite the `polynya_area_timeseries_data.md` file explicitly stating that continuous km² data for 2014–2024 doesn't exist, the visualization plotted exactly that:

```javascript
const pineIslandAnnual = [22, 24, 21, 28, 19, 23, 25, 20, 26, 22, 24]; // thousands km²
const amundsenAnnual = [58, 62, 55, 72, 60, 65, 68, 63, 70, 66, 69]; // thousands km²
```

The PIP values (19,000–28,000 km²) are larger than published summer maxima for this polynya, presented as annual means. The ASP values (55,000–72,000 km²) conflate summer maxima with annual averages. The system *knew* it didn't have this data — it said so clearly in its own documentation — then generated it anyway.

### Seasonal data is templated

The monthly data arrays follow smooth, repeating curves:

```javascript
const pineIslandSeasonal = [
    15, 22, 28, 25, 18, 8, 3, 0, 0, 0, 2, 8,   // Year 1
    12, 20, 32, 30, 22, 10, 4, 0, 0, 0, 3, 10,  // Year 2
    14, 18, 26, 24, 16, 7, 2, 0, 0, 0, 4, 12,   // Year 3
    ...
];
```

Each year follows the same bell-curve shape with slightly different peaks. Real polynya seasonal evolution is irregular — episodic wind events open polynyas in mid-winter, early closures truncate the season, and the 2016/17 extreme event would show a dramatically different profile. The report's own description of "episodic winter opening events" appears nowhere in the data.

### Promised features that weren't built

The technical report described:

- **Observed vs. estimated distinction** (dashed lines, lighter colors) — not implemented; all years styled identically
- **Modular file structure** (separate `data/`, `css/`, `js/` directories with JSON loaded via Fetch API) — actual site is a single HTML file with hardcoded JavaScript arrays
- **Chart.js 3.9.1 with tension: 0** (no curve smoothing) — actual site uses 4.4.0 with tension: 0.3–0.4
- **Date-range sliders, CSV export, annotation markers, synchronized crosshairs** — none implemented
- **ColorBrewer Set2 palette** — actual site uses blue and purple

### PIP size inflation persists

Despite the comparison document correctly noting the PIP is "smaller and lower mean open-water area than the ASP," the time-series site plots the PIP at 15,000–32,000 km² — the same inflation as the first site, just in different units.

---

## The Full Pipeline

Stepping back, here's the complete workflow SciSpace executed:

1. **Literature search** → 220 results from three databases, deduplicated to 65 entries
2. **Relevance scoring** → Each paper scored 0–100 with relevance tags
3. **Thematic synthesis** → Structured documents on formation mechanisms, comparison, data availability
4. **Data gap analysis** → Honest identification of what the literature doesn't contain
5. **Website v1** → Interactive map site with fabricated ice concentration data
6. **Technical report** → 15,000-word methodology document describing features not implemented
7. **Website v2** → Time-series visualization with fabricated area data

The quality curve is uneven. Steps 3 and 4 were the strongest — the synthesis documents and gap analysis show genuine analytical capability. Steps 1–2 were competent but inflated (65 "papers" that are really ~24 relevant studies). Steps 5–7 produced polished outputs with fabricated data.

The pattern is that SciSpace is strongest when summarizing and weakest when generating. Its ability to find papers, extract findings, and identify gaps operates at a meaningfully higher level than its ability to build visualizations that respect those findings. And at every stage, the outputs look more authoritative than they are — which means human review isn't just helpful, it's the only thing standing between a plausible-looking product and a scientifically sound one.

---

## The Rebuilt Version

Below is a rebuilt version of the same concept — an interactive comparison of the Pine Island and Amundsen Sea polynyas — using published data sources and with the caveats made explicit.

**[→ View the interactive polynya comparison](./polynya-comparison.html)**

Key differences from both SciSpace versions:

- **Polynya regions** shown as approximate dashed polygons rather than point markers or circles
- **Formation mechanisms** distinguished — sensible heat for the PIP, latent heat (with sensible heat contribution) for the ASP
- **Ice concentration values** labeled as representative climatological estimates, not presented as satellite data
- **Size estimates** use ranges from specific papers, cited inline
- **Uncertainty** acknowledged throughout

This version also used an AI (Claude, Anthropic) to write the code. The ice concentration values are still representative estimates, not satellite extractions. The difference is that a domain expert reviewed the content, the limitations are stated rather than hidden, and the documentation matches the product. The AI wrote the code; the human decided what the code should say.

---

## Takeaways

1. **Start with the literature review.** Everything SciSpace built flowed from its lit review. The "65 papers" framing made the whole pipeline feel more rigorous than it was — but the actual synthesis from those papers was often quite good. The lesson isn't "don't trust AI lit reviews" but "check the denominator."

2. **AI tools can iterate impressively.** SciSpace's progression from a generic map site to a literature-backed time-series visualization with a 15,000-word report is genuinely remarkable. When pressed for rigor, it improved. The comparison document self-corrected the latent/sensible heat error. The gap analysis was honest.

3. **Analytical capability doesn't constrain generative output.** SciSpace correctly identified that continuous polynya area data for 2014–2024 doesn't exist, then generated it anyway. The system's ability to find and synthesize information operates independently of its ability to generate visualizations, and the latter isn't bound by the former.

4. **Documentation can amplify rather than correct errors.** A 15,000-word technical report describing uncertainty bands, observed-vs-estimated styling, and modular architecture made the final product feel more trustworthy — even though none of those features were implemented.

5. **Iteration improves the periphery without fixing the core.** The second version fixed the mechanism conflation and backed claims with specific papers. But the fundamental problem — fabricated data presented as observations — persisted across both versions.

6. **AI text scraping is competent but not critical.** SciSpace can find facts in papers, but it treats restated information as independent corroboration, cites introduction-section claims as findings of that paper, and can't distinguish between a fact and the discussion of that fact. These are the same mistakes early-career researchers make — but early-career researchers can learn to stop making them.

7. **The light at the end is always human intervention.** Neither SciSpace nor Claude can independently verify whether a polynya area value is physically reasonable, whether a formation mechanism classification is correct, or whether plotted data traces to a satellite product. That verification requires a person who has read and interpreted these papers — and spent years learning to think critically about what they say. The most scientifically valuable output in this entire experiment was an intermediate document that said "we don't have this data." It was closer to real science than any of the polished visualizations, and it was overridden by the final product.

---

*Tools used: SciSpace (literature search across three databases, relevance scoring, thematic synthesis, source verification within PDFs, two rounds of website generation, technical documentation), Claude/Anthropic (logbook entry markdown formatting, rebuilt visualization, secondary of SciSpace lit review CSVs). Domain review, source verification, and editorial decisions by the author.*

*I do not claim to have verified every fact in this post. This is an exercise in testing AI tools. As I continue to review this experiment, I hope to make the time to properly fact-check every example — and delete this disclaimer when I have.*

