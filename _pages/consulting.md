---
permalink: /consulting/
title: "Consulting"
excerpt: "Consulting"
author_profile: true
classes: [wide, justify-body]
redirect_from:
  - /consulting.html
---

<div class="lede">“I want to open a retail business. Where should I put it?”</div>

A good location depends on who lives nearby, what businesses are already there, and how people reach it. **MaMi** is the tool I built to bring those pieces together and turn a citywide search into a shortlist of locations worth visiting.

---

### An idea borrowed from biology

To map where jaguars could live, ecologists study the places where jaguars are found. They look at forest cover, water, prey, elevation, and distance from roads, then identify other places with similar conditions. These species distribution models map the jaguar's **habitat**.

A business also has a habitat. A pharmacy, a café, and a clinical laboratory each depend on a different combination of customers, surrounding businesses, and accessibility. MaMi adapts the ecological approach to identify places with suitable conditions for each business.

Take pharmacies in Guadalajara, Mexico. Using successive editions of Mexico's national business directory, I follow pharmacies over time and study how their locations relate to the surrounding neighborhoods.

---

### How MaMi sees the city

MaMi divides the city into hexagons, each about 165 meters across. For each hexagon, it characterizes the surrounding area using more than 400 variables:

* **Who lives there:** population, age, education, household size, income proxies, and neighborhood growth.
* **What is already there:** competitors, other businesses, hospitals, schools, offices, parks, and markets.
* **How people reach it:** street layout, main roads, and bus and metro stops.

The model learns from the patterns of pharmacy locations over time and uses those patterns to assess other parts of the city. The resulting map helps identify promising locations without a nearby pharmacy, areas that may support another one, and neighborhoods with limited access to pharmacies.

<figure class="mami-fig">
  <a href="/mami/"><img src="/assets/images/mami_habitat_gdl.jpg"
     alt="Habitat suitability map of the Guadalajara metropolitan area, scored hexagon by hexagon for pharmacy viability."></a>
  <figcaption>MaMi's pharmacy habitat map for Guadalajara.</figcaption>
</figure>

---

### In practice

I built MaMi at **R2**, a market research firm in Guadalajara, and used it in client projects from 2020 to 2024. Eight businesses opened based on its recommendations, including pharmacies, clinical laboratories, and restaurants.

Clients receive:

* Scores for locations across the metropolitan area.
* A ranked shortlist of addresses or promising zones.
* An explanation of the factors behind each score.
* An interactive map they can explore.

Each analysis is tailored to the business. For a café, a gym, or a clinic, MaMi learns that business's habitat from its own pattern of locations.

---

### See it

<a class="demo-card" href="/mami/">
  <span class="demo-title">MaMi — Pharmacy site selection &rarr;</span>
  <span class="demo-desc">Explore the pharmacy habitat maps for Guadalajara and Monterrey.</span>
  <span class="demo-meta">This demonstration uses a subset of the model's variables. It illustrates the method and is not a complete site-selection assessment.</span>
</a>

To discuss a location study, [get in touch](mailto:gabrielcr@ucsd.edu).
