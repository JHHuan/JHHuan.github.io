---
title: "HUG-Driven Dexterous Grasping and VLA Simulation Pipeline"
excerpt: "Built an end-to-end dexterous-grasping pipeline that retargets HUG-generated MANO grasps to an O6Hand, collects successful Panda + O6Hand MuJoCo demonstrations, and trains and evaluates ACT and SmolVLA policies."
collection: portfolio
order: 40
permalink: /portfolio/hug-dexterous-grasping-vla-pipeline/
header:
  video: "assets/videos/hug-vla-act-rollout-001.mp4"
---

This personal project turns pretrained **HUG (Human Universal Grasping)** predictions into an executable dexterous-manipulation pipeline. It connects RGB-D grasp generation, MANO-to-O6Hand retargeting, Panda + O6Hand MuJoCo execution, automated demonstration collection, and closed-loop ACT / SmolVLA policy deployment.

> **Scope:** HUG's pretrained model and weights are credited to its original authors. My work focuses on robot-environment adaptation, MANO-to-O6Hand retargeting, automated data collection, and policy training and deployment.

## System Contributions

* **Dexterous-grasp retargeting:** Converted HUG-generated MANO wrist and joint poses into the O6Hand's 6-D control space while preserving thumb-opposition configurations needed for stable grasps.
* **Robust staged execution:** Designed pre-grasp, descent, thumb-safe closure, and lift phases for contact-aware tabletop grasping; selected equivalent precomputed grasp templates according to the target yaw instead of re-running expensive grasp generation for every rollout.
* **Automated data pipeline:** Integrated Panda and O6Hand in MuJoCo with randomized target poses, distractor layouts, and fixed dual third-person camera views. Only episodes that successfully lift the target are exported in LeRobot v3-compatible state, action, task, and video formats.
* **Policy-training loop:** Built matched collection and deployment environments for ACT and SmolVLA, with two visual observations plus a 13-D Panda/O6Hand state-action representation. The deployment tools support headless batch evaluation and visual replay.

## Data and Evaluation Setup

The collection setup uses two fixed third-person RGB views (`640 × 360`, 30 FPS) to avoid hand occlusion and camera interpenetration. A representative banana-grasp configuration includes randomized target and distractor placement, natural-language task conditioning, and 100 retained successful episodes (about 18,800 frames).

Recorded evaluations use a success criterion of lifting the banana by at least 5 cm:

| Policy | Recorded setting | Result |
| --- | --- | --- |
| ACT | 3 banana-grasp rollout episodes | 3 / 3 successful lifts; mean final lift: 0.210 m |
| SmolVLA | 5 language-conditioned, dual-view rollout episodes with distractors | 2 / 5 successful lifts; mean final lift: 0.111 m |

These runs document each policy's recorded evaluation setting and are not intended as a controlled comparison between ACT and SmolVLA.

## Demonstration Videos

<div class="hug-video-gallery">
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/hug-vla-act-rollout-001.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>ACT rollout 1: approach, grasp, and stable banana lift.</figcaption>
  </figure>
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/hug-vla-act-rollout-002.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>ACT rollout 2 under a different sampled tabletop arrangement.</figcaption>
  </figure>
  <figure>
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/hug-vla-act-rollout-003.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>ACT rollout 3: another recorded successful lift.</figcaption>
  </figure>
  <figure class="hug-video-gallery__wide">
    <video controls playsinline preload="metadata">
      <source src="/assets/videos/hug-vla-smolvla-rollout-001.mp4" type="video/mp4" />
      Your browser does not support HTML video.
    </video>
    <figcaption>SmolVLA rollout with synchronized dual third-person views and the instruction “Pick up the banana.”</figcaption>
  </figure>
</div>

**Tech stack:** Python, PyTorch, MuJoCo, RoboPal, HUG, MANO, Franka Panda, O6Hand, LeRobot v3, ACT, SmolVLA

**Acknowledgements:** [HUG: Human Universal Grasping](https://github.com/kevinywu/hug) provides the pretrained grasp model and public weights used by this project.
