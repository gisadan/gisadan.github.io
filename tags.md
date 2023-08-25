---
layout: page
permalink: /tags/
title: <i class="fa fa-tags" aria-hidden="true"></i> Tags
---


<ul class="tag-cloud">
{% for tag in site.tags %}
  <span style="font-size: {{ tag | last | size | times:5 | plus: 70  }}%">
    <a href="#{{ tag | first | slugize }}">
      {{ tag | first }}
    </a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span>
{% endfor %}
</ul>

<table>
<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    <h2 id="#{{ tag_name | slugize }}"><i class="fa fa-tags" aria-hidden="true"></i> {{ tag_name }}</h2>
    <a name="{{ tag_name | slugize }}"></a>
    {% for post in site.tags[tag_name] %}

        <tr>
      <td width="60%">
        <div class="archive-item2">
        <h5><a href="{{ post.url }}">{{ post.title }} <br> <p> <time>({{ post.date | date:"%y년 %m월 %d일" }})</time></p></a></h5>
        </div>
      </td>
      <td width="40%">
        <div>
          <div class="archive-image2">
          <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ post.image }}" ></a>
        </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
