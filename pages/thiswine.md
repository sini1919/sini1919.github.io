---
layout: page
title: All Wine
tagline: In Preparing
sitetime: No #display
permalink: /thiswine.html


## Below this line will be posted in the blog.
## Be noted following commands
#* ## : sub title ( large )
#* [hyperlink](link ip)
---
{% assign curtag = 'Wine' %}
<!--
## #Contact
<div>
Email: sini191919@gmail.com
</div>

Github: [link9596](https://github.com/link9596)



 ## #Wine Posts 

![wechat]()

![pay]()
-->

<article>

<div>

{% capture site_tags %}
{% for tag in site.tags %}
{{ tag | first }}
{% unless forloop.last %}
,{% endunless %}
{% endfor %}
{% endcapture %}
{% assign tag_words = site_tags | split:',' | sort %}

{% for item in (0..site.tags.size) %}
  {% unless forloop.last %}
    {% capture this_word %}{{ tag_words[item] | strip_newlines }}{% endcapture %}
    {% if this_word == curtag %}
    <h2 id="{{ this_word | cgi_escape }}" class="tag-title">
      #{{ this_word }}
    </h2>
    <!-- lists all posts corresponding to specific tag -->
    {% for post in site.tags[this_word] %}
      {% if post.title != null %}
        <div class="tagged-post">
          <h3 class="title">
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
          </h3>
          <div class="meta">
            {{ post.date | date: "%B %-d, %Y" }}
          </div>
        </div>
      {% endif %}  
    {% endfor %}
    {% endif %}
  {% endunless %}
{% endfor %}
</div>
</article>



