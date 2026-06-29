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
  <p>This section keeps my semester projects together so the ML, OOP, and future DLD work stays separate from the blog archive. Each card links to the project write-up and the original file when it is available.</p>
</section>

<section class="content-card project-section">
  <p class="section-label">2nd Semester</p>
  <h2>Machine Learning Project</h2>
  <div class="project-grid">
    <article class="project-card">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/uet-library.jpg' | relative_url }}" alt="UET Library building" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">Database Systems + Machine Learning</p>
        <h3>Chronic Kidney Disease Predictor</h3>
        <p>I used a Kaggle dataset with important medical features, trained a logistic regression classifier, and connected the model through a FastAPI backend. This was the project where database work and ML came together in a practical way.</p>
        <div class="project-link-row">
          <a class="read-more" href="{{ '/assets/reports/ckd-project-report.pdf' | relative_url }}" target="_blank" rel="noopener">Project Report</a>
          {% if ckd_post %}<a class="read-more" href="{{ ckd_post.url | relative_url }}">Project Write-up</a>{% endif %}
        </div>
      </div>
    </article>
  </div>
</section>

<section class="content-card project-section">
  <p class="section-label">2nd Semester</p>
  <h2>Object-Oriented Programming Projects</h2>
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
        <img src="{{ '/assets/images/site/uet-convocation-hall.jpg' | relative_url }}" alt="UET Convocation Hall" loading="lazy" decoding="async" />
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
  <p class="section-label">Coming Next</p>
  <h2>Digital Logic Design Project</h2>
  <div class="project-grid">
    <article class="project-card project-card--future">
      <figure class="project-visual">
        <img src="{{ '/assets/images/site/uet-electrical-engineering.jpg' | relative_url }}" alt="UET Electrical Engineering building" loading="lazy" decoding="async" />
      </figure>
      <div class="project-copy">
        <p class="project-kicker">DLD</p>
        <h3>Project files coming soon</h3>
        <p>I will add the DLD project here once the files are ready, so all semester projects can stay organized in one place.</p>
      </div>
    </article>
  </div>
</section>
