---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a postdoctoral researcher in the Department of Mechanical Engineering, working on the development of robot ultrasound system for surgery.


{% if site.data.cv.interests %}
<h2>Research Interests<h2>
======
{% for interest in site.data.cv.interests %}
* {{ interest.name }}{% if interest.keywords %}: {{ interest.keywords | join: ", " }}{% endif %}
{% endfor %}
{% endif %}



<!-- News Section -->
<h2 style="margin-top: 40px; color: #2c3e50;">📰 Recent News</h2>
<div style="max-height: 400px; overflow-y: auto; border: 1px solid #e0e0e0; border-radius: 8px; padding: 15px; background-color: #fafafa;">
  {% assign recent_news = site.data.news | sort: 'date' | reverse | slice: 0, 8 %}
  {% for item in recent_news %}
  <div style="margin-bottom: 20px; padding: 15px; background-color: white; border-radius: 6px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); {% if item.highlight %}border-left: 4px solid #3498db;{% endif %}">
    
    <!-- Date and Type Badge -->
    <div style="margin-bottom: 8px;">
      <span style="color: #7f8c8d; font-size: 0.9em; font-weight: 500;">
        {{ item.date | date: "%B %d, %Y" }}
      </span>
      
      {% if item.type %}
      <span style="
        background-color: 
        {% case item.type %}
        {% when 'publication' %}#27ae60
        {% when 'award' %}#f39c12
        {% when 'conference' %}#8e44ad
        {% when 'preprint' %}#16a085
        {% when 'career' %}#e74c3c
        {% else %}#95a5a6
        {% endcase %}
        ; color: white; padding: 2px 8px; border-radius: 12px; font-size: 0.8em; margin-left: 10px;">
        {{ item.type | capitalize }}
      </span>
      {% endif %}
      
      {% if item.highlight %}
      <span style="background-color: #3498db; color: white; padding: 2px 8px; border-radius: 12px; font-size: 0.8em; margin-left: 5px;">
        ⭐ Featured
      </span>
      {% endif %}
    </div>
    
    <!-- Title -->
    <h4 style="margin: 0 0 8px 0; color: #2c3e50;">
      {% if item.link %}
      <a href="{{ item.link }}" style="text-decoration: none; color: #2c3e50;">{{ item.title }}</a>
      {% else %}
      {{ item.title }}
      {% endif %}
    </h4>
    
    <!-- Description -->
    <p style="margin: 0; color: #555; line-height: 1.4;">{{ item.description }}</p>
    
    {% if item.link %}
    <a href="{{ item.link }}" style="color: #3498db; text-decoration: none; font-size: 0.9em;">Read more →</a>
    {% endif %}
  </div>
  {% endfor %}
</div>

<!-- Archive Link -->
<div style="text-align: center; margin-top: 15px;">
  <a href="/news/" style="color: #3498db; text-decoration: none; font-weight: 500;">View All News →</a>
</div>
