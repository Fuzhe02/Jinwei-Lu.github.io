---
layout: splash
title: "Jinwei Lu"
permalink: /
header:
  overlay_image: image-alignment-1200x4002.jpg
  overlay_filter: 0.35
  caption: "Shenzhen University"
  cta_label: "View CV"
  cta_url: "/cv/"
excerpt: |
  Researcher at Shenzhen University. Interests: Machine learning, signal processing, and intelligent sensing.

intro:
  - excerpt: |
      I build algorithms and systems at the intersection of data, optimization, and real-world applications.

feature_row:
  - image_path: image-alignment-580x300.jpg
    alt: Publications
    title: Publications
    excerpt: Curated list of peer‑reviewed papers and preprints
    url: "/publications/"
    btn_label: "Browse"
    btn_class: "btn--primary"
  - image_path: image-alignment-300x200.jpg
    alt: Teaching
    title: Teaching
    excerpt: Courses, mentoring, and educational resources
    url: "/teaching/"
    btn_label: "Explore"
    btn_class: "btn--primary"
  - image_path: 500x300.png
    alt: Talks
    title: Talks
    excerpt: Slides and videos of invited and conference talks
    url: "/talks/"
    btn_label: "Watch"
    btn_class: "btn--primary"

highlights:
  - image_path: 3953273590_704e3899d5_m.jpg
    alt: Selected Papers
    title: Selected Papers
    excerpt: |
      - Paper A, Journal/Conf, 2024
      - Paper B, Journal/Conf, 2023
      - Paper C, Journal/Conf, 2022
    url: "/publications/"
    btn_label: "All publications"
    btn_class: "btn--inverse"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="highlights" %}

### Recent publications

{% assign pubs = site.publications | sort: 'date' | reverse %}
<ul class="bibliography">
{% for pub in pubs limit:5 %}
  <li>
    <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>
    {% if pub.venue %}<span> · {{ pub.venue }}</span>{% endif %}
    <span> ({{ pub.date | date: "%Y" }})</span>
  </li>
{% endfor %}
</ul>

<p><a class="btn btn--primary" href="/publications/">All publications</a></p>