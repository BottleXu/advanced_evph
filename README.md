# Advanced EVPH: Advanced Omni-directional Vector Polar Histogram for Robust Navigation in Crowded Environments

This repostiory introduces our paper "Advanced EVPH: Advanced Omni-directional Vector Polar Histogram for Robust Navigation in Crowded Environments" in IEEE Robotics and Automation Letters(RA/L). 

## Introduction
We propose an Advanced EVPH to improve navigational performance significantly in crowded environments.

## Method Overview

## System Configuration and Experiment Setup

We selected Arena-Bench[^1] to evaluate a performance of the proposed method. 
The performance is compared with conventional methods as follows:
- Dynamic Window Approach (DWA),
- Timed Elastic Band (TEB),
- Reciprocal Collision Avoidance (RVO),
- Socially Attentive Reinforcement Learning (SARL*)[^2],
- Enhanced Vector Polar Histogram (VPH+),
- Extended Vector Polar Histogram (EVPH, our previous work).

We use Clearpath Jackal with RPLiDAR A3 range sensor.
![Robot](figures/Robot.png)

Our simulatuion environment is Ubuntu 20.04 with ROS Noetic, Intel Core i7 10700k, 16GB RAM, Nvidia RTX 3060. 

In real-world experiment, we use a laptop to execute robot framework (SLAM, path planning) with Ubuntu 20.04 with ROS Noetic, AMD Ryzen 5500U, 16GB RAM, Radeon Graphics.

## Simulation I
![Simulation I environment](figures/s1_results.png)
![Simulation I velocity plot](figures/s1_discussion.png)
The green and red circles represent the start and goal points, respectively, while gray and dark blue arrows indicate the paths of people moving at 0.2 m/s and 0.3 m/s. The environment includes 18 moving people and five static obstacles.
In the first simulation, our proposed method, AEVPH reaches the shortest traveling time (49.51 s), and ensures smoother and more efficient navigation through consistent forward movement (0.0064 m/s).



## Simulation II
Video
## Real-World
Video
## Reference
[^1]: Arena-bench
[^2]: SARL
