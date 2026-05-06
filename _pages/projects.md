---
layout: default
title: Neil Morrison - Portfolio
permalink: /projects/
---

<div class="featured-project" style="background-color: #f8f9fa; padding: 25px; border-radius: 8px; margin-bottom: 40px; border: 1px solid #ddd; text-align: center;">
    <h2><a href="{{ '/projects/2026-mae2250-project/' | relative_url }}">MAE2250: Automated System Design</a></h2>
    <p style="font-size: 1.1em; color: #444; max-width: 800px; margin: 10px auto;">
        <strong>Context:</strong> A comprehensive design project integrating mechanical components and microcontrollers.
    </p>
</div>

<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>