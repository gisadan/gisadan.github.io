---
layout: page
permalink: /category/
title: <i class="fa fa-sitemap fa-lg"> </i> Categories
---


<div id="tag-cloud">
{% for category in site.categories %}
  <div class="archive-group2">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head"><i class="fa fa-folder-open"> </i> {{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <div class="archive-item2">
      <p><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></p>
    </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
