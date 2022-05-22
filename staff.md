---
layout: page
title: Staff
description: Data 6 Summer 2022 Course Staff.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

## Instructors

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Undergraduate Student Instructors (uGSIs)

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

## Tutors

{% for staffer in tutors %}
{{ staffer }}
{% endfor %}
{% endif %}
