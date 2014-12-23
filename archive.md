---
layout: page
title: Archive
permalink: /archive/
---
<article>
{% for post in site.posts %}
{% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
{% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
{% if month != nmonth %}
{% if forloop.index != 1 %}</ul>{% endif %}
<h3>{{ post.date | date: '%Y년 %m월' }}</h3><ul>
{% endif %}
<p style="margin-bottom:-25px; padding-bottom:size:-10px;"> <a href="{{ post.url }}">{{ post.title }}</a>
<span class="date"><Font style="color: #828282; font-size: 13px;">({{ post.date | date: "%m-%d" }})</font></span> </p>

{% endfor %}

</article>


