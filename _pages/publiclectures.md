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

Throughout February, we are hosting public talks featuring a prominent and inspiring woman in astrophysics. Each talk will be followed by a structured Q&A.

These lectures are intended for a general audience. Most events will be held at the William Eckhardt Research Center (5640 S. Ellis Ave., Chicago, IL) at the University of Chicago, with doors open at 6pm and lectures starting at 6:30pm. Jocelyn Bell Burnell's talk on February 19 will be held at the Adler Planetarium; doors will open at 6:30pm and her lecture will begin at 7pm.


*Note that separate registration is required for each talk.*

#### Schedule
- Dara Norman -- February 3, 2025 -- [register here](https://forms.gle/FuAxS2zSCpuX4Seb6){:target="_blank"}/**[recording](https://uchicago.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=14636922-5ce0-4897-9d8a-b2b3013c026b){:target="_blank"}**
- Katie Mack -- February 7, 2025 -- [register here](https://forms.gle/4KhPRXvUTpyvM6Gm9){:target="_blank"}/**[recording](https://uchicago.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=fe917f9a-29d5-4381-8edb-b2b3013c6997){:target="_blank"}**
- Dame Jocelyn Bell Burnell -- February 19, 2025 -- registration for [virtual attendance](https://forms.gle/ez8ajBBiGjummteL6){:target="_blank"}/[in-person attendance](https://www.adlerplanetarium.org/event/jocelyn-bell-burnell-lecture/){:target="_blank"} \[sold out!\]/**[recording](https://uchicago.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=42977e3a-c02c-4c57-90cd-b2b3013c8800){:target="_blank"}**
- Anna Frebel -- February 25, 2025 -- [register here](https://forms.gle/1t9N3GGL31TEDykL6){:target="_blank"}/**[recording](https://uchicago.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=7c40717a-4b3a-4a56-bfda-b2b3013ca8a4){:target="_blank"}**

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