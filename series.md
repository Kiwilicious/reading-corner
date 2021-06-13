---
layout: default
---

# Series

Browse all posts by series.

{% for cat in site.categories %}

<h3>{{ cat[0] | split: "-" | join: " " | capitalize }}</h3>
<ul>
  {% for post in cat[1] %}
  <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}
