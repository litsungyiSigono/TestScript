---
layout: app
title: "Heaven"
permalink: Heaven
---
<img src="{{ site.baseurl }}/assets/img/yeah.gif" alt="booom" style="width:300px;height:300px;">

<h1>Heaven Builds</h1>
<h2>Release</h2>

<ul>
{% for post in site.posts %}
	{% if post.tags contains "Heaven" and post.tags contains "Release" %}
  <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  </li>	
	{% endif %}
{% endfor %}
</ul>

<h2>Development</h2>
<ul>
{% for post in site.posts %}
	{% if post.tags contains "Heaven" %}
		{% unless post.tags contains "Release" %}
  <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  </li>	
  		{% endunless %}
	{% endif %}
{% endfor %}
</ul>