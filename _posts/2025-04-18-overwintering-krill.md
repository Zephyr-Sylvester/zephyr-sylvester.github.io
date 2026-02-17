---
layout: post
title: "Untangling how Antarctic krill survive the winter — and what climate change means for their future"
date: 2025-04-18
description: "A qualitative network model reveals habitat-specific winners and losers as sea ice declines."
tags: [antarctica, krill, sea-ice, recruitment, climate-change, southern-ocean]
categories: publications
related_posts: false
---

Antarctic krill are small. About the size of your pinky finger. But they hold up an entire ocean.

Every penguin, seal, whale, and seabird in the Southern Ocean depends — directly or indirectly — on *Euphausia superba*. And every krill alive today survived something remarkably precarious: their first winter.

Our paper, published in *ICES Journal of Marine Science* in April 2025, takes a close look at that survival challenge — and at what happens to it as the ocean warms and sea ice disappears.

> Sylvester, Z., et al. (2025). Untangling larval Antarctic krill overwinter survival under climate change using a qualitative network model. *ICES Journal of Marine Science*. [https://doi.org/10.1093/icesjms/fsaf049](https://doi.org/10.1093/icesjms/fsaf049)

---

### The short version

Winters with extensive sea ice have long been linked to strong krill recruitment the following spring. But *why*? Sea ice does a lot of things at once — it provides food (ice algae), shelter from predators (in ice terraces and under-ice habitat), and physical structure that shapes the water column. Untangling which of these mechanisms matters most, and how their loss will affect larval survival differently in different habitats, is exactly what this paper attempts.

We used a **qualitative network model (QNM)** — a framework that lets you integrate both well-established and hypothesized ecological interactions and test what the system predicts under different scenarios, even when you don't have the quantitative data to parameterize a full simulation model.

<div class="row justify-content-sm-center mt-4">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/untangling-infographic.jpg" title="Untangling krill overwinter survival — infographic" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The full story in one image. See below for a guided walk-through of each piece.
</div>

The headline findings:

- **The northern Antarctic Peninsula continental shelf is most at risk.** Reduced autumn primary productivity and warming temperatures under future climate scenarios drive substantial declines in larval survival in this habitat.
- **Open-ocean habitats may see improved survival under cooler scenarios** — where sea-ice-associated processes like food availability and under-ice refuge remain intact.
- **Hypothesized mechanisms matter.** Including sea-ice terraces as potential predation refuges in the model *strengthened* the projected declines — suggesting that the loss of ice structure may matter as much as the loss of ice algae.
- **Glacial melt is an unresolved uncertainty.** Its influence on food web dynamics emerged as a critical knowledge gap that future field and lab work should target.

---

### Want to go deeper?

The rest of this post walks through the paper's logic in more detail — the biology, the model structure, and what the results mean for each habitat. I've broken it into sections so you can read as much or as little as you want.

---

## Why winter is the bottleneck

Circumpolar krill populations grow each year through the recruitment of the previous year's juvenile class. Four things shape how many juveniles make it into the adult population: spawning success and larval development in spring and summer, how well-prepared krill are heading into winter, and — the focus of this paper — how many larvae actually survive it.

<div class="row justify-content-sm-center mt-3">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/seasonal-cycles-overwintering-ZTS.png" title="Krill seasonal population dynamics" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Krill population dynamics: circumpolar krill populations increase each year through the recruitment of the previous year's juvenile class.
</div>

Winter in the Southern Ocean is brutal for anything small and hungry. With little to no sunlight, primary productivity essentially shuts down — and with it, the food web that krill depend on.

Adult krill have a strategy for this: they spend autumn eating as much as they can, building up lipid reserves from energy-rich prey like diatoms. Once winter hits, they stop feeding altogether and draw down those stores. They even *shrink* — physically reducing their body size to conserve energy until the light returns. It's a remarkable adaptation, but it only works because adults have the body mass to accumulate meaningful reserves in the first place.

Larvae don't have that option. Too small to build lipid stores, they must keep feeding continuously throughout the winter — even when food is almost nowhere to be found. What little food is available to them comes largely from algae that has been trapped in sea ice and is slowly released as the ice melts, or from microzooplankton persisting in the water column.

<div class="row justify-content-sm-center mt-3">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/Fall-Winter-recruitement-ZTS.png" title="Krill overwintering strategies by age class" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Krill have different overwintering strategies depending on their age: adults have lipid stores to sustain them through winter; larvae don't — and must keep feeding to survive.
</div>

This is what makes winter the critical bottleneck for recruitment. Sea ice isn't just frozen water — for larval krill, it's a food source, a refuge from predators, and in some cases a physical habitat. As sea ice declines and becomes less predictable under climate change, understanding exactly *which* of these roles matters most — and *where* — becomes urgently important.

---

## What mechanisms control overwinter survival?

Food and shelter — that's the short answer. Sea ice facilitates larval overwinter survival and subsequent recruitment by providing both.

During the winter months, a larval krill's ability to survive comes down to two things: access to sea ice algae as a food source, and the ability to avoid predation. The prevailing paradigm in krill biology centers on exactly this — that sea ice habitat is what makes larval survival possible, and that years with extensive, stable sea ice produce strong recruitment classes the following spring.

<div class="row justify-content-sm-center mt-3">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/food-shelter-ZTS-Ulrich-Frieir.png" title="Krill swarming on the underside of sea ice" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Krill swarming on the underside of sea ice — exactly the habitat that the prevailing paradigm puts at the center of larval overwinter survival. Photo: Ulrich Freier and Zephyr Sylvester.
</div>

That image captures something remarkable: krill aggregating on the underside of the ice, grazing on algae growing in and just below the ice surface. The ice isn't just a backdrop — it's actively being used, as food source and as physical structure that offers some refuge from the open water below where predators hunt.

But this paradigm, compelling as it is, raises a harder question: *which* of these mechanisms matters most? Is it the food, the shelter, or the physical habitat structure itself? And does the answer differ depending on where in the Southern Ocean the larvae are?

That's what our model was designed to untangle.

---

## What is a qualitative network model — and why use one?

It is unknown what adaptations larval krill have to survive the overwintering
period and what impacts decreases in sea ice may have on krill recruitment. Current
theories on overwintering mechanisms include:

- **Autumn food availability** — krill must build condition before winter arrives
- **Sea ice algae as a major energy source** — ice-associated algae as a critical 
  winter food subsidy for larvae
- **Alternate food sources** — microzooplankton and other pelagic prey when ice 
  algae is unavailable
- **Habitat flexibility** — larval distribution shifting between under-ice and 
  pelagic depending on the harshness of winter conditions

Each of these mechanisms carries different implications for how krill recruitment 
responds to environmental change, and in particular the role of sea ice.

While some empirical work has been done and some models have been tested, more 
clarity is needed in understanding how uncertain mechanisms may impact model 
predictions.

This brings me to my research question: **What is the impact of uncertainty in the 
mechanisms controlling overwintering survival on future projections of recruitment 
success?**

---

### How can the impact of uncertainty in the mechanisms controlling overwintering survival be quantified?

So how do we attempt to answer a question like this? We wanted to test three things:
knowns vs. unknowns, the region most important to krill, and climate change scenarios.

<div class="row justify-content-sm-center mt-3">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/hotspots-slide-pngs/Slide21.png" 
        title="Components tested in the QNM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Components tested: knowns vs. unknowns, the region most important to krill, 
    and climate change scenarios.
</div>

In order to test these three things in a non-computationally expensive way — while 
still capturing the complexity of the ecosystem — we developed a qualitative network 
model (QNM) that simplifies ecological relationships into their essential structure.

### Our Qualitative Network Analysis Framework

The approach follows five steps:

1. **Tabulate all interactions** — compile every relevant ecological relationship 
   from the literature
2. **Identify uncertain interactions** — classify each by the level of certainty 
   based on literature, expert knowledge, and observational data
3. **Evaluate models** — test the network structure with and without uncertain 
   mechanisms
4. **Aggregate results** — combine outputs across model variants
5. **Analyze** — interpret what the range of model structures tells us about 
   system behavior

<div class="row justify-content-sm-center mt-3">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/overwintering/Figure-1.png" 
        title="QNM interaction network" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Our QNM tabulates interactions critical for understanding the impacts on larval 
    survival and growth over the winter.
</div>

Once all possible interactions have been determined via an extensive literature 
review, interactions are classified based on the level of uncertainty as determined 
by the literature, expert knowledge, and observational data. This creates varying 
model structures that explicitly account for the level of certainty in the 
relationship between response variables.

The neat thing about a QNM is that it's computationally inexpensive which means 
we could include more complex features like sea ice convergence and terraces in the 
model without it becoming prohibitively costly to run.

We then ran simulations across each habitat of interest, for all climate change 
scenarios, with and without the uncertain mechanisms and set about answering 
our questions.

---

## What will happen to larval overwintering habitat in the future?

Habitat suitability for larval krill will decrease under all scenarios, 
particularly in the Northern Antarctic Peninsula. Out of all the possible 
relationships in the model, the one with the most influence on this result 
was the projected decrease in seasonal primary productivity — less food 
available in autumn means larvae arrive at winter already behind.

---

## How can we improve our understanding of larval overwintering?

This highlights how a single hypothesized mechanism can invert baseline 
projections — and underscores the importance of refining our understanding 
of the processes linking sea ice features, predator avoidance, and larval 
krill performance.

The two areas of greatest uncertainty that future work should target are:

- **Food availability and composition** — what larvae are actually eating 
  in winter, and how that changes as ice declines
- **Predation risk and sea ice terraces** — whether ice structure provides 
  meaningful refuge, and what is lost when that structure disappears

This is especially pertinent in the Northern Antarctic Peninsula, where 
habitat suitability is projected to decline due to reduced food availability 
— making it the region where resolving these uncertainties matters most.

Which brings us back to where we started:

<div class="row justify-content-sm-center mt-4">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" 
        path="assets/img/projects/overwintering/untangling-infographic.jpg" 
        title="Untangling krill overwinter survival — infographic" 
        class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The full picture: food, shelter, habitat, and the mechanisms we still 
    need to untangle. This is what the model is trying to capture — and 
    what future field and lab work needs to resolve.
</div>

The infographic tells the story we couldn't tell with equations alone. 
The QNM gave us a framework for holding competing hypotheses at once; 
the infographic makes visible why that complexity matters. Both are 
trying to do the same thing — make the invisible winter world of a 
larval krill a little more legible.
---

*This paper was produced as part of my dissertation research.*
