---
title: Projects
permalink: /projects/
layout: primary
lead: Websites, applications, and strategies that help agencies provide excellent value to the public.
content_wide: true
content_focus: false
redirect_from:
  - /consulting/
banner_cta: true
gridless: true
---
<style>
h2 {
  color:#2337CE;
}
</style>

<section class="usa-section background-gray">
<div class="usa-grid">
    <div class="usa-width-two-thirds">
      <h2 tabindex="0"> Projects </h2>
    </div>
</div>

<div class="usa-grid">
  <section class="usa-section">
    <div class="usa-section-bottom">
      <div class="usa-flex usa-flex-wrap">
        {% assign projects_list = site | find_collection: 'services_projects' | weighted_sort: 'project_weight', 'title' %}
        {% for project in projects_list %}
          {% include card.html
           image_src=project.image
           image_alt=project.image_accessibility
           image_icon=project.image_icon
           agency=project.agency
           tagline=project.title
           description=project.excerpt
           link=project.permalink
          %}
        {% endfor %}
      </div>
    </div>
  </section>
</div>
</section>