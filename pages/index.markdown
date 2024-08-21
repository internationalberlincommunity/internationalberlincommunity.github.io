---
layout: single
title: "Welcome to International Berlin Community"
permalink: /
---

<div class="page-header">
  <h1>Welcome to International Berlin Community</h1>
  <p>The International Berlin Community (IBC) is dedicated to promoting international understanding, tolerance, cultural exchange, and building an inclusive community in Berlin through social events.</p>
</div>

<div class="content-section">
  <h2>Our Programs</h2>
  <ul>
    <li><strong>Social Events</strong>: Regular gatherings to encourage social interaction and community building.</li>
    <li><strong>Cultural Festivals</strong>: Celebrating diverse cultures through festivals and events.</li>
    <li><strong>Educational Workshops</strong>: Offering workshops on various topics to educate and empower community members.</li>
    <li><strong>Sports Activities</strong>: Organizing sports events to promote physical health and teamwork.</li>
  </ul>

  <h2>Upcoming Events</h2>
  <ul>
    <li><a href="/events/2024-07-01-summer-festival/">Summer Festival - July 1, 2024</a></li>
    <li><a href="/events/2024-08-15-cultural-exchange-night/">Cultural Exchange Night - August 15, 2024</a></li>
  </ul>
  <a href="/events/" class="btn">View All Events</a>

  <h2>Meet Our Team</h2>
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

  <h2>Testimonials</h2>
  <blockquote>
    "IBC has been a fantastic way to meet new people and learn about different cultures. I highly recommend joining their events!" - John Doe
  </blockquote>
  <blockquote>
    "The community at IBC is very welcoming and inclusive. I always have a great time at their programs." - Jane Smith
  </blockquote>
  <a href="/contact/" class="btn">Join Us Today</a>
</div>
