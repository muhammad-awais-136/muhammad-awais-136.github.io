---
layout: default
title: Blog
permalink: /blog/
---

<section class="content-card">
  <p class="section-label">Blog</p>
  <h2>My Journey Folders</h2>
  <p>This page groups my computer engineering journey into semester folders. Open a folder to see only the related posts on the same page.</p>
</section>

<section class="media-panel">
  <div class="content-card media-copy">
    <p class="section-label">Folders</p>
    <h2>Study by semester, life by moments</h2>
    <p>The archive is arranged into eight semester folders and one separate hostel and campus life folder, so each part of the journey stays easy to find.</p>
  </div>
  <figure class="feature-visual">
    <img src="{{ '/assets/images/site/uet-library.jpg' | relative_url }}" alt="UET Library building" loading="lazy" decoding="async" />
    <figcaption>UET Library, representing study, reflection, and steady learning. <a href="https://commons.wikimedia.org/wiki/File:UET_Library.jpg">Photo source</a></figcaption>
  </figure>
</section>

{% assign semester_1_slugs = "my-goal-to-join-uet,first-semester-subjects,no-programming-background,difficulty-in-learning,my-effort-and-consistency,first-semester-result,my-first-semester-journey,my-current-mindset,my-future-goals" | split: "," %}
{% assign semester_2_slugs = "restarting-my-second-semester,working-for-a-better-grade,normalization-and-linear-regression,online-classes-and-staying-connected,oop-four-pillars-and-labs,university-admission-system-project,brick-breaker-game-project,ckd-predictor-database-project,dld-fire-and-smoke-alarm,final-week-before-exams,health-pressure-and-consistency,semester-reflection-and-results" | split: "," %}
{% assign life_slugs = "moving-from-shorkot-to-faisalabad,hostel-life-challenges,adjusting-to-hostel-life" | split: "," %}

{% assign semester_1_count = 0 %}
{% assign semester_2_count = 0 %}
{% assign life_count = 0 %}

{% for post in site.posts %}
  {% if semester_1_slugs contains post.slug %}
    {% assign semester_1_count = semester_1_count | plus: 1 %}
  {% endif %}
  {% if semester_2_slugs contains post.slug %}
    {% assign semester_2_count = semester_2_count | plus: 1 %}
  {% endif %}
  {% if life_slugs contains post.slug %}
    {% assign life_count = life_count | plus: 1 %}
  {% endif %}
{% endfor %}

<section class="folder-board">
  <a class="folder-card folder-card--active" href="#folder-semester-1">
    <p class="folder-label">Folder 1</p>
    <h3>1st Semester</h3>
    <p>Early university adjustment, programming basics, discipline, and the first lessons that shaped my foundation.</p>
    <div class="folder-meta">
      <span>{{ semester_1_count }} Articles</span>
      <span>2025 to early 2026</span>
    </div>
  </a>

  <a class="folder-card folder-card--active" href="#folder-semester-2">
    <p class="folder-label">Folder 2</p>
    <h3>2nd Semester</h3>
    <p>Online learning, labs, projects, machine learning, database work, and the pressure before final exams.</p>
    <div class="folder-meta">
      <span>{{ semester_2_count }} Articles</span>
      <span>March to June 2026</span>
    </div>
  </a>

  {% assign future_semesters = "3,4,5,6,7,8" | split: "," %}
  {% for semester in future_semesters %}
    <a class="folder-card folder-card--future" href="#folder-future">
      <p class="folder-label">Folder {{ semester }}</p>
      <h3>Semester {{ semester }}</h3>
      <p>Reserved for the next stage of the journey. This folder will open as the portfolio grows.</p>
      <div class="folder-meta">
        <span>0 Articles</span>
        <span>Coming soon</span>
      </div>
    </a>
  {% endfor %}

  <a class="folder-card folder-card--active" href="#folder-life">
    <p class="folder-label">Folder 9</p>
    <h3>Hostel &amp; Campus Life</h3>
    <p>Moving, hostel adjustment, daily routines, and the moments outside the classroom that still shaped the journey.</p>
    <div class="folder-meta">
      <span>{{ life_count }} Articles</span>
      <span>Life stories</span>
    </div>
  </a>
</section>

<section class="folder-section content-card" id="folder-semester-1">
  <p class="section-label">Folder 1</p>
  <h2>1st Semester</h2>
  <p>These posts show how the journey started, how the first semester felt, and how the early university routine slowly shaped my approach to learning.</p>
  <div class="posts-grid">
    {% for post in site.posts reversed %}
      {% if semester_1_slugs contains post.slug %}
        <article class="post-preview-card">
          {% assign cover = post.image | default: '/assets/images/posts/default-post-cover.svg' %}
          <a class="post-cover-link" href="{{ post.url | relative_url }}">
            <img class="post-cover" src="{{ cover | relative_url }}" alt="{{ post.image_alt | default: post.title }}" loading="lazy" decoding="async" />
          </a>
          <div class="post-preview-copy">
            <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt | strip_html | truncate: 170 }}</p>
            <a class="read-more" href="{{ post.url | relative_url }}">Read full post</a>
          </div>
        </article>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="folder-section content-card" id="folder-semester-2">
  <p class="section-label">Folder 2</p>
  <h2>2nd Semester</h2>
  <p>This folder keeps all second-semester posts together so the learning path, project work, online classes, and exam pressure are easy to follow in one place.</p>
  <div class="posts-grid">
    {% for post in site.posts reversed %}
      {% if semester_2_slugs contains post.slug %}
        <article class="post-preview-card">
          {% assign cover = post.image | default: '/assets/images/posts/default-post-cover.svg' %}
          <a class="post-cover-link" href="{{ post.url | relative_url }}">
            <img class="post-cover" src="{{ cover | relative_url }}" alt="{{ post.image_alt | default: post.title }}" loading="lazy" decoding="async" />
          </a>
          <div class="post-preview-copy">
            <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt | strip_html | truncate: 170 }}</p>
            <a class="read-more" href="{{ post.url | relative_url }}">Read full post</a>
          </div>
        </article>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="folder-section content-card" id="folder-life">
  <p class="section-label">Folder 9</p>
  <h2>Hostel &amp; Campus Life</h2>
  <p>This folder keeps the non-semester journey together, including hostel adjustment and the everyday moments that shaped university life outside class.</p>
  <div class="posts-grid">
    {% for post in site.posts reversed %}
      {% if life_slugs contains post.slug %}
        <article class="post-preview-card">
          {% assign cover = post.image | default: '/assets/images/posts/default-post-cover.svg' %}
          <a class="post-cover-link" href="{{ post.url | relative_url }}">
            <img class="post-cover" src="{{ cover | relative_url }}" alt="{{ post.image_alt | default: post.title }}" loading="lazy" decoding="async" />
          </a>
          <div class="post-preview-copy">
            <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt | strip_html | truncate: 170 }}</p>
            <a class="read-more" href="{{ post.url | relative_url }}">Read full post</a>
          </div>
        </article>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="content-card folder-section" id="folder-future">
  <p class="section-label">Folders 3 to 8</p>
  <h2>Future Semesters</h2>
  <p>These folders are kept visible now so the structure stays ready for the next semesters. As the portfolio grows, each one can be filled with its own stage of the journey.</p>
  <div class="future-folder-grid">
    {% for semester in future_semesters %}
      <article class="future-folder-card">
        <p class="folder-label">Folder {{ semester }}</p>
        <h3>Semester {{ semester }}</h3>
        <p>Reserved for later posts.</p>
      </article>
    {% endfor %}
  </div>
</section>
