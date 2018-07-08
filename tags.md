---
layout: page
title: Posts by tag
---
{% capture tags %}{% for tag in site.tags %}{{ tag[0] }}|{% endfor %}{% endcapture %}
{% assign sortedtags = tags | split:'|' | sort %}


{% for tag in sortedtags %}
  <p><a name="{{ tag }}"></a><h3>{{ tag }}</h3>
    {% for post in site.tags[tag] %}
    <p>
        <div class="page-meta"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_long_string }}</time></div>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </p>
    {% endfor %}
    </p>

{% endfor %}
