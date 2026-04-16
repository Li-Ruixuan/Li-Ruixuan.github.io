---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

## Courses

{% for item in site.data.teaching.courses %}
### {{ item.title }}
**Role:** {{ item.role }} &nbsp;|&nbsp; **Type:** {{ item.type }} &nbsp;|&nbsp; **Date:** {{ item.date }}  
*{{ item.venue }}*

{{ item.description }}

---
{% endfor %}

## Master Thesis Supervision

{% for thesis in site.data.teaching.theses %}
### {{ thesis.title }}
**Student:** {{ thesis.student }} &nbsp;|&nbsp; **Degree:** {{ thesis.degree }} &nbsp;|&nbsp; **Year:** {{ thesis.year }}  
**Status:** {% if thesis.status == "ongoing" %}🟡 Ongoing{% else %}✅ Completed{% endif %}

{% if thesis.description %}{{ thesis.description }}{% endif %}

---
{% endfor %}