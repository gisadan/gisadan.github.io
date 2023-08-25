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

      

      <table>              
        <tr>
          <td width="60%">
            <div class="archive-item2">
            <p><a href="{{ post.url }}">{{ post.title }}</a> <time>({{ post.date | date:"%d %b" }})</time></p>
            </div>
          </td>
          <td width="40%">
            <div>
              <div class="related-image">
              <img src="{{ post.image }}" ></a>
            </div>
          </td>
        </tr>
      </table>
      

  {% endfor %}
</div>
</div>
