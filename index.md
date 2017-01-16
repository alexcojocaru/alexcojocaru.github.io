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
<p></p>
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
