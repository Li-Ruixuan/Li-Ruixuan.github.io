---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

<h2>Courses</h2>
{% for item in site.data.teaching.courses %}
  <h3>{{ item.title }}</h3>
  <p><strong>Role:</strong> {{ item.role }} | <strong>Type:</strong> {{ item.type }} | <strong>Year:</strong> {{ item.date }}<br>
  <em>{{ item.venue }}</em></p>
  <p>{{ item.description }}</p>
  <hr>
{% endfor %}

<h2>Master Thesis Supervision</h2>
{% for thesis in site.data.teaching.theses %}
  <h3>{{ thesis.title }}</h3>
  <p><strong>Student:</strong> {{ thesis.student }} | <strong>Degree:</strong> {{ thesis.degree }} | <strong>Year:</strong> {{ thesis.year }}<br>
  <strong>Status:</strong> {% if thesis.status == "ongoing" %}🟡 Ongoing{% else %}✅ Completed{% endif %}</p>
  {% if thesis.description %}<p>{{ thesis.description }}</p>{% endif %}
  <hr>
{% endfor %}