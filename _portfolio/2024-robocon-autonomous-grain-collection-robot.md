---
title: "Autonomous Grain Collection and Placement Robot (2024)"
excerpt: "Project lead for an autonomous grain-tracking, grasping, and placement robot with a 3-DOF arm, four-swerve chassis, Intel RealSense D455 depth camera, LiDAR, and encoders."
collection: portfolio
permalink: /portfolio/robocon-2024-autonomous-grain-collection-robot/
header:
  overlay_image: "projects/robocon-2024-grain-hero.jpeg"
  overlay_filter: 0.35
  teaser: "projects/robocon-2024-grain-hero.jpeg"
---

As project lead, I led the end-to-end development of an autonomous robot for the 2024 ROBOCON “Granary Collection” competition. The robot identifies, tracks, grasps, and places grain targets while autonomously navigating the full competition field.

**Recognition**

* Third Place, ROBOCON “Granary Collection” main competition
* Champion, ROBOCON Skills Challenge
* First Prize, ROBOCON Programming Challenge

## System Overview

The system combines a four-swerve chassis with a 3-DOF cantilever arm. An Intel RealSense D455 depth camera, LiDAR, orthogonal encoders, and IMU support field localization and dynamic target perception. A Jetson AGX Orin runs target detection and communicates with the embedded controller for mobile-base and arm control.

## Technical Contributions

* Led the complete project cycle from concept design and task scheduling to robot integration, testing, and technical iteration.
* Designed the 3-DOF cantilever arm, swerve chassis, and gimbal in **SolidWorks**; verified structural strength with **ANSYS Workbench** static analysis.
* Integrated depth-camera, LiDAR, and encoder measurements for field and target localization, reaching **over 95%** accuracy in dynamic target tracking and grasping.
* Developed the coordinated mobile-base and arm workflow for autonomous tracking, grasping, transport, and multi-target placement.

## Competition Robot

<style>
.robocon-gallery {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
  margin: 1.5rem 0;
}
.robocon-gallery figure {
  margin: 0;
}
.robocon-gallery img {
  display: block;
  width: 100%;
  border: 1px solid #ddd;
  border-radius: 6px;
}
.robocon-gallery figcaption {
  color: #666;
  font-size: 0.9em;
  margin-top: 0.4rem;
}
@media (max-width: 768px) {
  .robocon-gallery {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="robocon-gallery">
  <figure>
    <img src="/images/projects/robocon-2024-grain-hero.jpeg" alt="Autonomous grain-collection robot at ROBOCON" />
    <figcaption>Competition robot during the ROBOCON event.</figcaption>
  </figure>
  <figure>
    <img src="/images/projects/robocon-2024-grain-course.jpeg" alt="Robot navigating the ROBOCON field" />
    <figcaption>Autonomous navigation and task execution on the competition field.</figcaption>
  </figure>
  <figure>
    <img src="/images/projects/robocon-2024-grain-system.png" alt="Robot system and control architecture" />
    <figcaption>Perception, localization, control, and mechanical-system architecture.</figcaption>
  </figure>
</div>

**Tech stack:** SolidWorks, ANSYS Workbench, Intel RealSense D455, LiDAR, encoders, IMU, Jetson AGX Orin, YOLO, embedded control, swerve chassis design
