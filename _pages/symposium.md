---
layout: page
title: Symposium
permalink: /symposium/
# description: A growing collection of your cool projects.
years: [2024]
nav: true
nav_order: 4
display_categories: [Invited Speakers]
horizontal: false
social: false
---

**Save the dates: March 4 - 6, 2025 at the University of Chicago William Eckhardt Research Center (5640 S. Ellis Ave., Chicago, IL)**

In March 2025, we will host a scientific symposium including female astrophysicsits from diverse institutions and backgrounds. We intend this to be an opportunity to engage in a larger discussion about the state of the field for women around the globe and will spend a portion of the symposium in “hack day” mode, looking to discuss solutions to universal and near-universal challenges to the retention of female astrophysicists. An extended goal is to codify these discussions in public white papers. This symposium alone will not fix the leaky pipeline, but we hope that crowd-sourcing best practices for increasing retention will inspire the implementation of even small, but significant changes that lead to inclusion. Simultaneously, we hope that promoting these sorts of discussions will lead to the potential for larger changes with expanded engagement.

*Registration information coming soon.*

See below for more information about each of the invited speakers and their talks (more to be added).

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.symposiumspeakers | where: "category", category -%}
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
