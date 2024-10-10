---
layout: page
title: Lectures
permalink: /lectures/
# description: A growing collection of your cool projects.
years: [2024]
nav: true
nav_order: 3
display_categories: [Invited Speakers]
horizontal: false
social: false
---

For each of the four weeks in February, we are hosting a public talk featuring a prominent and inspiring woman in astrophysics. Each talk will be followed by a structured Q&A.

These lectures are intended for a general audience and are suitable for all ages.


*Registration information coming soon. Note that separate registration is required for each talk.*

#### Schedule
- Dara Normal -- February 3, 2025
- Katie Mack -- date TBD
- Dame Jocelyn Bell Burnell -- February 19, 2025
- Anna Frebel -- February 25, 2025

See below for more information about each of the invited speakers and their talks.


<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.lecturespeakers | where: "category", category -%}
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