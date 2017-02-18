---
title: Contact
layout: post
permalink: /contact/
---

<h1 class="headline">By Authors</h1>
{% for post in site.posts %}
<h3><a href="{{post.url | prepend: site.baseurl}}">{{post.author}}</a></h3>
{% endfor %}
