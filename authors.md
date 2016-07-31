---
layout: page
title: Authors
permalink: /authors/
---

<!-- Posts by author -->
<div>
    {% for author in site.authors %}
        <h2 id="{{ author }}">{{ author }}</h2>
        {% for post in site.posts %}
            {% if post.author == author %}
                <div>
                    <span style="float: left;">
                        <a href="{{ post.url }}">{{ post.title }}</a>
                    </span>
                    <span style="float: right;">
                        {{ post.date | date_to_string }}
                    </span>
                </div>
                <div style="clear: both;"></div>
            {% endif %}
        {% endfor %}
        <br />
    {% endfor %}
</div>

