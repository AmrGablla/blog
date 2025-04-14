---
layout: page
title: Subscribe
permalink: /subscribe/
---

<div class="subscribe-options">
  <h2>Stay Updated with My Blog</h2>
  
  <div class="subscription-option">
    <h3><i class="fa fa-rss"></i> RSS Feed</h3>
    <p>Subscribe to my blog posts via RSS using your favorite feed reader:</p>
    <a href="{{ site.baseurl }}/feed.xml" class="subscribe-button">RSS Feed</a>
    <div class="reader-links">
      <p>Popular RSS readers:</p>
      <ul>
        <li><a href="https://feedly.com/i/discover" target="_blank">Feedly</a></li>
        <li><a href="https://inoreader.com/" target="_blank">Inoreader</a></li>
        <li><a href="https://www.newsblur.com/" target="_blank">NewsBlur</a></li>
      </ul>
    </div>
  </div>
  
  <div class="subscription-option">
    <h3><i class="fa fa-github"></i> GitHub</h3>
    <p>Watch the blog repository on GitHub for updates:</p>
    <a href="https://github.com/{{ site.github_username }}/blog/subscription" target="_blank" class="subscribe-button">Watch on GitHub</a>
  </div>
</div>

<style>
  .subscribe-options {
    max-width: 800px;
    margin: 0 auto;
  }
  
  .subscription-option {
    margin-bottom: 40px;
    padding: 20px;
    border: 1px solid #e8e8e8;
    border-radius: 5px;
    background-color: #f9f9f9;
  }
  
  .subscribe-button {
    display: inline-block;
    padding: 10px 20px;
    margin: 10px 0;
    background-color: #2a7ae2;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    transition: background-color 0.3s;
  }
  
  .subscribe-button:hover {
    background-color: #1756a9;
    text-decoration: none;
  }
  
  .reader-links {
    margin-top: 15px;
    font-size: 0.9em;
  }
  
  .reader-links ul {
    list-style-type: none;
    margin-left: 0;
    padding-left: 0;
  }
  
  .reader-links li {
    display: inline-block;
    margin-right: 15px;
  }
  
  @media (prefers-color-scheme: dark) {
    .subscription-option {
      border-color: #3d3d3d;
      background-color: #2d2d2d;
    }
    
    .subscribe-button {
      background-color: #4dabf7;
    }
    
    .subscribe-button:hover {
      background-color: #3793dd;
    }
  }
</style>