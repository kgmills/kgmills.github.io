---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## Introduction
Keith George Mills is an Assistant Professor at the Division of Computer Science and Engineering (CSE) at Louisiana State University (LSU). He received his BSc. with Distinction and MSc. in Computer Engineering from University of Alberta in 2018 and 2020, respectively. He completed his Ph.D. in Software Engineering and Intelligent Systems from the University of Alberta in 2025. Keith's doctoral thesis, titled "Automated and Efficient Deep Neural Network Design via Quantifiable Data Science" was selected to receive the George Walker Award for Best Doctoral Thesis for UAlberta ECE.

His research interests primarily lie in the domains of automated, efficient and interpetable/explainable machine learning through neural architecture search, model compression, graph theory and representation learning for applications primarily in computer vision and generative AI. 

## Recent News
<ul>
{% for post in site.posts limit:5 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span style="color:gray; font-size:0.9em;">{{ post.date | date: "%B %d, %Y" }}</span>
  </li>
{% endfor %}
</ul>

<script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=r5Z6O1gcjjkI42JAX36E9tBUnnnqd8FCHDt7Ppoh4qU"></script>