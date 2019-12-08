---
layout: page
title: <i class="fa fa-archive fa-lg"> </i> Archive
---
<div class="post-content">
{% for post in site.posts %}
{% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
{% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
{% if month != nmonth %}
{% if forloop.index != 1 %}{% endif %}
<h3>{{ post.date | date: '%Y년 %m월' }}</h3>

{% endif %}

<p style="margin-bottom:0px; padding-bottom:size:0px;">
<a href="{{ post.url }}">{{ post.title }}</a>
<span class="date">
<Font style="color: #0e0d0d; font-size: 13px;">
({{ post.date | date: "%m-%d" }})

{% endfor %}
