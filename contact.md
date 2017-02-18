---
title: Contact
layout: post
permalink: /contact/
---

<h1 class="headline">By Authors</h1>
<h1 class="headline">aaaa</h1>

<p align ="center">pikachu</p>

{% assign items_grouped = site.posts | group_by: 'author'  %}
{% for group in items_grouped %}
<h3>{{group.name}}</h3>
    {% for item in group.items %}
        <p>{{item.title}}</p>
    {% endfor %}
{% endfor %}
