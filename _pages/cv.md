---
layout: archive
title: "<h1 style='font-size: 42px; border-bottom: 3px solid #2c3e50; margin-bottom: 1.5rem;'>CV</h1>"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
<style>
  /* 增强标题层级对比 */
  h2 {
    font-size: 32px !important;  /* Education 标题大小 */
    color: #34495e;
    margin-top: 2rem;
  }
</style>
## Education
======
* Ph.D in Computer Science, the University of Auckland, 2023 - present
* M.S. in Software Engineering, Southwest University, 2016 - 2019
* B.S. in Software Engineering, South-Central Minzu University, 2012 - 2016

  
## Skills
======
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
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
   
## Service and leadership
======
* ICDE reviewer
