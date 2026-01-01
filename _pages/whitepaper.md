---
layout: page
title: White Paper
permalink: /whitepaper/
nav: false
nav_order: 4
display_categories: [Recommendations]
horizontal: false
social: false
---

***White paper out now: [arXiv:2512.24465](https://arxiv.org/abs/2512.24465){:target="_blank"}!***

In March 2025, when more than 200 astronomers came together in a hybrid symposium focused on the state of the field for female scientists, symposium participants engaged in solution-oriented discussions aimed at ameliorating the effects that drive the disproportionate attrition of women at each career stage (sometimes colloquially referred to as the "leaky pipeline"). These discussions resulted in a white paper (available on [arXiv](https://arxiv.org/abs/2512.24465){:target="_blank"}), which provides community-level recommendations and best practices for the retention of talent in astrophysics.  

See below for some summarized recommendations and "cheatsheets" that can be readily shared alongside the Picture an Astronomer white paper. We note that these cheatsheets are not a substitute for reading the white paper and engaging with the full context and literature presented therein, nor do they comprehensively list recommendations from each section of the white paper.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.recommendations | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>


<hr style="height:1px; visibility:hidden;" />

*While the symposium was supported by the University of Chicago Women's Board, the Kavli Institute for Cosmological Physics, and the Department of Astronomy & Astrophysics at the University of Chicago, and we are immensely grateful for that support, we note that the work presented in the white paper is not specifically endorsed by, or representative of the view of, those organizations. Instead, this white paper is the work of the authors.*