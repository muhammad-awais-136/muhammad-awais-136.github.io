---
layout: default
title: Projects
permalink: /projects/
---

{% assign ckd_post = site.posts | where: "slug", "ckd-predictor-database-project" | first %}
{% assign admission_post = site.posts | where: "slug", "university-admission-system-project" | first %}
{% assign brick_post = site.posts | where: "slug", "brick-breaker-game-project" | first %}

<section class="content-card">
  <p class="section-label">Projects</p>
  <h2>Semester Level Projects</h2>
  <p>This section keeps my semester projects together so the ML, OOP, and DLD work stays separate from the blog archive. ML was taught by Dr. Bilal Ahmad, OOP projects were guided by Mam Rimsha, and DLD was taught by Sir Abdullah Bilal. Each card links to the project write-up and the original file when it is available.</p>
</section>

<section class="content-card project-section">
  <p class="section-label">2nd Semester</p>
  <h2>Machine Learning Project</h2>
  <div class="project-grid">
    <article class="project-card">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/kidney-disease-predictor.png' | relative_url }}" alt="Kidney Disease Predictor interface" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">Database Systems + Machine Learning</p>
        <h3>Kidney Disease Predictor</h3>
        <p>I used a Kaggle dataset with important medical features, trained the model for disease prediction, and connected the backend so the interface could work like a proper CKD early detection system.</p>
        <div class="project-link-row">
          <a class="read-more" href="{{ '/assets/projects/ml/kidney-disease-project-report.docx' | relative_url }}" target="_blank" rel="noopener">Project Report</a>
          {% if ckd_post %}<a class="read-more" href="{{ ckd_post.url | relative_url }}">Project Write-up</a>{% endif %}
        </div>
      </div>
    </article>
  </div>
</section>

<section class="content-card project-section">
  <p class="section-label">2nd Semester</p>
  <h2>Object-Oriented Programming Projects</h2>
  <p class="project-teacher-note">These projects were taught and guided by Mam Rimsha.</p>
  <div class="project-grid">
    <article class="project-card">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/uet-main-block.jpg' | relative_url }}" alt="UET Lahore main block" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">OOP Mini Project</p>
        <h3>University Admission System</h3>
        <p>This mini project focused on building an organized admission flow instead of only writing theory. It helped me think about classes, data handling, and how a real system should behave.</p>
        <div class="project-link-row">
          <a class="read-more" href="{{ '/assets/projects/oop/university-admission-system-report.docx' | relative_url }}" target="_blank" rel="noopener">Project Report</a>
          {% if admission_post %}<a class="read-more" href="{{ admission_post.url | relative_url }}">Project Write-up</a>{% endif %}
        </div>
      </div>
    </article>

    <article class="project-card">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/brick-breaker-game.png' | relative_url }}" alt="Brick Breaker game screen" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">OOP GUI Project</p>
        <h3>Brick Breaker Game</h3>
        <p>I built this 2D GUI game in Python and VS Code, and it made the semester feel more practical because I could see the game logic working on screen. It also gave me a clear hands-on feel for interaction, movement, and debugging.</p>
        <div class="project-link-row">
          <a class="read-more" href="{{ '/assets/projects/oop/brick-breaker-game-report.docx' | relative_url }}" target="_blank" rel="noopener">Project Report</a>
          <a class="read-more" href="{{ '/assets/projects/oop/brick-breaker.slnx' | relative_url }}">Open in Visual Studio</a>
          {% if brick_post %}<a class="read-more" href="{{ brick_post.url | relative_url }}">Project Write-up</a>{% endif %}
        </div>
      </div>
    </article>
  </div>
</section>

<section class="content-card project-section">
  <p class="section-label">3rd Semester</p>
  <h2>Digital Logic Design Project</h2>
  <p class="project-teacher-note">This project was taught by Sir Abdullah Bilal.</p>
  <div class="project-grid">
    <article class="project-card">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/uet-electrical-engineering.jpg' | relative_url }}" alt="UET Electrical Engineering building" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">DLD</p>
        <h3>Fire and Smoke Alarm</h3>
        <p>This DLD project was taught by Sir Abdullah Bilal and focused on a practical alarm system design. I kept the report here so the project section stays complete and easy to follow.</p>
        <div class="project-link-row">
          <a class="read-more" href="{{ '/assets/projects/dld/dld-project-report.docx' | relative_url }}" target="_blank" rel="noopener">Project Report</a>
        </div>
      </div>
    </article>
  </div>
</section>
