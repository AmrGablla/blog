---
layout: page
title: Archives
permalink: /archives/
---

<div class="archives">
  {% for post in site.posts %}
    {% assign currentdate = post.date | date: "%Y" %}
    {% if currentdate != date %}
      {% unless forloop.first %}</ul>{% endunless %}
      <h2 id="y{{post.date | date: "%Y"}}">{{ currentdate }}</h2>
      <ul class="post-list">
      {% assign date = currentdate %}
    {% endif %}
    <li>
      <span class="post-meta">
        {{ post.date | date: "%b %-d" }}
        {% if post.tags.size > 0 %}
        • 
        {% for tag in post.tags %}
          <a href="{{ site.baseurl }}/tags/#{{ tag | slugify }}" class="post-tag">{{ tag }}</a>
        {% endfor %}
        {% endif %}
      </span>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% if forloop.last %}</ul>{% endif %}
  {% endfor %}
</div>

<style>
  .archives h2 {
    margin-top: 30px;
    padding-bottom: 10px;
    border-bottom: 1px solid #e8e8e8;
  }
  
  .archives .post-list {
    margin-left: 0;
    list-style: none;
  }
  
  .archives .post-list > li {
    margin-bottom: 10px;
  }
  
  .archives .post-meta {
    font-size: 14px;
    color: #828282;
    display: inline-block;
    min-width: 120px;
  }
  
  .archives .post-link {
    display: inline;
    font-size: 16px;
  }
  
  .archives .post-tag {
    display: inline-block;
    padding: 0 5px;
    margin-right: 2px;
    background-color: #f0f0f0;
    border-radius: 3px;
    font-size: 0.7em;
    color: #333;
    text-decoration: none;
  }
  
  @media (prefers-color-scheme: dark) {
    .archives h2 {
      border-bottom-color: #3d3d3d;
    }
    
    .archives .post-tag {
      background-color: #3d3d3d;
      color: #eee;
    }
  }
</style>