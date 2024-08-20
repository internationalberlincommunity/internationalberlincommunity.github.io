---
layout: single
title: "Welcome to International Berlin Community"
permalink: /
---

## Welcome to International Berlin Community

The International Berlin Community (IBC) is dedicated to promoting international understanding, tolerance, cultural exchange, and building an inclusive community in Berlin through social events.

![Community Event](/assets/images/community-event.jpg)

### Our Programs

We offer a variety of programs to engage our community members:

- **Social Events**: Regular gatherings to encourage social interaction and community building.
- **Cultural Festivals**: Celebrating diverse cultures through festivals and events.
- **Educational Workshops**: Offering workshops on various topics to educate and empower community members.
- **Sports Activities**: Organizing sports events to promote physical health and teamwork.

### Upcoming Events

- [Summer Festival - July 1, 2024](/events/2024-07-01-summer-festival/)
- [Cultural Exchange Night - August 15, 2024](/events/2024-08-15-cultural-exchange-night/)

[View All Events](/events/)

### Meet Our Team

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

### Testimonials

> Example update august 10

> "IBC has been a fantastic way to meet new people and learn about different cultures. I highly recommend joining their events!" - John Doe

> "The community at IBC is very welcoming and inclusive. I always have a great time at their programs." - Jane Smith

[Join Us Today](/contact/)
