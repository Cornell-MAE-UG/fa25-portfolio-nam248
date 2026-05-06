---
layout: default
title: Neil Morrison - Portfolio
permalink: /projects/
---

<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p><strong>{{ project.title }}</strong></p>
        </a>
        <p style="font-size: 0.9em; color: #555; margin-top: 5px;"><em>{{ project.description }}</em></p>
      </div>
    {% endfor %}
</div>
</div>