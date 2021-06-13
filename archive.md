---
layout: default
---

# Archive

Browse all posts by month and year.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}

  <h3>{{ yearMonth.name }}</h3>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
