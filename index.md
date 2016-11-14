---
title: Econ Notes at UVic
layout: page
---

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}

	<span class="post-date">
            
            {% if post.tags != empty %}
            |
            {% for tag in post.tags %}
			<a class="codinfox-tag-mark badge" href="{{ site.url }}/tag/#{{ tag | slugify }}" >
				<span class="glyphicon glyphicon-tag" aria-hidden="true"> </span> &nbsp; {{ tag }}
			</a>
            {% endfor %}
            {% endif %}
	</span>
    
    <!-- <p class="post-meta">Posted by {% if post.author %}{{ post.author }}{% else %}{{ site.title }}{% endif %}</p> -->

    <div class="post-entry">
      {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
	  <a href="{{ post.url | prepend: site.url }}" class="post-read-more">Read More</a>
</div>
  </li>
{% endfor %}
</ul>
