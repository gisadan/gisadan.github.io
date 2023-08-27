---
layout: page
title: <i class="fa fa-archive fa-lg"> </i> Archive
---

<style>
  .tb { border-collapse: collapse; width:640px; }
  .tb th, .tb td { padding: 5px; border: solid 1px #777; }
  .tb th { background-color: lightblue; }
</style>

<table>
<div id="tag-cloud">
  {% for post in site.posts %}
  {% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
  {% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
  {% if month != nmonth %}
  {% if forloop.index != 1 %}{% endif %}
  {% endif %}
  
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
  </div>
  {% endfor %}

