---
layout: page
title: photography | & life doesn't stop for anybody
description: photography portfolio
sitemap:
    priority: 0.7
    lastmod: 2019-06-30
    changefreq: weekly
---

<div id="photowall">
{% for image in site.static_files %}
    {% if image.path contains 'assets/images/gallery' %}
        <img class="grid" src="{{ site.baseurl }}{{ image.path }}" alt="image" />
    {% endif %}
{% endfor %}
</div>