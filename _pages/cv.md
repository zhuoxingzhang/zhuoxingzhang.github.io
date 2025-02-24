---
layout: archive
title: "<h1 style='font-size: 52px; border-bottom: 10px solid #2c3e50; margin-bottom: 2rem;'>CV</h1>"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
<style>
  h2 {
    font-size: 32px !important;  /* subtitle size */
    color: #34495e;
    margin-top: 2rem;
  }
</style>
## Education
* Ph.D in Computer Science, the University of Auckland, 2023 - present
* M.S. in Software Engineering, Southwest University, 2016 - 2019
* B.S. in Software Engineering, South-Central Minzu University, 2012 - 2016

  
## Skills
* Database Expert
  * Data Normalization
  * Normal Forms
* Data Mining
  * Log Anomaly Detection via Deep Learning
* Programming 
  * Java
  * Python
  * Pytorch

## Publications
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
   
## Service and leadership
* ICDE reviewer
