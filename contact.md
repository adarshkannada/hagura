---
title: ByAuthors
layout: post
permalink: /contact/
---

{% assign items_grouped = site.posts | group_by: 'author'  %}
{% for group in items_grouped %}
<h3>{{group.name}}</h3>
{% for item in group.items %}
<a href="{{item.url | prepend: site.baseurl}}">{{item.title}}</a>
{% endfor %}
{% endfor %}
