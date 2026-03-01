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
<h2> About Me</h2>
I am a <b>Computer Science Instructor</b> at <b>Lewis Univeristy</b> where I work at Department of Engineering, Computing and Mathematical Sciences (ECaMS). I am a PhD candidate in the Department of Computer Science at the Illinois Institute of Technology where I work closely with <href src=http://www.cs.iit.edu/~scs/sun/biography.html>Prof. Xian-He Sun</href> at the <href src=https://grc.iit.edu/>Gnosis Research Center</href>. My research is in <b>system memory architecture</b>, <b>memory hierarchy optimization</b> for computer systems.
</p>

<p style="line-height:1.6">
Currently serving as Computer Science Instructor at Lewis University, teaching undergraduate courses: Operating Systems, Computer Organization, Database Systems, Algorithms and Data Structures, Software Systems Capstone, Computer Infrastructure Capstone, Applied Programming Languages, Programming Fundamentals, and Introduction to Computer Science. Previously completed a Software Engineer Internship at Cybridge Group, Inc. (Tokyo, Japan) developing web and mobile applications on Laravel PHP framework.
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
* Efficient KV cache eviction policies for Large Language Models

## Technology Skills

**Programming Languages:** C++, C#, MASM, Java, Python, MySQL, Go, COBOL 
**Web Technologies:** HTML5, CSS, React, JavaScript, Django, Laravel, PHP
<!-- **Web & Blockchain Technologies:** HTML5, CSS, React, JavaScript, Django, Laravel, PHP, Solidity, OpenZeppelin, Web3, Moralis, Python-Selenium, Java-Selenium -->

**Operating Systems & Virtualization:** Linux, Windows, macOS, WSL, VPS, VMware, VirtualBox, Vagrant
<!-- **Operating Systems & Virtualization:** Windows, MacOS X, Linux, WSL, VPS, NAS, iOS, Android, VMWare, VirtualBox, Vagrant -->

**Cloud & Research Infrastructure:** Azure, Digital Ocean, Chameleon Cloud

**Tools & Systems:** ChampSim, Wireshark, Nmap, Metasploit, SQL Server, Google Apps Script, FileZilla, Git

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