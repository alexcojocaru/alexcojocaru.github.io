---
layout: default
---


Projects
--------

{% assign repositories = (site.github.public_repositories | sort: "pushed_at") | reverse %}
{% for repository in repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})  
    {{ repository.description }}
{% endfor %}

{% assign site_repositories = ["frame-geometry-comparator","cycle-route-planner"] %}
{% if site_repositories contains "frame-geometry-comparator" %}
test
{% endif %}
