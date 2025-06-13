---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---



{% include base_path %}

<!-- # {{ site.data.cv.basics.name }}
**{{ site.data.cv.basics.label }}**   -->
<!-- Email: {{ site.data.cv.basics.email }}    -->


<h2>Work Experience<h2>
======
{% for work in site.data.cv.work %}
* **{{ work.position }}** - {{ work.company }} ({{ work.startDate }}{% if work.endDate %} - {{ work.endDate }}{% endif %})
  {% if work.summary %}
  * {{ work.summary }}
  {% endif %}
  {% if work.highlights %}
  {% for highlight in work.highlights %}
  * {{ highlight }}
  {% endfor %}
  {% endif %}
{% endfor %}


<h2>Education<h2>
======
{% for edu in site.data.cv.education %}
* **{{ edu.studyType }}** in {{ edu.area }}, {{ edu.institution }} ({{ edu.startDate }}{% if edu.endDate %} - {{ edu.endDate }}{% endif %})
  {% if edu.gpa %}
  * GPA: {{ edu.gpa }}
  {% endif %}
  {% if edu.courses %}
  * Relevant Courses: {{ edu.courses | join: ", " }}
  {% endif %}
{% endfor %}

{% if site.data.cv.skills %}
<h2>Skills<h2>
======
{% for skill in site.data.cv.skills %}
* **{{ skill.name }}**: {{ skill.keywords | join: ", " }}
{% endfor %}
{% endif %}

{% if site.data.cv.awards %}
<h2>Awards & Honors<h2>
======
{% for award in site.data.cv.awards %}
* **{{ award.title }}** - {{ award.awarder }} ({{ award.date }})
  {% if award.summary %}
  * {{ award.summary }}
  {% endif %}
{% endfor %}
{% endif %}

<!-- {% if site.data.cv.volunteer %}
Service & Volunteer Work
======
{% for vol in site.data.cv.volunteer %}
* **{{ vol.position }}** - {{ vol.organization }} ({{ vol.startDate }}{% if vol.endDate %} - {{ vol.endDate }}{% endif %})
  {% if vol.summary %}
  * {{ vol.summary }}
  {% endif %}
{% endfor %}
{% endif %} -->


You can find my CV here: [Download](./assets/cv_2024.pdf)

