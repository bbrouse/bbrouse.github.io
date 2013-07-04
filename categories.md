---
layout: base_page
title: Categories & Tags
header: Posts By Category and Tag
group: navigation
nav_title: Categories & Tags
---
{% include JB/setup %}
<p></p>
# Post Categories
<div class="well well-large">
	<ul class="tag_box inline">
	  {% assign categories_list = site.categories %}
	  {% include JB/categories_list %}
	</ul>


	{% for category in site.categories %} 
	  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
	  <ul>
	    {% assign pages_list = category[1] %}  
	    {% include JB/pages_list %}
	  </ul>
	{% endfor %}
</div>

# Post Tags
<div class="well well-large">
	<ul class="tag_box inline">
	  {% assign tags_list = site.tags %}  
	  {% include JB/tags_list %}
	</ul>


	{% for tag in site.tags %} 
	  <h2 id="{{ tag[0] }}-ref">{{ tag[0] }}</h2>
	  <ul>
	    {% assign pages_list = tag[1] %}  
	    {% include JB/pages_list %}
	  </ul>
	{% endfor %}
</div>

