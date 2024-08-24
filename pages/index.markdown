---
layout: default
title: "Welcome to International Berlin Community"
permalink: /
---

<div class="content-section">
  <div class="page-header">
    <h1>Our programs</h1>
  </div>

  <!-- Slideshow Section -->
  <section>
    <div class="slideshow-container">
      <div class="prev" onclick="plusSlides(-1)">&#10094;</div>
      
      <div class="mySlides fade" onclick="window.location.href='/programs/#hiking'">
        <img src="/assets/images/hiking.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Hiking</div>
        </div>
      </div>

      <div class="mySlides fade" onclick="window.location.href='/programs/#languageExchange'">
        <img src="/assets/images/languageExchange.jpeg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Language Exchange</div>
        </div>
      </div>
      
      <div class="mySlides fade" onclick="window.location.href='/programs/#picnic'">
        <img src="/assets/images/picnic.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Picnic</div>
        </div>
      </div>

      <div class="mySlides fade" onclick="window.location.href='/programs/#museum'">
        <img src="/assets/images/museum.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Museum Visits</div>
        </div>
      </div>

      <div class="mySlides fade" onclick="window.location.href='/programs/#dayTrips'">
        <img src="/assets/images/dayTrips.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Day Trips</div>
        </div>
      </div>

      <div class="mySlides fade" onclick="window.location.href='/programs/#beachDay'">
        <img src="/assets/images/beachDay.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Beach Days</div>
        </div>
      </div>

      <div class="mySlides fade" onclick="window.location.href='/programs/#culturalEvents'">
        <img src="/assets/images/culturalEvents.jpg" class="slideshow-image">
        <div class="text-overlay">
          <div class="text">Cultural Events</div>
        </div>
      </div>

      <div class="next" onclick="plusSlides(1)">&#10095;</div>
    </div>
    <br>
    <div style="text-align:center">
      <span class="dot" onclick="currentSlide(1)"></span> 
      <span class="dot" onclick="currentSlide(2)"></span> 
      <span class="dot" onclick="currentSlide(3)"></span> 
      <span class="dot" onclick="currentSlide(4)"></span> 
      <span class="dot" onclick="currentSlide(5)"></span> 
      <span class="dot" onclick="currentSlide(6)"></span> 
      <span class="dot" onclick="currentSlide(7)"></span> 
    </div>
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

<script>
let slideIndex = 0;
showSlides();

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides() {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  slideIndex++;
  if (slideIndex > slides.length) {slideIndex = 1}    
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
  setTimeout(showSlides, 7000); // Change image every 4 seconds
}

// Toggle dark mode
function toggleDarkMode() {
  document.body.classList.toggle("dark-mode");
}
</script>
