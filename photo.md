---
layout: resume
title: photography
sitemap:
    priority: 0.7
    lastmod: 2019-06-30
    changefreq: weekly
---

<header class="major">
	<p>selection of images shot somewhere between 2013 and now (early 2019). shot with a canon eos 20d. with a few exceptions, glass is either a <a href="https://www.sigmaphoto.com/70-300mm-f4-5-6-apo-dg-macro" target="_blank">sigma 70-300mm</a> or the beautiful <a href="https://www.lightandmatter.org/2012/equipment-reviews/the-canon-ef-50mm-f1-8-mark-i/" target="_blank">canon ef 50mm mk i</a>.</p>
</header>

<div class="photowall">
{% for image in site.static_files %}
    {% if image.path contains 'assets/images/gallery' %}
        <img class="grid" src="{{ site.baseurl }}{{ image.path }}" alt="image" />
    {% endif %}
{% endfor %}
</div>