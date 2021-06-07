---
layout: default
site_repositories:
  - elevation-profile
  - frame-geometry-comparator
  - cycle-route-planner
---


Projects
--------

{% assign repositories = (site.github.public_repositories | sort: "pushed_at") | reverse %}
<ul>
{% for repository in repositories %}
  {% if page.site_repositories contains repository.name %}
    <li>
		<a href="{{ site.github.url }}/{{ repository.name }}">{{ repository.name }}</a>
		<br />
		{{ repository.description }}
	</li>
  {% endif %}
{% endfor %}
</ul>
