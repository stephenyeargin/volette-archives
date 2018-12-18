---
layout: home
---

<h1><em>The Volette</em></h1>

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

<h2>News</h2>

{% for post in site.posts %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{{ post.date | date: '%B %e, %Y' }}
{{ post.excerpt }}
{% endfor %}

<ul>
{% assign volumes = (site.pages | sort: 'volume') | reverse %}
{% for volume in volumes %}
<li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
