---
layout: default
site_repositories:
  - frame-geometry-comparator
  - cycle-route-planner
---


Projects
--------

{% assign repositories = (site.github.public_repositories | sort: "pushed_at") | reverse %}
<p>{{ site.github.hostname }}</p>
<p>{{ site.github.pages_hostname }}</p>
<p>{{ site.github.project_title }}</p>
<p>{{ site.github.owner_name }}</p>
<p>{{ site.github.owner_url }}</p>
<p>{{ site.github.repository_name }}</p>
<p>{{ site.github.url }}</p>
<ul>
{% for repository in repositories %}
  {% if page.site_repositories contains repository.name %}
    <li>
		<a href="{{ repository.html_url }}">{{ repository.name }}</a>
		<br />
		{{ repository.description }}
	</li>
  {% endif %}
{% endfor %}
</ul>
