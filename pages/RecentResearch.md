---
layout: page
title: Recent Research
tagline:
permalink: /Recent.html  # What is Perma Link ==> What is shown on the URL, https://sini1919.github.io/[permalink].html 이런식
---


{% for f in site.data.friends %}  
<div class="link-chip">
 <img alt="{{f.describe}}" src="{{f.image}}" class="link-chip-icon">
 <a title="{{f.describe}}" target="_blank" class="link-chip-title" href="{{f.url}}">{{f.name}}</a>
</div>
{% endfor %}

Energies : ["A Long-Term Evaluation on Transmission Line Expansion Planning"](https://doi.org/10.3390/en13081899)

IEEE Transaction on Smart Grid : [ "Optimal Bidding and Operation Strategies for EV Aggegators by Regrouping Aggregated EV Batteries"](https://doi.org/10.1109/TSG.2020.2999887)

[되돌아가기]({{ site.url }})

<hr/>

  {% if site.data.social.valine_comment.enable  == true %}
  <script src="/comment/av-min.js"></script>
  <script src="/comment/Valine.min.js"></script>
  <div id="comments"></div>
  {% include comments.html %}
  {% endif %}

  {% include scripts.html %}
