---
layout: page
title: Destinos
permalink: /destinos/
---

<!-- blog post -->
<section class="section">
  <div class="container">
    <div class="row">
      {% for post in site.destinos reversed %}
      <div class="col-12 mb-100">
        <article data-file="{{ post.url | prepend: site.baseurl }}" data-target="article" class="article-full-width {{class}}">
          <div class="post-image">
            <img class="img-fluid" src="{{post.image | relative_url}}" alt="{{post.title}}">
          </div>
          <div class="post-content">
            <ul class="list-inline d-flex justify-content-between border-bottom post-meta pb-2 mb-4">
              <li class="list-inline-item"><i class="ti-calendar mr-2"></i>{{post.date | date: '%b %d, %Y'}}</li>
              <li class="list-inline-item"><i class="ti-alarm-clock mr-2"></i><span class="eta"></span> read</li>
            </ul>
            <h4 class="mb-4"><a href="{{ post.url | prepend: site.baseurl }}" class="text-dark">{{post.title}}</a></h4>
            <p class="mb-0 post-summary">{{ post.content | strip_html | truncatewords: 35 }}</p>
            <a class="btn btn-transparent mb-4" href="{{ post.url | prepend: site.baseurl }}">Continue...</a>
          </div>
        </article>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
<!-- /blog post -->