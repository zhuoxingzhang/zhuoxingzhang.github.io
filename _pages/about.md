---
permalink: /
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<!-- 🧠 Short Bio -->
<h2>Short Bio</h2>
<p class="justify">
&emsp;&emsp;I am currently pursuing a PhD in Computer Science at the University of Auckland since 2023. Previously, I was a visiting student at Southwest University during 2019 - 2022. Prior to that, I completed an MSc in Software Engineering at Southwest University in 2019 and a BSc in Software Engineering at South-Central Minzu University in 2016. My current research specialises in relational database theory with a focus on data normalization techniques and anomaly detection from system logs.<br> 
&emsp;&emsp;Specifically, my work mainly consists of the following areas:
</p>

<ul class="custom-list">
  <li><i>Schema Design Optimization</i>: Developing novel normalization algorithms to minimize data redundancy and improve update efficiency while preserving functional dependencies.</li>
  <li><i>Update Cost Reduction</i>: Quantifying the trade-offs between normalization levels and update overheads in database systems.</li>
  <li><i>Mining FDs/Keys from Data</i>: Mining meaningful Functional Dependencies/Keys from data with domain expert knowledge.</li>
  <li><i>Detecting Anomalies from System Logs</i>: Mining anomalous patterns from system logs to find root causes via deep learning techniques.</li>
</ul>

---

<!-- 🧾 Selected Publications -->
<h2>Selected Publications</h2>
<div class="wordwrap">You can also find all my papers on my <a href="https://dblp.org/pid/223/8303.html" target="_blank">DBLP</a> profile.</div>

<ul class="custom-list">
{% for pub in site.data.pubs %}
  {% assign authors = pub.authors | split: ',' %}
  {% assign formatted_authors = "" %}

  {% for a in authors %}
    {% assign author = a | strip %}
    {% if author == "Zhuoxing Zhang" %}
      {%- comment -%}
        用 append 分段拼接，避免引号嵌套问题
      {%- endcomment -%}
      {% assign formatted_authors = formatted_authors | append: "<strong>" | append: author | append: "</strong>" %}
    {% else %}
      {% assign formatted_authors = formatted_authors | append: author %}
    {% endif %}
    {% unless forloop.last %}
      {% assign formatted_authors = formatted_authors | append: ", " %}
    {% endunless %}
  {% endfor %}

  <li>
    <!-- 论文名加类以应用蓝色样式 -->
    <strong class="pub-title">{{ pub.title }}</strong>, {{ formatted_authors }}, <i class="venue">{{ pub.venue }}</i>, {{ pub.year }}
  </li>
{% endfor %}
</ul>


<style>
/* 🎨 全局风格 */
body, p, li {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #333;
  line-height: 1.7;
}

/* 🔹 一级标题（Short Bio, Selected Publications） */
h2 {
  color: #004aad;
  font-size: 24px;
  font-weight: 600;
  margin-top: 1em;
  margin-bottom: 0.6em;
  border-bottom: 2px solid #004aad33; /* 淡蓝下划线 */
  padding-bottom: 0.2em;
}

/* 🧾 段落样式：首行缩进 + 两端对齐 */
p.justify {
  text-align: justify;
  text-justify: inter-word;
  line-height: 1.8;
  font-size: 16px;
  color: #3a3a3a;
  margin-bottom: 1em;
}

/* 🔹 自定义列表 */
ul.custom-list {
  list-style: none;
  padding-left: 1.5em;
  margin: 0.5em 0 1em 0;
}

ul.custom-list li {
  position: relative;
  text-align: justify;
  text-justify: inter-word;
  margin-bottom: 0.3em;
  font-size: 16px;
  color: #333;
}

/* 💠 蓝色符号 */
ul.custom-list li::before {
  content: "- ";
  position: absolute;
  left: -1.5em;
  color: #004aad;
  font-weight: bold;
}

/* 🪶 斜体项目名 */
ul.custom-list i {
  font-style: italic;
  color: #004aad;
  font-weight: 600;
}

/* 🔹 论文标题样式（与 venue 一样蓝色） */
.pub-title {
  color: #004aad;
  font-weight: 600;
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

.page__title {
  display: none !important;
}
</style>
