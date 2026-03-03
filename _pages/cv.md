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
* **Ph.D in Computer Science**, Illinois Institute of Technology, Chicago, IL (September 2023 - Present)
  * GPA: 3.84
* **M.S. in Computer Science**, Lewis University, Romeoville, IL (May 2022)
  * GPA: 3.76
  * Concentration: Software Engineering
* **B.S. in Computer Science**, Lakeland University, Plymouth, WI (May 2020)
  * GPA: 3.8

Publications
======

{% for post in site.publications reversed %}
[**{{ post.title }}**]({{ post.url }}) ({{ post.date | date: "%B %Y" }})
<br>{{ post.venue }}
<br>{{ post.type }}
{% endfor %}
  
Positions
======

{% for post in site.positions reversed %}
[**{{ post.title }}**]({{ post.url }}) ({{ post.date | date: "%B %Y" }} - {% if post.date_end %}{{ post.date_end | date: "%B %Y" }}{% else %}Present{% endif %})
<br>{{ post.venue }}
<br>{{ post.type }}
{% endfor %}

<head>
  <link rel="stylesheet" href="../_pages/100-small_custom_style.css">
</head> 


Projects
======

{% include_relative 005-tech_skills.html %}


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
        <p><em>Published: {{ post.venue }}</em></p>
      {% endif %}
    </div>
  {% endfor %}
</div>

