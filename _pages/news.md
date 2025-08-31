---
permalink: /news/
title: News
author_profile: true
---

{% assign sorted_news = site.posts | sort: 'date' | reverse %}
<ul>
    {% for post in sorted_news %}
        <li>
            <strong>{{ post.title }}</strong> <br>
            <small>{{ post.date | date: "%B %d, %Y" }}</small>
            <p>{{ post.excerpt }}</p>
            <a href="{{ post.url }}">Read more</a>
        </li>
    {% endfor %}
</ul>