---
layout: page
permalink: /research/
title: research
description: Publications and selected research projects
nav: true
nav_order: 2
display_categories: [research]
horizontal: false
---

<h2>Publications</h2>

{% include bib_search.liquid %}

<div class="publications">
{% bibliography %}
</div>

<h2>Projects</h2>

<div class="projects">
{% assign sorted_projects = site.projects | sort: "importance" %}
<div class="row row-cols-1 row-cols-md-3">
  {% for project in sorted_projects %}
    {% include projects.liquid %}
  {% endfor %}
</div>
</div>
