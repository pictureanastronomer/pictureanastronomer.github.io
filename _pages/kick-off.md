---
layout: page
title: Kick-off
permalink: /kickoff/
years: [2024]
nav: true
nav_order: 2
display_categories: [Invited Speakers, Other Presenters]
horizontal: false
social: false
---

**January 30, 2025 at the University of Chicago William Eckhardt Research Center (5640 S. Ellis Ave., Chicago, IL) and online**

**Recording available [here](https://uchicago.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=b8fb0b8b-2ea4-4a12-8a5c-b2b3013b19eb){:target="_blank"}**

To set the tone for the rest of the Picture an Astronomer programming and highlight the astronomical contributions of local women, we are hosting a kick-off event, featuring talks from female faculty in the Department of Astronomy & Astrophysics. In-person attendees will receive a hard copy of the SIRIUS B pedagogical text, [Astronomy as a Field: A Guide for Aspiring Astrophysicists](https://arxiv.org/abs/2312.04041){:target="_blank"}, which was created by a University of Chicago PhD candidate and features contributions from a number of Chicago astrophysicists.

The talks will be followed by a panel discussion. Other department members will also be available to answer questions about astronomy in general, and there will be ample opportunity to engage with more junior women in the department (PhD students and postdoctoral fellows) to learn more about their work.

*~Register [here](https://docs.google.com/forms/d/1aoZqLiu0woXlWP5EOr7J5kd93tlrJpk1bMbaSU4y6Jk/viewform?edit_requested=true){:target="_blank"} for in-person or virtual attendance.~*

Schedule:
- 6pm: Doors open (opportunity to mingle and engage casually with astronomers before the talks)
- 6:30 - 6:50pm: Lecture by Chihway Chang (cosmology) - "From Pixels to Cosmology -- How we make sense of the sky"
- 6:50 - 7:10pm: Lecture by Hsiao-Wen Chen (galaxies) - "Mapping the Dark Universe"
- 7:10 - 7:30pm: Lecture by Leslie Rogers (exoplanets)
- 7:30 - 8pm: Q&A/panel discussion

See below for more information about each of the invited speakers and their talks.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.kickoffspeakers | where: "category", category -%}
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
