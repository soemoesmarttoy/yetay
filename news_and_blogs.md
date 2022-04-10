---
layout: home
page_title: News & Blogs
permalink: /news_and_blogs/
---
<div class="row row-cols-1 row-cols-md-3 g-4 mt-4">
{% for post in site.posts %}
<div class="col">
<div class="card" style="width: 18rem;">
{% for file in site.static_files %}
    {% if (file.basename == post.title) %}
  <img src="{{ file.path | relative_url }}" class="card-img-top" alt="{{ file.name }}">
    {% endif %}
{% endfor %}
  <div class="card-body">
    <h5 class="card-title">{{ post.title }}</h5>
    <p class="card-text">{{ post.description }}</p>
    <a href="{{post.url}}" class="btn btn-dark">Read More</a>
  </div>
</div>
</div>
{% endfor %}
</div>
