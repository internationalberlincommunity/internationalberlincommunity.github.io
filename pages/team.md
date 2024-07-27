---
layout: single
title: "Meet Our Team"
permalink: /team/
---

## Meet Our Team

<div class="team">
  {% for member in site.data.team %}
  <div class="team-member">
    <a href="{{ member.link }}"><img src="{{ member.photo }}" alt="{{ member.name }}"></a>
    <h3><a href="{{ member.link }}">{{ member.name }}</a></h3>
    <p>{{ member.bio }}</p>
    <div class="team-member-links">
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank"><i class="fab fa-linkedin"></i></a>
      {% endif %}
      {% if member.email %}
      <a href="mailto:{{ member.email }}"><i class="fas fa-envelope"></i></a>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>
