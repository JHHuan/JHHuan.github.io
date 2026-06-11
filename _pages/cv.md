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
* Robotic Manipulation
* Imitation Learning
* 3D Vision & Point Cloud Processing
* Sim-to-Real Transfer
* Machine Learning

Skills
======
* Programming: Python, C/C++, MATLAB
* Deep Learning: PyTorch, TensorFlow
* Robotics: MuJoCo, RoboPal, ROS, DemoGen
* Computer Vision: OpenCV, Point Cloud Processing
* Tools: Git, LaTeX, Linux, Docker

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
