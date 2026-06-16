---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## Introduction
Keith George Mills is an Assistant Professor at the Division of Computer Science and Engineering (CSE) at Louisiana State University (LSU). He is the PI of the Artificial intelligence Techniques for Hardware-aware Efficient Neural network Automation (<a href="https://github.com/LSU-ATHENA">ATHENA</a>) Lab. He also serves as a supporting faculty member for <a href="https://www.ece.lsu.edu/ecocar/">LSU's EcoCAR '26-'30 team</a> as an AI subject matter expert.

Dr. Mills' primary research interests lie in the intersection of efficient, automated and interpretable machine learning. At the moment he is primarily focused on initial noise optimization for Diffusion Models and graph-based Neural Architecture Search. He is also interested in using AI/ML to model chemical/physical design processes, power delivery, as well as AI for education. 

Dr. Mills received his BSc. with Distinction and MSc. in Computer Engineering from University of Alberta in 2018 and 2020, respectively. He completed his Ph.D. in Software Engineering and Intelligent Systems from the University of Alberta in 2025. Dr. Mills' doctoral thesis, titled "Automated and Efficient Deep Neural Network Design via Quantifiable Data Science" was selected to receive the George Walker Award for Best Doctoral Thesis for UAlberta ECE.

**Recruiting**

I am actively recruiting self-motivated PhD and MSc students with strong technical skills. Topics include:  
* Efficient and Hardware-Aware AI Computing
* AutoML and Neural Architecture Search
* Explainable and Interpretable AI
* Applications of AI and Agentic Systems

I am primarily targetting intake for Spring 2027. Exceptional candidates interested in Fall 2026 admission are also encouraged to apply. <a href="assets/recruiting/athena_hiring.pdf">Please consult the ATHENA application guidelines when reaching out.</a>


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