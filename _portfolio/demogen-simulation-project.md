---
title: "One-Shot Demo Synthesis for Robot Imitation Learning"
excerpt: "A data-efficient robotic manipulation system using DemoGen for synthetic demonstration generation, training 3D Diffusion Policy (DP3) models deployable on both simulation and real Franka Panda robots with minimal human data."
collection: portfolio
order: 10
header:
  teaser: "sim_assembly.gif"
---

This project implements data-efficient robotic manipulation. Using Robopal simulation and DemoGen for synthetic demonstration generation, we train 3D-Diffusion-Policy models deployable on both simulation and real Franka Panda robots with minimal human data.

**Key Contributions:**
- **One-shot demo synthesis**: Generate hundreds of synthetic demonstrations from a single human teleoperation demo via spatial augmentation
- **3D Diffusion Policy (DP3)**: Train visuomotor policies using point cloud observations for spatial generalization
- **Sim-to-real transfer**: Directly deploy simulated policies to real FR3 robot without fine-tuning

**Experiments:**
- Achieved **88.8% average success rate** across 5 manipulation tasks with synthesized data + multi-view point cloud completion
- Single-shot synthesis (74.4%) significantly outperforms 10 real demos (47.8%)
- Validated on real FR3 robot with Linker Hand O6 dexterous hand

**Tech Stack:** Python, PyTorch, MuJoCo, RoboPal, DemoGen, Intel RealSense L515

## Simulation Demos

<style>
.sim-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 6px;
  margin: 1em 0;
}
.sim-grid .sim-item {
  text-align: center;
}
.sim-grid .sim-item:nth-child(4),
.sim-grid .sim-item:nth-child(5) {
  /* center the last row of 2 items */
}
.sim-grid img {
  width: 100%;
  height: auto;
  border-radius: 4px;
  border: 1px solid #ddd;
}
.sim-grid .sim-label {
  font-size: 0.85em;
  margin-top: 2px;
  color: #555;
}
@media (max-width: 768px) {
  .sim-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>

<div class="sim-grid">
  <div class="sim-item">
    <img src="/images/sim_stack_cube.gif" alt="Stack Cube" />
    <div class="sim-label">Stack Cube (79%)</div>
  </div>
  <div class="sim-item">
    <img src="/images/sim_press_button.gif" alt="Press Button" />
    <div class="sim-label">Press Button (99%)</div>
  </div>
  <div class="sim-item">
    <img src="/images/sim_pick_cube.gif" alt="Pick Cube" />
    <div class="sim-label">Pick Cube (87%)</div>
  </div>
  <div class="sim-item">
    <img src="/images/sim_assembly.gif" alt="Assembly" />
    <div class="sim-label">Assembly (80%)</div>
  </div>
  <div class="sim-item">
    <img src="/images/sim_close_box.gif" alt="Close Box" />
    <div class="sim-label">Close Box (95%)</div>
  </div>
</div>

[GitHub Repository](https://github.com/JHHuan/Demogen-simulation-project)
