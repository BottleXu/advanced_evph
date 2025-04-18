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
The green and red circles represent the start and goal points, respectively, while gray and dark blue arrows indicate the paths of people moving at 0.2 m/s and 0.3 m/s. The environment includes 18 moving people and five static obstacles. In the first simulation, our proposed method, AEVPH reaches the shortest traveling time (49.51 s), and ensures smoother and more efficient navigation through consistent forward movement (0.0064 m/s).

Video demonstration of the first simulation is provided [here](https://youtube.com "Simulation I link")

## Simulation II
![Simulation II environment](figures/s2_results.png)
![Simulation II velocity plot](figures/s2_discussion.png)
The green and red circles represent the start and goal points, respectively, while gray and dark blue arrows indicate the paths of people moving at 0.2 m/s and 0.3 m/s. The environment includes a narrow path surrounded by static obstacles and crowds. In the second simulation, our proposed method, AEVPH reaches the shortest traveling time (53.01 s), and ensures smoother and more efficient navigation through consistent forward movement (0.0092 m/s).

Video demonstration of the second simulation is provided [here](https://youtube.com "Simulation II link")

## Real-World
![Real-World](figures/real_result.png)
The green and red circles represent the robot’s start and goal positions, respectively. The dark blue circle indicates the person’s initial position, and the arrow shows their walking path. In the real-world experiment, our proposed method, AEVPH reaches the shortest traveling time (36.46 s), and ensures smoother and more efficient navigation through consistent forward movement (0.0049 m/s). Also, it operated at an average frequency
of 9.2 Hz, ensuring real-time performance.

| Methods  | Collision(Y/N) | Traveling distance(m)  | Traveling time(s) | Average variability of linear velocity (m/s)  |
| ------------- | :-------------: | -------------: | -------------: |-------------: |
| DWA  | N  | 10.52 | 38.85 | 0.0388 |
| TEB  | N  | 12.24 | 43.75 | 0.0692 |
| RVO  | N  | 10.68 | 42.49 | 0.0128 |
| SARL*  | N  | 10.56 | 38.01 | 0.0247 |
| VPH+  | N  | 11.10 | 38.96 | 0.0047 |
| EVPH  | N  | 10.76 | 38.02 | 0.0057 |
| **Proposed**  | N  | 10.66 | **36.46** | 0.0049 |

Video demonstration of the real-world experiment is provided [here](https://youtube.com "Simulation II link")

## Reference
[^1]: Arena-bench
[^2]: SARL
