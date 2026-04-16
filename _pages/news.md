---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

{% for item in site.data.news %}
**{{ item.date }}** — {{ item.title }}


<p><strong>Description:</strong> {{ item.description }}</p>
{% if item.link %}[Read more]({{ item.link }}){% endif %}

---
{% endfor %}