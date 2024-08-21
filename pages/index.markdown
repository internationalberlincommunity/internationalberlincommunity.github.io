---
layout: default
title: "Welcome to International Berlin Community"
permalink: /
---

<div class="content-section"> <!-- Merged content div -->
  <div class="page-header">
    <h1>Welcome to International Berlin Community</h1>
    <p>Promoting international understanding, tolerance, and cultural exchange in Berlin through social events.</p>
  </div>

  <section>
    <h2>Our Programs</h2>
    <ul class="program-list">
      <li><strong>Social Events</strong>: Regular gatherings to encourage social interaction and community building.</li>
      <li><strong>Cultural Festivals</strong>: Celebrating diverse cultures through festivals and events.</li>
      <li><strong>Educational Workshops</strong>: Offering workshops on various topics to educate and empower community members.</li>
      <li><strong>Sports Activities</strong>: Organizing sports events to promote physical health and teamwork.</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section>
    <h2>Upcoming Events</h2>
    <ul class="event-list">
      <li><a href="/events/2024-07-01-summer-festival/">Summer Festival - July 1, 2024</a></li>
      <li><a href="/events/2024-08-15-cultural-exchange-night/">Cultural Exchange Night - August 15, 2024</a></li>
    </ul>
    <p><a href="/events/">View All Events</a></p>
  </section>

  <hr class="section-divider">

  <section>
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
  </section>

  <hr class="section-divider">

  <section>
    <h2>Testimonials</h2>
    <blockquote>
      "IBC has been a fantastic way to meet new people and learn about different cultures. I highly recommend joining their events!" - John Doe
    </blockquote>
    <blockquote>
      "The community at IBC is very welcoming and inclusive. I always have a great time at their programs." - Jane Smith
    </blockquote>
  </section>
</div>
