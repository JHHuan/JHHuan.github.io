---
title: "ROBOCON 2025: Wheel-Legged Dunking Robot"
excerpt: "Project lead for a 1.5 m wheel-legged robot that combines high-speed swerve motion, jumping, ball reception, and dunking. Achieved a 40 cm vertical jump and over 95% dunking success in 100+ fixed-point tests."
collection: portfolio
header:
  teaser: "projects/robocon-2025-dunking-hero.png"
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

## Robot Development

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
    <img src="/images/projects/robocon-2025-dunking-hero.png" alt="Wheel-legged dunking robot during a test" />
    <figcaption>Dunking test with the final robot.</figcaption>
  </figure>
  <figure>
    <img src="/images/projects/robocon-2025-dunking-robot.png" alt="Close view of the wheel-legged robot" />
    <figcaption>Five-link jumping mechanism and mobile chassis.</figcaption>
  </figure>
  <figure>
    <img src="/images/projects/robocon-2025-dunking-lab.png" alt="ROBOCON dunking robot test area" />
    <figcaption>End-to-end testing in the competition field.</figcaption>
  </figure>
</div>

**Tech stack:** MATLAB/Simulink, Simscape Multibody, SLIP, VMC, LQR, PD control, IMU, LiDAR localization, swerve chassis design
