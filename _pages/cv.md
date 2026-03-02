---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /cv
---

{% include base_path %}

Education
======
* **Ph.D in Computer Science**, Illinois Institute of Technology, Chicago, IL (September 2023 – Present)
  * GPA: 3.84
* **M.S. in Computer Science**, Lewis University, Romeoville, IL (May 2022)
  * GPA: 3.76
  * Concentration: Software Engineering
* **B.S. in Computer Science**, Lakeland University, Plymouth, WI (May 2020)
  * GPA: 3.8

Publications
======

{% for post in site.publications reversed %}
**{{ post.title }}**  
<b>Authors</b>: {{ post.excerpt }}  
{{ post.venue }} ({{ post.date | date: "%Y" }})  
{% endfor %}
  
Teaching
======

{% for post in site.teaching reversed %}
**{{ post.title }}** ({{ post.date | date: "%B %Y" }}{% if post.date_end %} – {{ post.date_end | date: "%B %Y" }}{% endif %})
<br>{{ post.venue }}
<br>{{ post.type }}
- Held office hours to help students with questions and homework
- Supported instructors by uploading and managing content on Blackboard
- Worked with instructors to identify students requiring additional assistance
- Monitored discussion board for student questions
- Assisted with grading courses
- Maintained Discord channel for students
{% endfor %}

Professional Experience
======
* **Software Engineer Internship** (June 2021 – October 2021)
  * Cybridge Group, Inc., Tokyo, Japan
  * Developed web and mobile applications using Laravel PHP framework for Android and iOS
  * Enhanced and integrated new features into existing web systems, including debugging and unit testing with Selenium
  * Contributed to pre-market software projects and authored comprehensive documentation
  * Collaborated with clients to refine system requirements and participated in team meetings


Projects
======

<div class="projects-container">
  {% for post in site.projects reversed %}
    <div class="project">
      <h3>{{ post.title }}</h3>
      {% if post.tags %}
        {% for tag in post.tags %}
          <span class="tag tag-{{ tag | slugify }}">{{ tag | capitalize }}</span>
        {% endfor %}
      {% endif %}
      {% if post.technologies %}
        <p><strong>Technologies:</strong> {{ post.technologies }}</p>
      {% endif %}
      <p>
        {{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' | strip }}
      </p>
      {% if post.venue %}
        <p><em>Published/Completed: {{ post.venue }}</em></p>
      {% endif %}
    </div>
  {% endfor %}
</div>

<style>
.skills-header {
  border: 1px solid var(--global-border-color, #d0d7de);
  border-radius: 8px;
  padding: 1.2rem 1.5rem;
  margin-bottom: 2rem;
  background-color: var(--global-bg-color, #f9f9f9); /* light fallback */
  transition: background-color 0.3s ease, border-color 0.3s ease;
}

.skills-tagline {
  margin: 0 0 0.8rem 0;
  color: var(--global-text-color-light, #555);
  font-size: 0.9rem;
  font-style: italic;
}

.skills-grid {
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}

.skill-row {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  font-size: 0.9rem;
  line-height: 1.5;
  align-items: baseline;
}

.skill-cat {
  font-weight: 700;
  color: var(--global-bold-color, #2c3e50);
  min-width: 180px;
  flex-shrink: 0;
  text-align: right;
}

.skill-vals {
  color: var(--global-text-color, #333);
}

/* Dark mode overrides */
html[data-theme="dark"] .skills-header {
  background-color: #222 !important;
  border-color: #444 !important;
}

html[data-theme="dark"] .skills-tagline {
  color: #aaa !important;
}

html[data-theme="dark"] .skill-cat {
  color: #a0c0ff !important; /* light blue accent for category */
}

html[data-theme="dark"] .skill-vals {
  color: #ddd !important;
}

/* Keep your project card styles (just showing the fixed part) */
.project {
  margin-bottom: 1.5rem;
  padding: 1.5rem;
  border: 1px solid var(--global-border-color, #444);
  border-radius: 8px;
  background-color: var(--global-bg-color, #2a2a2a); /* dark fallback */
  transition: background-color 0.3s ease;
}

.project h3 {
  margin-top: 0;
  color: var(--global-bold-color, #ffffff);
  font-size: 1.1rem;
}

.project p {
  margin-bottom: 0.5rem;
  line-height: 1.6;
  color: var(--global-text-color, #e0e0e0);
}

.project p strong {
  color: #a8d0ff; /* light accent for emphasis */
}

.tag {
  display: inline-block;
  font-size: 0.75rem;
  font-weight: 600;
  padding: 0.25rem 0.6rem;
  border-radius: 12px;                /* pill shape — less boxy */
  margin-right: 0.5rem;
  margin-bottom: 0.4rem;
  letter-spacing: 0.02em;
  color: #ffffff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.15); /* subtle depth */
  transition: all 0.2s ease;
}

.tag:hover {
  transform: translateY(-1px);
  box-shadow: 0 3px 6px rgba(0,0,0,0.2);
}


/* Cleaner / more modern colors — not too bright/neon */
.tag-research   { background-color: #0d6efd; }  /* Bootstrap blue */
.tag-published  { background-color: #198754; }  /* success green */
.tag-systems    { background-color: #6f42c1; }  /* purple */
.tag-blockchain { background-color: #cf7b36; }  /* orange */
.tag-software   { background-color: #017890; }  /* cyan */
.tag-game       { background-color: #dc3545; }  /* red */
.tag-web        { background-color: #198754; }  /* green again or #6610f2 purple */
</style>