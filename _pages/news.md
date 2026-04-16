

---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

{% if site.data.news %}
{% for item in site.data.news %}
<div>
  <strong>{{ item.date }}</strong> — {{ item.text }}
</div>
{% endfor %}
{% else %}
No news yet.
{% endif %}
