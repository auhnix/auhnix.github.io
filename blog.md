---
layout: post
title: thoughtsposting
---
<ul>
	{% assign sorted_tags = site.tags | sort %}
	{% for tag in sorted_tags %}
	{% assign vids = tag[1] | sort %}

	{% if vids != empty %}

	  <a href="/tag/{{ tag[0] }}"><h2 id="{{tag[0] | uri_escape | downcase}}">{{tag[0]}}</H2></a>
	     <p>
	      {% for p in vids %}
	      <a href="{{ p.url }}">{{ p.title }}</a> ({{p.type}}/{{p.category}}) &raquo;  <span class="entry-date"><time datetime="{{ p.date | date_to_xmlschema }}" itemprop="datePublished">{{ p.date | date: "%B %d, %Y" }}</time></span>
	     <br />
	      {% endfor %}
	    </p>
	  
	{% endif %}
{% endfor %}
</ul>

<ul>
  {% for post in site.posts %}
    <li>
      <h2 style="margin-bottom: -.8em"><a href="{{ post.url }}">{{ post.title }}</a></h2><br><em>[{{ post.date | date: site.theme_config.date_format }}]</em><br>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>