---
layout: default
title: 课堂内外，丰富多彩
---

<p>{{ page.title }}</p>
        <p>{{ user.name }}</p>
        <ul>
            {% for post in site.posts %}
            <li>
                <a href="{{ post.url }}">{{ post.title }}</a>
            </li>
            {% endfor %}
        </ul>
        <BR>
        -------
        <BR>
        {% for tag in site.tags %}
        <h3>{{ tag[0] }}</h3>
            <ul>
                {% for post in tag[1] %}
                <li><a href="{{ post.url }}">{{ post.title }}</a></li>
                {% endfor %}
            </ul>
            {% endfor %}
-------
<ul>
    {% for member in site.data.members %}
    <li>
        <a href="https://github.com/{{ member.github }}">{{ member.name }}</a>
    </li>
    {% endfor %}
    </ul>