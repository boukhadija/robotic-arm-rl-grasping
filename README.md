# robotic-arm-rl-grasping
robotic-arm-rl-grasping

Robotic Arm Grasping with Reinforcement Learning

A 6-joint robotic arm, designed in CATIA and trained in simulation to learn how to grasp objects using reinforcement learning.

Overview

This project combines mechanical design and machine learning: a robotic arm modeled in CATIA is exported into a physics simulator, where a reinforcement learning agent learns — through trial and error — how to move the arm and grasp objects of different shapes, while avoiding obstacles in the environment.

The project is simulation-only (no physical hardware build).

Motivation

Personal interest in bridging a mechanical engineering background with machine learning / AI engineering — specifically exploring the hardware-software interface through robotics.

Tech Stack
- CATIA — 3D mechanical design of the arm (base, links, gripper)
- URDF — robot description format bridging CAD design and simulation
- PyBullet — physics simulation environment
- Gymnasium — standard RL environment interface
- Stable-Baselines3 (DQN) — reinforcement learning algorithm
Python

Project Scope
- 6 joints: base rotation, elbow, gripper
- Discrete action space: a small fixed set of movements (e.g. move +X, move -X, move up, move down, open/close   gripper), rather than continuous joint control
- Objects to grasp: simple shapes (cubes, cylinders) placed in the simulated environment
- Obstacles: static objects the arm must learn to avoid while reaching for targets
Pipeline

1- Design — arm modeled and assembled in CATIA

2- Export — each link exported individually as STL

3- URDF — links and joints described in a URDF file for simulation

4- Environment — custom Gymnasium environment built in PyBullet (arm, table, objects, obstacles)

5- Training — DQN agent trained to reach and grasp objects via a reward function (distance-based shaping + grasp success bonus + collision penalty)

6- Evaluation — success rate and average reward tracked across training

Status

🚧 In progress — CATIA design complete, working on STL export and URDF setup.

Roadmap

(done) Design 6-joint arm in CATIA

 Export STLs and write URDF
 
 Load and verify arm in PyBullet
 
 Build custom Gymnasium environment
 
 Implement reward function
 
 Train baseline DQN agent
 
 Evaluate and iterate on reward shaping
 
 Record demo video / results
 
 
Author

Khadija Boudalaa — CS student (math minor), Hunter College (CUNY)
