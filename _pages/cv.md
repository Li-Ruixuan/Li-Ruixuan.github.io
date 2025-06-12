---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---



{% include base_path %}

# {{ site.data.cv.basics.name }}
**{{ site.data.cv.basics.label }}**  
Email: {{ site.data.cv.basics.email }}  
Website: {{ site.data.cv.basics.website }}

Education
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

Work Experience
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

{% if site.data.cv.skills %}
Skills
======
{% for skill in site.data.cv.skills %}
* **{{ skill.name }}**: {{ skill.keywords | join: ", " }}
{% endfor %}
{% endif %}

{% if site.data.cv.awards %}
Awards & Honors
======
{% for award in site.data.cv.awards %}
* **{{ award.title }}** - {{ award.awarder }} ({{ award.date }})
  {% if award.summary %}
  * {{ award.summary }}
  {% endif %}
{% endfor %}
{% endif %}

Publications
======
{% if site.data.cv.publications %}
{% for pub in site.data.cv.publications %}
* {{ pub.name }} ({{ pub.releaseDate }})
  {% if pub.summary %}
  * {{ pub.summary }}
  {% endif %}
{% endfor %}
{% else %}
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endif %}

{% if site.data.cv.volunteer %}
Service & Volunteer Work
======
{% for vol in site.data.cv.volunteer %}
* **{{ vol.position }}** - {{ vol.organization }} ({{ vol.startDate }}{% if vol.endDate %} - {{ vol.endDate }}{% endif %})
  {% if vol.summary %}
  * {{ vol.summary }}
  {% endif %}
{% endfor %}
{% endif %}

{% if site.data.cv.interests %}
Research Interests
======
{% for interest in site.data.cv.interests %}
* {{ interest.name }}{% if interest.keywords %}: {{ interest.keywords | join: ", " }}{% endif %}
{% endfor %}
{% endif %}