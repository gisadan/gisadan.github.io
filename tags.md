---
layout: page
permalink: /tags/
title: <i class="fa fa-tags" aria-hidden="true"></i> Tags
---

<ul class="tag-cloud">
{% for tag in site.tags %}
  <span style="font-size: {{ tag | last | size | times:3 | plus: 80  }}%">
    <a href="#{{ tag | first | slugize }}">
      {{ tag | first }}
    </a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span>
{% endfor %}
</ul>

<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    
    
    {% for post in site.tags[tag_name] %}

    <div class="archive-item3">
    <i class="fa fa-tags" aria-hidden="true"></i> {{ tag_name }}<a name="{{ tag_name | slugize }}"></a>
    </div>

    <div class="archive-item2">
      <h5><a href="{{ root_url }}{{ post.url }}">{{post.title}}<br> <p> <time>({{ post.date | date:"%y년 %m월 %d일" }})</time></p></a></h5>
    </div>

    <div class="archive-item2-img">
    <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ post.image }}" ></a>
    </div>

    {% endfor %}
  </div>
{% endfor %}
</div>
