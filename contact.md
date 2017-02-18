---
title: Contact
layout: post
permalink: /contact/
---

<h1 class="headline">By Authors</h1>
<!-- {% for post in site.posts %}
<h3><a href="{{post.url | prepend: site.baseurl}}">{{post.author}}</a></h3>
{% endfor %} -->

{% assign sorted-posts = site.posts | where: "author","adarsha" %}
{% for post in sorted-posts limit: 10 %}
<li>{{post.author}}</li>
{% endfor %}

<!-- {% assign sorted-posts = site.posts | where: "author","deepak basrur" %}
{% for post in sorted-posts limit: 10 %}
<li>{{post.author}}</li>
{% endfor %} -->

