---
permalink: /
title: "Vadim Biryukov"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
layout: single
classes: wide
---

<div style="display:flex;flex-direction:row;align-items:flex-start;gap:2rem;margin-bottom:2rem">
<div style="flex:1;display:flex;flex-direction:column">
<div style="display:flex;gap:1rem;margin-bottom:1.5rem;align-items:center">
<a href="mailto:vbiryukov@hawk.illinoistech.edu" style="color:inherit;font-size:1.5rem;text-decoration:none" title="vbiryukov@hawk.illinoistech.edu">
<i class="fas fa-envelope"></i>
</a>
<a href="https://github.com/VadimBir" target="_blank" style="color:inherit;font-size:1.5rem;text-decoration:none" title="@VadimBir">
<i class="fab fa-github"></i>
</a>
<a href="https://www.linkedin.com/in/vadim-biryukov" target="_blank" style="color:inherit;font-size:1.5rem;text-decoration:none" title="vadim-biryukov">
<i class="fab fa-linkedin"></i>
</a>
</div>

<p style="margin-top:0;line-height:1.6">
Vadim Biryukov is a PhD candidate in the Department of Computer Science at the Illinois Institute of Technology and a member of the Gnosis Research Center. His research specializes in system memory architecture, memory hierarchy optimization, and developing hardware prefetchers for computing systems. He holds an M.S. in Computer Science from Lewis University and a B.S. in Computer Science from Lakeland University.
</p>
</div>

<div style="flex-shrink:0">
<img src="/images/biryukov.jpg" alt="Vadim Biryukov" style="border-radius:16px;width:160px;height:auto">
</div>
</div>

## Research Interests

* System memory architecture
* Memory hierarchy optimization
* Hardware prefetchers
* Computing systems

## Publications

{% if site.publications.size > 0 %}
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
{% else %}
<p>No publications found for <strong>Vadim Biryukov</strong>.</p>
{% endif %}

## Teaching

{% if site.teaching.size > 0 %}
{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}
{% else %}
<p><strong>Lewis University</strong> - Teaching Assistant/Instructor</p>
{% endif %}

## News & Updates

{% if site.posts.size > 0 %}
{% for post in site.posts limit:5 %}
* **{{ post.date | date: "%B %Y" }}**: {{ post.title }}
{% endfor %}
{% else %}
<p>No recent news updates.</p>
{% endif %}