---
layout: page
title: Blog
tagline: news
group: navigation
weight: 10
---
{% include JB/setup %}

[Archive](../archive.html) [By Category](../categories.html)

<ul >
    {% for post in site.posts limit 4 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
        {{ post.content | truncatewords:75}}<br>
            <a href="{{ post.url }}">Read more...</a><br><br>
    {% endfor %}
</ul>
