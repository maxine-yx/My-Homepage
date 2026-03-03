---
title: "Publications"
permalink: /publications/
layout: single
author_profile: true
---

## Conference Papers

{% for post in site.publications reversed %}
  {% if post.status == "accepted" %}
  <div class="publication-item">
    <h3><a href="{{ post.paperurl }}">{{ post.title }}</a></h3>
    <p><strong>Authors:</strong> {{ post.authors }}</p>
    <p><strong>Venue:</strong> {{ post.venue }}</p>
    <p><strong>Status:</strong> {{ post.status | capitalize }}</p>
    {% if post.codeurl %}
    <p><strong>Code:</strong> <a href="{{ post.codeurl }}">GitHub Repository</a></p>
    {% endif %}
    <p>{{ post.excerpt }}</p>
  </div>
  <hr>
  {% endif %}
{% endfor %}

## Preprints & Under Review

{% for post in site.publications reversed %}
  {% if post.status == "preprint" or post.status == "under review" %}
  <div class="publication-item">
    <h3><a href="{{ post.paperurl }}">{{ post.title }}</a></h3>
    <p><strong>Authors:</strong> {{ post.authors }}</p>
    <p><strong>Status:</strong> {{ post.status | capitalize }}</p>
    {% if post.codeurl %}
    <p><strong>Code:</strong> <a href="{{ post.codeurl }}">GitHub Repository</a></p>
    {% endif %}
    <p>{{ post.excerpt }}</p>
  </div>
  <hr>
  {% endif %}
{% endfor %}