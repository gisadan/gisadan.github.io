---
layout: page
title: Search <i class="fa fa-search fa-3x"></i>
permalink: /search2/
---
<div id="tag-cloud">
<div id="results">
  <h1><!-- `key` listing for `value` --></h1>

  <ul class="results">
    <!-- results lists -->
  </ul>
</div>

<!— Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" placeholder="Search...">
<ul id="results-container"></ul>
</div>

<!-- Script pointing to jekyll-search.js -->
<script src="{{site.baseurl}}/dest/jekyll-search.js" type="text/javascript"></script>


<script type="text/javascript">
      SimpleJekyllSearch({
        searchInput: document.getElementById('search-input'),
        resultsContainer: document.getElementById('results-container'),
        json: '{{ site.baseurl }}/search2.json',
        searchResultTemplate: '<p><a href="{url}" title="{desc}">{title}</a></p>',
        noResultsText: 'No results found',
        limit: 10,
        fuzzy: false,
        exclude: ['Welcome']
      })
</script>
</div>
<br><br><br><br><br><br><br><br><br>
