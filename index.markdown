---
layout: default
title: Coding-guidelines
excerpt: Collection of files, settings and documents concerning code writing at ZEIT ONLINE.
---

# Guideline overview

{% for post in site.posts %}
* ## [{{ post.title }}]({{ post.url }})
  {{ post.excerpt }}
{% endfor %}
