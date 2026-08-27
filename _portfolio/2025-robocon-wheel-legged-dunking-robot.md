---
title: "Wheel-Legged Dunking Robot (2025)"
excerpt: "Project lead for a 1.5 m wheel-legged robot that combines high-speed swerve motion, jumping, ball reception, and dunking. Achieved a 40 cm vertical jump and over 95% dunking success in 100+ fixed-point tests."
collection: portfolio
project_category: competition
order: 30
permalink: /portfolio/robocon-2025-wheel-legged-dunking-robot/
header:
  video: "assets/videos/robocon-2025-final-dunk.mp4"
---

As project lead, I led the design, implementation, testing, and three iterations of a wheel-legged robot for the 2025 ROBOCON basketball competition. The final robot combines three-swerve high-speed motion, a five-link jumping mechanism, ball reception, and a lifting dunking mechanism.

**Recognition**

* National First Prize, ROBOCON Robot Basketball Competition
* National First Prize, ROBOCON Robot Basketball Skills Challenge
* ROBOCON Robot Basketball Best Technical Award

## Results

* **1.5 m** overall height and **25 kg** total mass
* **>40 cm** vertical jump height
* **>95%** dunking success rate over **100+** fixed-point tests

## Technical Contributions

* Proposed jumping planning based on the **spring-loaded inverted pendulum (SLIP)** model.
* Built a five-link parallel-mechanism multibody dynamics model in **Simulink** and **Simscape Multibody** for full-phase jump simulation.
* Implemented **virtual model control (VMC)** to generate virtual forces, together with virtual-spring PD control for impact buffering and soft landing.
* Integrated **IMU-LQR** attitude control to keep the leg posture level after landing.
* Led three hardware iterations: separated the jump and motion mechanisms, adopted a three-swerve chassis for faster and more stable movement, and added LiDAR-based global localization and ball-reception functionality.

## Demonstration Videos

<div class="robocon-video-grid">
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/robocon-2025-initial-dunk.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>First-generation dunking prototype.</figcaption>
  </figure>
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/robocon-2025-final-dunk.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>Final robot dunking demonstration.</figcaption>
  </figure>
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/robocon-2025-landing-buffer.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>Landing buffer and posture stabilization.</figcaption>
  </figure>
</div>

**Tech stack:** MATLAB/Simulink, Simscape Multibody, SLIP, VMC, LQR, PD control, IMU, LiDAR localization, swerve chassis design
