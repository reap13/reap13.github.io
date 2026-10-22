---
permalink: /
title: "About"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="home-hero">
  <p class="home-hero__eyebrow">Quantitative Psychology · University of Virginia</p>
  <p>Rea Pillai is currently a Quantitative Psychology PhD student at the University of Virginia. She earned her B.A. in Psychology with a minor in Data Science from the University of Virginia in 2026. Her research interests include network modeling, predictive modeling of psychological constructs, and intensive longitudinal data, with an emphasis on refining models to better capture mental healthcare disparities within vulnerable populations.</p>
</div>

<h2 class="home-section">Research interests</h2>

<ul class="chips">
  <li>Network modeling</li>
  <li>Predictive modeling</li>
  <li>Intensive longitudinal data</li>
  <li>Mental healthcare disparities</li>
</ul>

<h2 class="home-section">Explore</h2>

<div class="home-cards">
  <a class="home-card" href="{{ base_path }}/publications/">
    <span class="home-card__label">Publications</span>
    <span class="home-card__desc">Journal articles and a book</span>
  </a>
  <a class="home-card home-card--warm" href="{{ base_path }}/talks/">
    <span class="home-card__label">Talks &amp; posters</span>
    <span class="home-card__desc">Conference presentations</span>
  </a>
  <a class="home-card home-card--teal" href="{{ base_path }}/cv/">
    <span class="home-card__label">Curriculum vitae</span>
    <span class="home-card__desc">Education, research, teaching and leadership</span>
  </a>
</div>

<h2 class="home-section">Recent articles</h2>

{% assign recent = site.publications | where: "category", "manuscripts" | sort: "date" | reverse %}
<ul class="home-recent">
  {% for post in recent limit: 3 %}
  <li>
    <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
    <span class="home-recent__meta">{{ post.venue }} · {{ post.date | date: "%Y" }}</span>
  </li>
  {% endfor %}
</ul>
