---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

{% for item in site.data.news %}
**{{ item.date }}** — {{ item.title }}

{{ item.description }}
{% if item.link %}[Read more]({{ item.link }}){% endif %}

---
{% endfor %}