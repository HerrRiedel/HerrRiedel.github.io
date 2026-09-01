---
permalink: /consulting/
title: "Consulting"
excerpt: "Consulting"
author_profile: true
redirect_from:
  - /consulting.html
---

<div class="lede">“I want to open a pharmacy in Guadalajara. Where should I put it?”</div>

The usual answer to that question is a broker's intuition, an observation that a
particular corner has a lot of foot traffic, and a handful of blocks near enough
to go and look at. What an owner would rather have is every corner of the city
considered, on reasons they can inspect, ending in a shortlist they can drive to.

**MaMi** is the tool I built to do that.

---

## An idea borrowed from biology

How do biologists map where a jaguar could live, without following jaguars
around the whole country? They take the places where jaguars *are*, ask what
those places have in common — forest cover, water, prey, elevation, distance
from roads — and then find every other place that looks like that. They never
ask the jaguar. They learn its **habitat**. Ecologists call these species
distribution models, and they are standard practice in conservation planning and
in predicting where an invasive species will spread next.

A pharmacy also has a habitat.

## One twist biology does not have

A jaguar sighting means the jaguar *lived* there. But a pharmacy that opened
last year and closed this year tells us the opposite of what we want to know. So
the model does not study where pharmacies **are**. It studies where pharmacies
**survive**.

Mexico's business census records every establishment in the country twice a
year, which gives roughly a dozen photographs of the city's commerce between
2016 and 2026. Following each pharmacy across that decade lets us ask, of every
spot in the city: *if a pharmacy had opened here, would it still be open three
years later?*

## How the model sees the city

Guadalajara is cut into **40,608 hexagons**, each about 160 metres across. For
each one the question is what you can reach on foot — at five, ten and fifteen
minutes' walk, following real streets rather than circles drawn on a map. A
ravine, a highway or a wall means you cannot get there, and a customer on foot
knows it even when the map says two hundred metres.

Inside each of those walking distances the model looks at three things: **who
lives there** (population, ages, schooling, household size, income proxies, how
fast the area has grown since 2010), **what is already there** (every other
business by type, hospitals, schools, offices, how mixed the street life is),
and **how reachable it is** (street layout, main avenues, bus and metro stops,
parks and markets). That comes to about 150 signals per hexagon. Nobody tells
the model which of them matter; it finds that out by comparing thousands of
pharmacies that survived against thousands of places where none did.

A location can also be perfect and useless, because a pharmacy is already
standing on it. So the same map answers three different business questions —
where there is an open opportunity with no pharmacy within a five-minute walk,
where there is room for one more, and where the pharmacy deserts are.

<figure class="mami-fig">
  <a href="/mami/"><img src="/assets/images/mami_habitat_gdl.jpg"
     alt="Habitat suitability map of the Guadalajara metropolitan area, scored hexagon by hexagon for pharmacy viability."></a>
  <figcaption>The result: a habitat map for pharmacies in Guadalajara. The colour
  ramp runs from sand through grassland and forest to deep water — the surface is
  a habitat suitability map, so it may as well read like one.</figcaption>
</figure>

## Does it actually work?

The honest test is to hide entire neighbourhoods from the model, train it on the
rest of the city, and then ask it to judge the neighbourhoods it has never seen.
It holds up under that.

The harder test is a different city altogether. We built a second model for
**Monterrey** — eight hundred kilometres away, a different climate, a different
economy, a different shape of city — and then took the Guadalajara model, which
had never seen a single street in Monterrey, and asked it to judge Monterrey. It
recovered **97% of the local model's accuracy**. The levels differ, since
Monterrey simply has fewer pharmacies per neighbourhood, but what makes a corner
work turns out to be nearly the same in both.

---

## In practice

I built MaMi at **R2**, a market research firm in Guadalajara, and worked with it
there from 2020 to 2024. Eight businesses opened on its recommendations —
pharmacies, clinical laboratories and restaurants.

What a client receives is a score for every corner of the metro area, a ranked
shortlist of addresses, or ranked zones where a whole area is promising; for each
one, the reasons behind the score; and an interactive map anyone can explore.
Change the business type — a café, a gym, a clinic — and the same machinery
re-learns that habitat from scratch.

The work rarely ended at the ranking. It ended in a room with the owner or the
board, going through why a particular corner scored the way it did and which
conditions were carrying the result. A site that ranks well for the wrong reason
is one an owner should be able to overrule, and that is only possible if the
model can say what it is reacting to.

## What it is not

**It is not a crystal ball.** It says a place *looks like* the places where
pharmacies last. Your rent, your staff and your neighbours still decide the
outcome.

**It does not see everything.** Informal commerce, property prices and the
inside of a building are invisible to it.

**It is a shortlist, not a verdict.** It turns forty thousand candidate spots
into thirty worth visiting. The visit still matters.

---

## See it

<a class="demo-card" href="/mami/">
  <span class="demo-title">MaMi — Pharmacy site selection &rarr;</span>
  <span class="demo-desc">The habitat map for Guadalajara and Monterrey, scored hexagon by hexagon. Switch between the raw model score and the three competition views, then open any ranked candidate to see the conditions pushing its score up or down.</span>
  <span class="demo-meta">Calibrated survival probabilities · validated on spatially held-out blocks</span>
</a>
