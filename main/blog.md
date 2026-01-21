---
title: Blog
---

Welcome to my blog! I write about my adventures and thoughts.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

{% if site.posts.size == 0 %}
*No posts yet. Check back soon!*
{% endif %}
