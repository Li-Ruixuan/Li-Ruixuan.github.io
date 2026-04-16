---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

<h2>Master Thesis Supervision</h2>
{% for thesis in site.data.teaching.theses %}
  <h3>{{ thesis.title }}</h3>
  <strong>Student:</strong> {{ thesis.student }} <br>
  <strong>Year:</strong> {{ thesis.year }}, <strong>Degree:</strong> {{ thesis.degree }}<br> 
  <strong>Description:</strong> {{ thesis.description }}</p>
  <hr>
{% endfor %}

<h2>Courses</h2>
{% for item in site.data.teaching.courses %}
  <h3>{{ item.title }}, {{ item.date }}</h3> 
  <strong>Role:</strong> {{ item.role }}, <em>{{ item.venue }}</em><br>
  <strong>Description:</strong> {{ item.description }}</p>
  <hr>
{% endfor %}

