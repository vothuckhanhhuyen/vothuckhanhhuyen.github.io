---
layout: page
title: gallery
permalink: /gallery/
nav: true
nav_order: 4
---

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 16px; margin-top: 1rem;">
  {% for item in site.data.gallery %}
    <div style="display: flex; flex-direction: column; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      <img
        src="{{ item.image | prepend: '/assets/img/gallery/' | relative_url }}"
        alt="{{ item.caption }}"
        style="width: 100%; height: 220px; object-fit: cover;"
      />
      {% if item.caption %}
        <div style="padding: 8px 12px; font-size: 0.85em; color: var(--global-text-color-light); text-align: center;">
          {{ item.caption }}
        </div>
      {% endif %}
    </div>
  {% endfor %}
</div>
