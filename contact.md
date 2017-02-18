---
title: Contact
layout: post
permalink: /contact/
---

<h1 class="headline">By Authors</h1>
<!-- {% for post in site.posts %}
<h3><a href="{{post.url | prepend: site.baseurl}}">{{post.author}}</a></h3>
{% endfor %} -->

<!-- {% assign sorted-posts = site.posts | where: "author","adarsha" %}
{% for post in sorted-posts limit: 10 %}
<li>{{post.author}}</li>
{% endfor %}

{% assign sorted-posts = site.posts | where: "author","deepak basrur" %}
{% for post in sorted-posts limit: 10 %}
<li>{{post.author}}</li>
{% endfor %} -->

<section id="site-authors">
{% for author in authors %}
  {% capture rawposts %}{% for post in site.posts %}{% if post.author == author %}{{ post.title }}*{{ post.url }}|{% endif %}{% endfor %}{% endcapture %}
  {% assign posts = rawposts | split:'|' | sort %}
  <h2 id="{{ author | downcase }}-ref">{{ author }}</h2>
  {% for post in posts %}
  <ul>
    {% assign parts = post | split:'*' %}
    <li><a href="{{ BASE_PATH }}{{ parts[1] }}">{{ parts[0] }}</a></li>
  </ul>
  {% endfor %}
{% endfor %}
</section>
