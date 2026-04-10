---
layout: page
title: gallery
permalink: /gallery/
nav: false
---

<div class="gallery-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 12px; margin-top: 1rem;">
  {% assign images = site.static_files | where_exp: "file", "file.path contains '/assets/img/gallery/'" %}
  {% for image in images %}
    <div style="overflow: hidden; border-radius: 8px;">
      <img
        src="{{ image.path | relative_url }}"
        alt="{{ image.name }}"
        class="img-fluid rounded z-depth-1"
        style="width: 100%; height: 220px; object-fit: cover; cursor: zoom-in;"
        data-zoomable
      />
    </div>
  {% endfor %}
</div>
