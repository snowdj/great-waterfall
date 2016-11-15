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

    <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}"><h3 class="h1 post-title">{{ post.title }}</h3></a>
       
       {% if post.subtitle %}
        <h5 class="post-subtitle">
            {{ post.subtitle }}
        </h5>
       {% endif %}    
    
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>    

 
            {% if post.categories != empty %}
            Catogories:
            {% for category in post.categories %}
	    
			<a class="codinfox-tag-mark badge" href="{{ site.url }}/categories/#{{ category | slugify }}" >
				 &nbsp; #{{ category }}
			</a>
			
            {% endfor %}
	    
            {% endif %}
	    
            
            {% if post.tags != empty %}
            |&nbsp; tags:
            {% for tag in post.tags %}
	    
			<a class="codinfox-tag-mark badge" href="{{ site.url }}/tags/#{{ tag | slugify }}" >
				 &nbsp; #{{ tag }}
			</a>
			
            {% endfor %}
	    
            {% endif %}


	
	
    <!-- <p class="post-meta">Posted by {% if post.author %}{{ post.author }}{% else %}{{ site.title }}{% endif %}</p> -->

    <div class="post-entry">
      {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
	  <a href="{{ post.url | prepend: site.url }}" class="post-read-more">Read More</a>
    </div>
  </li>
{% endfor %}
</ul>
