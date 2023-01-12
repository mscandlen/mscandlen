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
        <div>
          <a href="{{ site.baseurl }}{{ post.url }}" class="post_title">{{ post.title }}</a> <a class="post_date">{{ post.date | date: "%B %Y" }}</a>
        </div>
      
      <div class="excerpt">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
  </div>
{% endfor %}
</div>

