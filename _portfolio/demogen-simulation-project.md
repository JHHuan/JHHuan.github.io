---
title: "One-Shot Demo Synthesis for Robot Imitation Learning"
excerpt: "A data-efficient robotic manipulation system using DemoGen for synthetic demonstration generation, training 3D Diffusion Policy (DP3) models deployable on both simulation and real Franka Panda robots with minimal human data."
collection: portfolio
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

[GitHub Repository](https://github.com/JHHuan/Demogen-simulation-project)
