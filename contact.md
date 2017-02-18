---
title: Contact
layout: post
permalink: /contact/
---

{% assign sorted-posts = post.author | sort: 'title' %}
{% for post in sorted-posts limit: 10 %}
<li>{{post.title}}</li>
{% endfor %}
