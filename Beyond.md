---
layout: app
title: "Beyond"
permalink: Beyond
---
<img src="{{ site.baseurl }}/assets/img/explode.png" alt="booom" style="width:300px;height:300px;">

<h1>Beyond Builds</h1>
<h2>Release</h2>

<ul>
{% for post in site.posts %}
	{% if post.tags contains "Beyond" and post.tags contains "Release" %}
  <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  </li>	
	{% endif %}
{% endfor %}
</ul>

<h2>Development</h2>
<ul>
{% for post in site.posts %}
	{% if post.tags contains "Beyond" %}
		{% unless post.tags contains "Release" %}
  <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  </li>	
  		{% endunless %}
	{% endif %}
{% endfor %}
</ul>