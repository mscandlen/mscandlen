---
layout: page
permalink: /projects/
title: Projects
---

<div id="projects">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    
    {% for post in site.categories[category_name]%}
    <article class="post">
        <p><b><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></b> - {{ post.date | date: "%B %Y" }}</p>
        <p class="excerpt">{{ post.excerpt }}<a href="{{ site.baseurl }}{{ post.url }}">Read More</a></p>
      
    </article>
  {% endfor %}
  </div>
{% endfor %}
</div>

