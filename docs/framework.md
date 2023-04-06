---
comments: true
hide:
    - toc
---


## Roadmap

### Models

- [x] Gaussian Process Regression (GPR): continuous
- [ ] Occupanocy Grid Map (OGM): discrete

### Objectives

- [x] Entropy

### Planners

- [x] Myopic Planner: produces a single informative waypoint
- [ ] Monte Carlo Tree Search (MCTS): sampling-based, producesa sequence of waypoints or actions
- [ ] Rapidly-Exploring Random Trees (RRT): sampling-based, producesa a sequence of waypoints
- [ ] Bayesian Optimization (BO): trajectory optimization, producesa a parameterized trajectory
- [ ] Covariance Matrix Adaptation Evolution Strategy (CMA-ES): trajectory optimization, produces a parameterized trajectory

### Controllers

- [x] Proportional Derivative (PD) Controller
- [ ] Model Predictive Controller (MPC)

### Sensors

- [x] Single-Beam Ranger: sonar
- [ ] Multi-Beam Ranger: LiDAR, depth camera

### Robots

- [ ] Omni-Directional Robot
- [x] Differential-Drive Robot
- [ ] Ackermann-Steering Robot


### Tasks

!!! note

    Navigation is not a RIG task.

- [ ] Navigation:
- [x] Active Mapping
    - [x] Environmental Mapping
    - [ ] Occupancy Mapping
    - [ ] Autonomous Inspection
    - [ ] Search and Rescue
- [ ] Active Localization
- [ ] Active Simultaneous Localization and Mapping (SLAM)

| Task | Goal | Requires Target Map | Requires Obstacle Map | Considers Collision | Localization Algorithm | Mapping Algorithm |
| ---- | ---- | :-----------------: | :-------------------: | :-----------------: | :--------------------: | :---------------: |
| Navigation | Move from start position to goal position | ❌ | ✅ </br> Known | ✅ | ❌ | ❌ |
| Environmental Mapping | Build the target map | ✅ </br> Unknown | ❌/✅ <br/> Free/Known | ❌/✅ | ❌ | ✅ |
| Occupancy Mapping | Build the obstacle map | ❌ | ✅ </br> Unknown | ✅ | ❌ | ✅ |
| Autonomous Inspection | Build the target map | ✅ </br> Unknown </br> Dense  | ✅ </br> Unknown | ✅ | ❌ | ✅ |
| Search and Rescue | Locate as many victims as possible | ✅ </br> Unknown </br> Sparse | ✅ </br> Unknown | ✅ | ❌ | ✅ |
| Active Localization | Actively reduce localization uncertainty while navigation | ❌ | ✅ </br> Known | ✅ | ✅ | ❌ |
| Active SLAM | Actively reduce localization and mapping uncertainty | ❌ | ✅ </br> Unknown | ✅ | ✅ | ✅ |
