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
    
    <h2 class="category-head">{{ category_name }}</h2>
    <a name="{{ category_name | slugize }}"></a>
    
    {% for post in site.categories[category_name]%}
    <article class="post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <h3>{{ post.title }}</h3>
        <div>
          <p class="post_date">{{ post.date | date: "%B %Y" }}</p>
        </div>
      </a>
      
      <div class="excerpt">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
  </div>
{% endfor %}
</div>

