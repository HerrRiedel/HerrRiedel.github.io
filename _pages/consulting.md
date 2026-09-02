---
permalink: /consulting/
title: "Consulting"
excerpt: "Consulting"
author_profile: true
redirect_from:
  - /consulting.html
---

<div class="lede">“I want to open a retail business. Where should I put it?”</div>

The usual answer to that question is a broker's intuition or an observation that
a particular corner has a lot of foot traffic. What an owner would rather have is
every possible location considered, ending in a handful of addresses worth
visiting.

**MaMi** is the tool I built to do that.

---

## An idea borrowed from biology

How do biologists map where a jaguar could live, without following jaguars around
the whole country? They take the places where jaguars *are*, ask what those
places have in common (forest cover, water, prey, elevation, distance from
roads), and then find every other place that looks like that. They learn the
jaguar's **habitat**. Ecologists call these species distribution models, and they
are standard practice in conservation planning and in predicting where an
invasive species will spread next.

A business also has a habitat. Take, for example, pharmacies in Guadalajara,
Mexico.

Mexico's business census records every establishment in the country twice a year,
which gives roughly a dozen photographs of the city's commerce between 2016
and 2026. Following each pharmacy across that decade lets MaMi learn the
pharmacy's environment: which socioeconomic variables determine where a pharmacy
flourishes?

---

## How the model sees the city

A city is cut into hexagons, each about 165 meters across. For each hexagon we
ask: what is the surrounding area like? What is the habitat there?

For each hexagon's surrounding area, the model looks at three things: **who lives
there** (population, ages, schooling, household size, income proxies, how fast
the area has grown since 2010), **what is already there** (every other business
by type, hospitals, schools, offices, how mixed the street life is), and **how
reachable it is** (street layout, main avenues, bus and metro stops, and parks
and markets). That comes to more than 400 signals per hexagon. The model finds the
habitat by comparing places where pharmacies flourished against places where none
did.

One map answers three different business questions — where there is an open
opportunity with no pharmacy nearby, where there is room for one more, and where
the pharmacy deserts are.

<figure class="mami-fig">
  <a href="/mami/"><img src="/assets/images/mami_habitat_gdl.jpg"
     alt="Habitat suitability map of the Guadalajara metropolitan area, scored hexagon by hexagon for pharmacy viability."></a>
  <figcaption>The result: a habitat suitability map for pharmacies in Guadalajara.</figcaption>
</figure>

---

## In practice

I built MaMi at **R2**, a market research firm in Guadalajara, and worked with it
there from 2020 to 2024. Eight successful businesses opened on its
recommendations, including pharmacies, clinical laboratories, and restaurants.

What a client receives is a score for every location in the metro area; a ranked
shortlist of addresses, or of zones, when a whole area is promising; the reasons
behind each score; and an interactive map they can explore. Change the business
type (a café, a gym, a clinic), and the same machinery re-learns that habitat
from scratch.

---

## See it

<a class="demo-card" href="/mami/">
  <span class="demo-title">MaMi — Pharmacy site selection &rarr;</span>
  <span class="demo-desc">The pharmacy habitat map for Guadalajara and Monterrey.</span>
  <span class="demo-meta">This is a sample. It uses only a subset of the model's variables. It is meant to show the method, not to site a business.</span>
</a>
