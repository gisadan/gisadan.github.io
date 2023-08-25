---
layout: page
title: <i class="fa fa-archive fa-lg"> </i> Archive
---


<div id="tag-cloud">
  {% for post in site.posts %}
  {% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
  {% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
  {% if month != nmonth %}
  {% if forloop.index != 1 %}{% endif %}

  <div class="archive-group">
  <h3>{{ post.date | date: '%Y년 %m월' }} </h3>
  {% endif %}

      
            <div class="archive-item2">
            <h3><a href="{{ post.url }}">{{ post.title }}</a> <time>({{ post.date | date:"%d %b" }})</time></h3>
            </div>

            <div>
              <div class="archive-image">
              <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ post.image }}" ></a>
            </div>

      

  {% endfor %}
</div>
</div>
