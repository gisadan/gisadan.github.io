---
layout: page
permalink: /category/
title: <i class="fa fa-sitemap fa-lg"> </i> Categories
---

<table>

<div id="tag-cloud">
{% for category in site.categories %}
  <div class="archive-group2">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h2 class="category-head"><i class="fa fa-folder-open"> </i> {{ category_name }}</h2>
    <a name="{{ category_name | slugize }}"></a>

    {% for post in site.categories[category_name] %}
    
    <tr>
      <td width="60%">
        <div class="archive-item2">
        <h5><a href="{{ post.url }}">{{ post.title }} <br> <p> <time>({{ post.date | date:"%y년 %m월 %d일" }})</time></p></a></h5>
        </div>

      <td width="40%">
        <div>
          <div class="archive-image2">
          <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ post.image }}" ></a>
        </div>


    {% endfor %}
  </div>
{% endfor %}
</div>
