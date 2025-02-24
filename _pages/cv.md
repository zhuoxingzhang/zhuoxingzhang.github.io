---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D, the University of Auckland, 2023 - present
* M.S., Southwest University, 2016 - 2019
* B.S., South-Central Minzu University, 2012 - 2016

  
Skills
======
* Database expert
  * Data normalization
  * Normal forms
* Data mining
  * Log anomaly detection via deep learning
* Programming 
  * Java
  * Python
  * Pytorch

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* ICDE reviewer
