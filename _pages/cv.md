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
* M.S. in Computer Science (expected), Beijing Institute of Technology, 2026 (expected)
* B.S. in University of Science and Technology Beijing, 2022 - 2026

Research Interests
======
* Machine Learning
* Computer Vision
* Artificial Intelligence
* Robotics

Skills
======
* Programming: Python, C/C++, MATLAB
* Deep Learning Frameworks: PyTorch, TensorFlow
* Computer Vision: OpenCV
* Robotics: ROS
* Tools: Git, LaTeX, Linux

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Portfolio
======
  <ul>{% for post in site.portfolio reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
