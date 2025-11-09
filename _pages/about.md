---
permalink: /
author_profile: true
---

<!-- 🧠 Short Bio -->
<h1 id="short-bio">Short Bio</h1>
<p class="justify">
&emsp;&emsp;I am currently pursuing a PhD in Computer Science at the University of Auckland since 2023. Previously, I was a visiting student at Southwest University during 2019 - 2022. Prior to that, I completed an MSc in Software Engineering at Southwest University in 2019 and a BSc in Software Engineering at South-Central Minzu University in 2016. My current research focuses on relational databases and anomaly detection from system logs.<br> 
&emsp;&emsp;Specifically, my work mainly consists of the following areas:
</p>

<!-- 🌱 Short Bio 列表 -->
<ul class="bio-list">
  <li><i>Schema Design Optimization</i>: Developing novel normalization algorithms to minimize data redundancy and improve update efficiency while preserving functional dependencies.</li>
  <li><i>Update Cost Reduction</i>: Quantifying the trade-offs between normalization levels and update overheads in database systems.</li>
  <li><i>Mining FDs/Keys from Data</i>: Mining meaningful Functional Dependencies/Keys from data with domain expert knowledge.</li>
  <li><i>Detecting Anomalies from System Logs</i>: Mining anomalous patterns from system logs to find root causes via deep learning techniques.</li>
</ul>
<p class="justify">
If you are interested in exploring possible collaborations, please don’t hesitate to reach out.
</p>

---

<!-- 🧾 Selected Publications -->
<h1 id="publications">Publications</h1>
<div class="wordwrap">You can also find all my papers on my <a href="https://dblp.org/pid/223/8303.html" target="_blank">DBLP</a> profile.</div>

<!-- 📚 Publications 列表 -->
<ul class="pub-list">
{% for pub in site.data.pubs %}
  {% assign authors = pub.authors | split: ',' %}
  {% assign formatted_authors = "" %}

  {% for a in authors %}
    {% assign author = a | strip %}
    {% if author == "Zhuoxing Zhang" %}
      {% assign formatted_authors = formatted_authors | append: "<strong>" | append: author | append: "</strong>" %}
    {% else %}
      {% assign formatted_authors = formatted_authors | append: author %}
    {% endif %}
    {% unless forloop.last %}
      {% assign formatted_authors = formatted_authors | append: ", " %}
    {% endunless %}
  {% endfor %}

  <li>
    <i>{{ pub.title }}</i>, {{ formatted_authors }}, <i class="venue">{{ pub.venue }}</i>, {{ pub.year }}
  </li>
{% endfor %}
</ul>


<style>
/* 🎨 全局字体样式 */
body, p, li {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #333;
  line-height: 1.7;
}

/* 🔹 一级标题样式 */
h1 {
  color: #004aad;
  font-size: 24px;
  font-weight: 600;
  margin-top: 0em;
  margin-bottom: 1em;
  border-bottom: 2px solid #004aad33;
  padding-bottom: 0.4em;
}

/* 🧾 段落样式 */
p.justify {
  text-align: justify;
  text-justify: inter-word;
  line-height: 1.8;
  font-size: 16px;
  color: #3a3a3a;
  margin-bottom: 0.2em;
}

/* 🌱 Short Bio 列表样式 */
ul.bio-list {
  list-style: none;
  padding-left: 1.5em;
  margin: -0.2em 0 0em 0;
}
ul.bio-list li {
  position: relative;
  text-align: justify;
  text-justify: inter-word;
  margin-bottom: 0em;
  font-size: 16px;
  color: #333;
}
ul.bio-list li::before {
  content: "• ";
  position: absolute;
  left: -1.5em;
  /* color: #007acc;  /* 稍浅蓝色 */ */
  color: #333;
  font-weight: bold;
}
ul.bio-list i {
  font-style: italic;
  /* color: #004aad; */
  color: #333;
  font-weight: 600;
}

/* 📚 Publications 列表样式 */
ul.pub-list {
  list-style: none;
  padding-left: 1.5em;
  margin: 0.5em 0 2em 0;
}
ul.pub-list li {
  position: relative;
  text-align: justify;
  text-justify: inter-word;
  margin-bottom: 1.5em;
  font-size: 16px;
  color: #333;
}
ul.pub-list li::before {
  content: "- ";
  position: absolute;
  left: -1.5em;
  /* color: #004aad; */
  color: #333;
  font-weight: bold;
}

.venue {
  color: #004aad;
  font-style: italic;
  font-weight: 600;
}

/* 🔗 链接样式 */
a {
  color: #004aad;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

/* 🚫 隐藏 Home 默认标题 */
.page__title {
  display: none !important;
}

html {
  scroll-behavior: smooth;
}
</style>
