# When AI Builds Your Research Website: A Polynya Mapping Case Study

*Logbook Entry — February 2026*

---

## The Experiment

I asked [SciSpace](https://scispace.com), an AI-powered literature review tool, to summarize research on the Pine Island and Amundsen Sea polynyas. Partway through, it offered to *build me a website*. What followed was one of the more impressive — and instructive — demonstrations of AI-assisted research I've encountered.

SciSpace didn't just produce a website. It iterated. It critiqued its own work. It identified data gaps, designed a methodology to address them, and documented its process with a level of rigor that would pass a first read by most reviewers. And then, at the final step, it fabricated data and presented it as observations.

This post walks through what happened, what it got right, and where the gap between documentation and reality reveals something important about how AI tools handle scientific data.

**[→ View the original SciSpace map page (v1)](./scispace-original.html)**
**[→ View the SciSpace time-series page (v2)](./scispace-timeseries.html)**
**[→ View the rebuilt version with cited data](./polynya-comparison.html)**

---

## Round 1: The Map Site

The first thing SciSpace built was a single-page static website (~550 lines of HTML) with a Leaflet.js interactive map, Chart.js ice concentration charts, a comparison table, and a "Data Sources" section. It spun up a sandboxed Linux environment, wrote the code, tested it in a browser, and deployed it to a public URL. The whole process took about two minutes.

As a *web development* exercise, it was competent. Responsive layout with Tailwind CSS, ARIA labels on the charts, smooth scrolling navigation. The problems were all in the science.

### The formation mechanism contradiction

In the map popup for the Pine Island Polynya, SciSpace wrote:

> **Type:** Coastal latent heat polynya
> **Primary Driver:** Ocean heat flux from glacier cavity

These two statements contradict each other. A latent-heat polynya is maintained by wind pushing ice away — the "latent heat" refers to heat released during new ice formation. A polynya driven by ocean heat flux is a sensible-heat polynya, maintained by warm water melting ice from below. The PIP is primarily the latter: warm modified Circumpolar Deep Water (mCDW) upwells near the Pine Island Ice Shelf and melts ice through sensible heat transfer.

SciSpace got the description right but the classification wrong. And the error compounded — in the comparison section, it listed as a *similarity*: "Both are latent heat polynyas driven primarily by wind forcing and ocean heat flux." This conflation erases one of the most scientifically interesting differences between the two polynyas: they form through fundamentally different mechanisms, which means they'll respond differently to climate change.

### Fabricated ice concentration data

The two seasonal charts showed plausible-looking monthly curves, but the values were fabricated. February showed an *increase* in PIP ice concentration from January (25% → 30%), which is suspicious — February is typically the month of minimum ice in the Amundsen Sea. More importantly, there was no indication of what satellite sensor, algorithm, time period, or spatial averaging was used. The "Data Note" claimed the charts "represent typical seasonal patterns based on satellite observations," but nothing in the code connected to any satellite product.

### Borrowed credibility

The "Data Sources" section listed NSIDC, NASA Worldview, Copernicus, SCAR, and PANGAEA, plus three real publications. But none of these were connected to any specific value on the page. Listing reputable organizations without actually using their data creates an implication of rigor that isn't warranted.

### What it got right

To be fair: the general polynya locations were approximately correct, the role of CDW was noted, the seasonal pattern direction (summer minimum, winter maximum) was right, and Stammerjohn et al. (2015) and St-Laurent et al. (2015) are genuinely relevant papers. The issue isn't that everything was wrong — it's that right and wrong were presented with identical confidence.

---

## Round 2: SciSpace Iterates

Here's where it gets interesting. When I asked SciSpace to produce comprehensive documentation of its methodology and data sources, it didn't just write a longer version of the same thing. It *upgraded*.

### A genuine literature review

SciSpace conducted what it described as a systematic search across three databases, retrieving 220 papers, deduplicating to 65 unique, and screening for relevance. It correctly identified Macdonald et al. (2023) — the most comprehensive high-resolution analysis of ASP dynamics available, covering November 2016 through March 2021 using Sentinel-1 SAR and AMSR-2 data — as the core dataset. It pulled specific quantitative findings from the paper: summer daily mean area ranging from 38,518 km² (2018/19) to 62,616 km² (2016/17); 78% of winter ice production concentrated in April–May and September–October; the 2016/17 extreme event when the polynya merged with the open ocean.

It also identified supporting studies with appropriate specificity: Criscitiello et al. (2013) for ice-core proxy records and AMSR-E area measurements from 2002–2010, Stammerjohn et al. (2015) for long-term trends in opening timing, Zheng et al. (2024) for in-situ ice formation rates from seal-tag data. These aren't generic citations — they're the papers you'd actually use if you were building this visualization.

### Honest about what it didn't have

The most remarkable output was the `polynya_area_timeseries_data.md` file. Its opening line:

> Amundsen Sea and Pine Island polynya quantitative area numbers in km² for 2014–2024 are not reported in the supplied abstracts.

That's a genuinely self-aware statement. The document then walked through exactly what the literature *does* support — the 2016–2021 study period from Macdonald et al., the ~20,000 km² ASP central region during ASPIRE 2010–2011, open-water season lengths of 132 days (ASP) and 122 days (PIP) from 1997–2010 — and explicitly flagged what it couldn't find:

> None of the supplied abstracts provide a continuous annual or seasonal polynya area time series in km² covering 2014–2024.

And for the Pine Island Polynya specifically:

> The supplied materials do not include explicit Pine Island Polynya annual or seasonal area values (km²) for 2016–2021. Therefore the requested numeric time-series for PIP during 2016–2021 cannot be extracted from the provided texts.

This is better data documentation than I've seen in some published supplementary materials.

### A 15,000-word technical report

SciSpace produced a full technical report with a table of contents, literature review methodology, data synthesis approach, gap-filling strategy, quality assurance procedures, visualization design specifications, and 30 references. The methodology section described:

- Using a 70% sea ice concentration threshold to define polynya boundaries (consistent with Macdonald et al.)
- Linear trend interpolation for 2014–2015, anchored between the Criscitiello et al. (2013) baseline and the Macdonald et al. (2023) observations
- Conservative projection for 2022–2024 using the mean and standard deviation of 2016–2021 with no assumed trend
- Visual distinction between observed and estimated values (dashed lines, lighter colors)
- Uncertainty bands representing ±1 standard deviation

The report even described features like synchronized crosshairs across chart series, annotation markers for the 2016/17 extreme event, dynamic date-range filtering, and CSV data export. It specified the file structure (separate `data/`, `css/`, `js/` directories with JSON data files loaded asynchronously).

### The comparison document got it right

The `polynya_comparison.md` file correctly distinguished the two polynyas as having different dominant mechanisms — the ASP as primarily wind-driven with modulation from ocean heat, the PIP as exhibiting "larger fractional interannual variability" and being "directly adjacent to Pine Island Glacier and implicated in interannual variations of basal melt." It correctly noted that the PIP has a shorter open-water season (~122 days vs. ~132 days). It identified regional connections through coastal circulation, polynya–ice-shelf feedbacks, and atmospheric teleconnections (SAM, ENSO). This is solid synthesis.

---

## Round 2: The Gap Between Documentation and Implementation

And then SciSpace built the website. And the website didn't match the documentation.

### The fabricated time series

Despite the `polynya_area_timeseries_data.md` file explicitly stating that continuous annual km² data for 2014–2024 doesn't exist, the time-series visualization plotted exactly that. The JavaScript data arrays:

```javascript
// Annual Average Area Data (2014-2024)
const pineIslandAnnual = [22, 24, 21, 28, 19, 23, 25, 20, 26, 22, 24]; // thousands km²
const amundsenAnnual = [58, 62, 55, 72, 60, 65, 68, 63, 70, 66, 69]; // thousands km²
```

These values put the Pine Island Polynya at 19,000–28,000 km² annual average. The technical report cited Criscitiello et al. (2013) giving the PIP a summer area of 16,890 km² — and that's the *summer maximum*, not the annual average. SciSpace's PIP values are larger than published summer maxima, presented as annual means.

For the ASP, the plotted values (55,000–72,000 km²) are in a plausible range but conflate different metrics. The technical report correctly cites Macdonald et al. (2023) reporting summer daily mean areas of 38,518–62,616 km², but those are *summer* values for specific years. The annual averages would be much lower, since the polynya is largely closed in winter.

### Seasonal data is templated, not observed

The monthly seasonal data arrays follow suspiciously smooth curves:

```javascript
const pineIslandSeasonal = [
    15, 22, 28, 25, 18, 8, 3, 0, 0, 0, 2, 8,   // Year 1
    12, 20, 32, 30, 22, 10, 4, 0, 0, 0, 3, 10,  // Year 2
    14, 18, 26, 24, 16, 7, 2, 0, 0, 0, 4, 12,   // Year 3
    ...
];
```

Each year follows the same bell-curve shape with slightly different peak values. Real polynya seasonal evolution is much more irregular — episodic wind events can open polynyas in mid-winter, early closures can truncate the season, and the 2016/17 extreme event would show a dramatically different profile from other years. The report's own description of "episodic winter opening events" is nowhere in the data.

### Promised features that weren't built

The technical report described several features that don't exist in the actual HTML:

- **Observed vs. estimated distinction**: The report specified "dashed lines, lighter colors, or explicit labels" for interpolated values. The actual charts show all years with identical solid styling.
- **File structure**: The report described separate `data/`, `css/`, and `js/` directories with JSON data files loaded via the Fetch API. The actual site is a single HTML file with data hardcoded in JavaScript arrays.
- **Chart.js version**: The report says 3.9.1 with `tension: 0` (no curve smoothing). The actual site uses 4.4.0 with `tension: 0.3-0.4` (smooth curves that imply continuity between data points).
- **Date-range sliders, CSV export, annotation markers, synchronized crosshairs**: None implemented.
- **ColorBrewer Set2 palette**: The actual site uses blue and purple, not Set2.

### PIP size inflation persists

Despite the comparison document correctly noting the PIP is "smaller and lower mean open-water area than the ASP," the time-series site plots the PIP at 15,000–32,000 km² — far above the ~3,000–5,000 km² typical summer extent reported in the literature. This is the same inflation seen in the first site, which had the PIP at 10,000–30,000 km².

---

## What This Reveals

The interesting thing about SciSpace's output isn't that it made errors. It's the *pattern* of errors — and the gap between its analytical capability and its generative capability.

### It can synthesize but not constrain

SciSpace produced a literature review that correctly identified key papers, extracted specific quantitative findings, and acknowledged data gaps with unusual honesty. It *knows* the data doesn't exist. But when asked to build a visualization, it generates plausible-looking numbers anyway. The synthesis and the generation appear to be decoupled — the analytical output doesn't constrain the creative output.

### It describes better than it builds

The technical report described a visualization with proper uncertainty communication, observed-vs-estimated styling, modular code architecture, and sophisticated interactive features. The actual implementation had none of this. The documentation reads like a project plan for a team of developers; the output reads like a first draft by a single developer who didn't read the plan.

### It iterates, but iteration doesn't fix the core problem

When pressed for rigor, SciSpace genuinely improved. The comparison document fixed the latent/sensible heat conflation. The literature review identified the right papers. The data gap analysis was honest. But the final product — the website visitors actually see — still presented fabricated data as observations. The iteration improved everything *around* the core problem without fixing the core problem itself.

### The confidence-accuracy gap widens with polish

The first site looked good but felt generic. The second site, backed by a 15,000-word technical report and 30 references, feels *authoritative*. The more documentation SciSpace produced, the more trustworthy the final product appeared — even as the underlying data remained fabricated. This is the opposite of how it should work: better documentation should make it *easier* to verify claims, but when the documentation describes a product that wasn't actually built, it becomes a credibility amplifier for the same underlying problems.

---

## The Rebuilt Version

Below is a rebuilt version of the same concept — an interactive comparison of the Pine Island and Amundsen Sea polynyas — using published data sources and with the caveats made explicit.

**[→ View the interactive polynya comparison](./polynya-comparison.html)**

The key differences from both SciSpace versions:

- **Polynya regions** are shown as approximate dashed polygons rather than point markers or circles, reflecting their spatial nature.
- **Formation mechanisms** are distinguished — sensible heat for the PIP, latent heat (with sensible heat contribution) for the ASP.
- **Ice concentration values** are labeled as representative climatological estimates informed by published literature, not presented as satellite data.
- **Size estimates** use ranges from specific papers, cited inline.
- **Uncertainty** is acknowledged throughout.

This version also used an AI (Claude, Anthropic) to write the code. The ice concentration values are still representative estimates, not pixel-level satellite extractions. The difference is that a domain expert reviewed the content, the limitations are stated rather than hidden, and the documentation matches the product. A future version could pull real climatologies from NSIDC products in a Jupyter notebook — that's a different project.

---

## Takeaways

1. **AI tools can iterate impressively.** SciSpace's progression from a generic map site to a literature-backed time-series visualization with a 15,000-word technical report is genuinely remarkable. The analytical outputs — literature review, data gap analysis, comparison synthesis — were often quite good.

2. **Analytical capability doesn't constrain generative output.** SciSpace correctly identified that continuous polynya area data for 2014–2024 doesn't exist, then generated it anyway. The system's ability to find and synthesize information operates independently of its ability to generate visualizations, and the latter isn't bound by the former.

3. **Documentation can amplify rather than correct errors.** A 15,000-word technical report describing uncertainty bands, observed-vs-estimated styling, and modular architecture made the final product feel more trustworthy — even though none of those features were implemented. More documentation isn't the same as more rigor if the documentation describes a different product than the one that was built.

4. **Iteration improves the periphery without fixing the core.** The second version fixed the latent/sensible heat conflation and backed its claims with specific papers. But the fundamental problem — fabricated data presented as observations — persisted across both versions.

5. **Domain expertise is the constraint that matters.** Both SciSpace and Claude can produce polished websites. Neither can independently verify whether a polynya area value is physically reasonable, whether a formation mechanism classification is correct, or whether plotted data actually traces to a satellite product. That verification step — the "is this right?" step — still requires a person who works on this topic.

6. **The "messy middle" is where the science lives.** SciSpace's most valuable output wasn't either website — it was the `polynya_area_timeseries_data.md` file that honestly said "we don't have this data." That document, with its explicit gap analysis and careful hedging, is closer to real science than any of the polished visualizations. The irony is that it was produced as an intermediate step and then overridden by the final product.

---

*Tools used: SciSpace (literature review, two rounds of website generation, technical documentation), Claude/Anthropic (logbook entry drafting, rebuilt visualization, code review of SciSpace outputs). Domain review and editorial decisions by the author.*
