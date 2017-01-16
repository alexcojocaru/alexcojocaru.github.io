---
layout: default
---


Projects
--------

{% assign repositories = (site.github.public_repositories | sort: "pushed_at") | reverse %}
{% assign site_repositories = [ "frame-geometry-comparator", "cycle-route-planner" ] %}
{% for repository in repositories %}
  {% if site_repositories contains repository.name %}
    * [{{ repository.name }}]({{ repository.html_url }})  
      {{ repository.description }}
  {% endif %}
{% endfor %}
