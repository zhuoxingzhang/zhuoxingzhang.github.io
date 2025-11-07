---
permalink: /
title: "Short Bio"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* 🎨 整体风格 */
body, p, li {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #333;
  line-height: 1.7;
}

/* 🧾 段落样式：首行缩进 + 两端对齐 */
p.justify {
  text-align: justify;
  text-justify: inter-word;
  line-height: 1.8;
  font-size: 16px;
  color: #3a3a3a;
  margin-bottom: 0em;
  margin-top: 9em;
}

/* 🧷 标题样式 */
h1, h2, h3 {
  color: #004aad;  /* 蓝色标题 */
  font-weight: 600;
}

/* 🔹 自定义列表 */
ul.custom-list {
  list-style: none;
  padding-left: 1.5em;  /* 控制整体左缩进 */
  margin: 0em 0 0.8em 0;
}

ul.custom-list li {
  position: relative;
  text-align: justify;
  text-justify: inter-word;
  margin-bottom: 0.01em;
  font-size: 16px;
  color: #333;
}

/* 💠 自定义符号（可改为 "★"、"◆"、"✔"、"➤" 等） */
ul.custom-list li::before {
  content: "- ";
  position: absolute;
  left: -1.5em;
  color: #004aad;     /* 蓝色符号 */
  font-weight: bold;
}

/* 🪶 斜体项目名样式 */
ul.custom-list i {
  font-style: italic;
  color: #004aad;
  font-weight: 500;
}
</style>

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
