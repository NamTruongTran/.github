# Arena Rosnav (Arena 3.0) 

[Arena Rosnav](https://github.com/Arena-Rosnav/arena-rosnav) is a platform for developing and benchmarking navigation algorithms in human-centric social environments. We offer a wide variety of different social force models, robots, planners, and world generation algorithms, and many more to use. All functions are abstracted and can be run across three widely used simulators: Flatland 2D, Gazebo, and Unity 3D. Arena Rosnav also offers a complete evaluation pipeline for benchmarking the performance of robots and planners based on standard metrics, and a trainings pipeline for navigational models based on DRL and PPO. With this pipeline our own DRL planner [ROSNavRL](https://github.com/Arena-Rosnav/rosnav-rl) was created.

### Documentation
Follow the documentation for details how to use the platform: 

[Documentation](https://arena-rosnav.readthedocs.io/en/latest/)

### Arena-Education
We also offer worksheets which contain tasks and solutions and are a great starting point for beginners aiming to learn about robotics and the Arena platform:

[https://edu.arena-rosnav.org/](https://edu.arena-rosnav.org/) \
[Worksheet #1: Installation and First Steps](https://edu.arena-rosnav.org/)



<!-- |          Warehouse environment in Gazebo           |          Hospital environment in Gazebo          |
| :------------------------------------------------: | :----------------------------------------------: |
| <img src="docs/images/gifs/gazebo_simulation.gif"> | <img src="docs/images/gifs/hospital_gazebo.gif"> |

<br/>

|                Simulation in Flatland                 |         Multiple agents in one simulation          |
| :---------------------------------------------------: | :------------------------------------------------: |
| <img src="docs/images/gifs/flatland_simulation.gif" > | <img src="docs/images/gifs/marl_custom_rviz.gif" > | -->

#### Unity

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/unity_1.gif"> | <img  src="docs/tutorials/gazebo_tutorial/new_gifs/unity_2.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: | 

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/unity_4.gif"> | <img  src="docs/tutorials/gazebo_tutorial/new_gifs/unity_5.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: |

<img width="1300" height="300" src="docs/tutorials/gazebo_tutorial/new_gifs/unity_6.gif">

#### Gazebo

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/arena_hospital_small.gif"> | <img src="docs/tutorials/gazebo_tutorial/new_gifs/arena_hawker_centre.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: | 

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/com_3.gif"> | <img  src="docs/tutorials/gazebo_tutorial/new_gifs/aws_house.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: |

<img width="1300" height="300" src="docs/tutorials/gazebo_tutorial/new_gifs/factory.gif">

#### Flatland

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/flatland_1.gif"> | <img  src="docs/tutorials/gazebo_tutorial/new_gifs/flatland_2.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: | 

| <img  src="docs/tutorials/gazebo_tutorial/new_gifs/flatland_4.gif"> | <img  src="docs/tutorials/gazebo_tutorial/new_gifs/flatland_5.gif"> | 
| :--------------------------------------------------------------: | :---------------------------------------------------------------------: |

<img width="1300" height="300" src="docs/tutorials/gazebo_tutorial/new_gifs/flatland_3.gif">

### Features

- Automatic installation script for the arena rosnav environment 
- 3 different simulators including [Unity](#unity), [Gazebo](#gazebo) and [Flatland](#flatland)
- We offer prebuilt, realistic simulation [environments](#supported-worlds), including offices, hospitals, canteens, warehouses, and much more
- Dynamic Map Generation including dynamic mazes
- Variety of Task Modes for robots and pedestrians

  | Task Mode | Short Description | Robots | Obstacles |
  | --- | --- | --- | --- |
  | `scenario` | load scenario file | ✓ | ✓ |
  | `random` | generate random positions | ✓ | ✓ |
  | `parametrized` | more fine-tuned random | | ✓ |
  | `guided` | waypoint sequence | ✓ | |
  | `explore` | explore map | ✓ | |

- Variety of [Robots](#supported-robots) including the go1 quadruped robot
- Variety of [Planners](#supported-planners) including our own DRL planner `ROSNavRL`
- Variety of social force models for pedestrians 
- Pipeline for evaluating approaches and analysing them based on standard metrics with our `Arena Evaluation` package.
- Pipeline to train planner agents based on reinforcement learning approaches from `stable baselines3`
- Modular and flexible structure for extension of new functionalities and approaches
- Fully integrated `Move Base Flex` in our Arena-Rosnav ecosystem




<!-- - Integration of [Flatland](https://flatland-simulator.readthedocs.io/en/latest/) to train new agents and [Flatland](https://flatland-simulator.readthedocs.io/en/latest/) and [Gazebo](https://classic.gazebosim.org/) for evaluating existing approaches.
- Variety of planners, robots and worlds
- Pipeline to train planner agents based on reinforcement learning approaches from [stable baselines3](https://github.com/DLR-RM/stable-baselines3.git)
- [Task generator](packages/task_generator.md) for managing highly dynamic and custom environments
- Our own DRL planner [ROSNavRL](packages/rosnavrl.md)
- Pipeline for evaluating approaches and analysing them based on standard metrics with our [Arena Evaluation](packages/arena_evaluation.md) package.
- Modular structure for extension of new functionalities and approaches
- Evaluation of multiple robots and planners in the same simulation
- Dynamic rviz config file creation for visualization -->

## Supported Planners

| Planner  | Type | Robot | Description | Authors |
|-------------|-----------|---------|---------------|---------------|
| **Applr** | Hybrid | Jackal | A hybrid planner combining different approaches for adaptive planning. | [Xiao et al.](https://www.researchgate.net/publication/342184799_APPLD_Adaptive_Planner_Parameter_Learning_from_Demonstration) | 5 |
| **Cohan**  | Classic | All | A traditional planner focusing on human-aware navigation strategies. | [Singamaneni et al.](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rWw5YTsAAAAJ&citation_for_view=rWw5YTsAAAAJ:9yKSN-GCB0IC) |
| **Dragon** | Hybrid | Jackal | A hybrid navigation system designed for dynamic environments. | [Xiao et al.](https://www.researchgate.net/publication/362858861_Autonomous_Ground_Navigation_in_Highly_Constrained_Spaces_Lessons_learned_from_The_BARN_Challenge_at_ICRA_2022) | 
| **DWA**  | Classic | All | Dynamic Window Approach, a reactive collision avoidance method considering the robot’s dynamics. | [Khatib et al.](https://www.researchgate.net/publication/3113619_Real-Time_Obstacle_Avoidance_for_Fast_Mobile_Robots) | 
| **TEB** | Classic | All | Timed Elastic Bands, optimizing a global path by considering kinematic and dynamic constraints. | [Rösmann, et al.](https://rst.etit.tu-dortmund.de/storages/rst-etit/r/Global/Paper/Roesmann/2015_Roesmann_ECC.PDF) | 
| **MPC**  | Classic | All | Model Predictive Control, using a model of the robot’s dynamics to predict and optimize future trajectories. | [Rösmann et al.](https://www.researchgate.net/publication/320281520_Time-Optimal_Nonlinear_Model_Predictive_Control_with_Minimal_Control_Interventions) | 
| **LFLH** | Hybrid | All | A hybrid planner leveraging both learned and heuristic components for effective navigation. | [Xiao et al.](https://arxiv.org/abs/2011.13112) | 
| **RLCA**  | Learning | All | Reinforcement Learning Collision Avoidance, using RL for dynamic obstacle avoidance. | [Long et al.](https://arxiv.org/abs/1709.10082) |  
| **ROSNavRL** | Learning | All | A learning-based approach trained on Arena 2.0 with Reinforcement Learning. | Arena-Rosnav Team | 
| **Trail**  | Learning | All | A learning-based planner focusing on trail navigation in unstructured environments. | [Xiao et al.](https://www.researchgate.net/publication/362858861_Autonomous_Ground_Navigation_in_Highly_Constrained_Spaces_Lessons_learned_from_The_BARN_Challenge_at_ICRA_2022) | 
| **Crowdnav** | Learning | All | Focuses on navigating safely and efficiently in crowded environments using machine learning techniques. | [Chen et al.](https://arxiv.org/abs/1809.08835) | 
| **Sarl**  | Learning | All | Socially Aware Reinforcement Learning, emphasizing social norms in navigation. | [Li et al.](https://www.researchgate.net/publication/338722340_SARL_Deep_Reinforcement_Learning_based_Human-Aware_Navigation_for_Mobile_Robot_in_Indoor_Environments) | 
| **BRNE** | Game Theory  | Quadruped | Utilizes game theory for decision-making in complex scenarios suitable for quadruped robots. | [Muchen Sun et al.](https://www.academia.edu/100123106/Move_Beyond_Trajectories_Distribution_Space_Coupling_for_Crowd_Navigation?uc-g-sw=108439277) | 
| **iPlanner**  | Learning | Quadruped | A learning-based planner for complex dynamic situations, suitable for quadruped robots. | [Yang et al.](https://arxiv.org/abs/2302.11434) | 
| **ArtPlanner** | Learning | Quadruped | A learning-based planner optimized for articulated, quadruped robots. | [Hutter et al.](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/507668/2021_iros_wellhausen_planner_final_version.pdf?sequence=1) | 
| **Aggressive**  | Heuristic | All | Employs aggressive strategies for rapid navigation, often in competitive or urgent scenarios. | Arena-Rosnav Team | 
| **Polite** | Heuristic | All | Prioritizes polite and socially compliant behaviors in navigation. | Arena-Rosnav Team |
| **Sideways**  | Heuristic | All | Specializes in sideways maneuvers, useful in narrow or constrained spaces. | Arena-Rosnav Team |

<!-- - [ROSNavRL](packages/rosnavrl.md): Our own planner based on neural networks.
- Dragon: from the [BARN challenge](https://github.com/Arena-Rosnav/dragon)
- Trail: from the [BARN challenge, TRAIL lab](https://github.com/TempleRAIL/nav-competition-icra2022-drl-vo)
- Applr: a hybrid approach by [Xuesu et al.](https://arxiv.org/abs/2105.07620)
- RLCA-ROS: a DRL-based colision avoidance approach from [Long et al.](https://github.com/Acmece/rl-collision-avoidance)
- CADRL: a DRL-based colision avoidance approach from [Everett et al.](https://github.com/mit-acl/cadrl_ros)
- SARL-Star 
- Crowdnav-ROS: a DRL-based colision avoidance approach from [Chen et al.](https://github.com/vita-epfl/CrowdNav)
- TEB: a classic approach by [Rösmann et al.](https://github.com/rst-tu-dortmund/teb_local_planner)
- DWA: the standard ROS local planning approach by [Marder-Eppstein et al.](http://wiki.ros.org/dwa_local_planner)
- MPC: a classic approach by [Rösmann et al.](https://github.com/rst-tu-dortmund/teb_local_planner)
- and many more (added with Arena 3.0) -->

## Supported Robots

|                       _Quadruped-GO1_                        |                       _Car-O-Bot4 (cob4)_                         |                        _Tiago_                        |                       _Jackal_                       |                       _Robotino(rto)_                       |
| :--------------------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------------: | :----------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/images/robots/go1.png"> | <img width="250" src="docs/images/robots/cob4.jpg"> | <img width="250" src="docs/images/robots/tiago.jpg"> | <img width="250" src="docs/images/robots/jackal.jpg"> | <img width="250" src="docs/images/robots/rto.jpg"> |

|                  _Agv-Ota_                      |                       _Youbot_                        |                         _ridgeback_                        |                 _Turtlebot3_Waffle_pi_                 |                       _Turtlebot3-Burger_                        |
| :------------------------------------------------: | :---------------------------------------------------: | :------------------------------------------------------------------: | :-------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/images/robots/agv-ota.png"> | <img width="250" src="docs/images/robots/youbot.jpg"> | <img width="250"  src="docs/images/robots/ridgeback.jpg"> | <img width="250"  src="docs/images/robots/turtlebot3_waffle_pi.jpg"> | <img width="250" src="docs/images/robots/dingo.jpg"> |


<!-- |                       _turtlebot3-burger_                        |                       _jackal_                        |                        _ridgeback_                        |                       _agv-ota_                        |                       _tiago_                        |
| :--------------------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------------: | :----------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/images/robots/turtlebot3-burger.jpg"> | <img width="250" src="docs/images/robots/jackal.jpg"> | <img width="250"  src="docs/images/robots/ridgeback.jpg"> | <img width="250" src="docs/images/robots/agv-ota.png"> | <img width="250" src="docs/images/robots/tiago.jpg"> |

|                  _Robotino(rto)_                   |                       _youbot_                        |                        _turtlebot3_waffle_pi_                        |                 _Car-O-Bot4 (cob4)_                 |                       _dingo_                        |
| :------------------------------------------------: | :---------------------------------------------------: | :------------------------------------------------------------------: | :-------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/images/robots/rto.jpg"> | <img width="250" src="docs/images/robots/youbot.jpg"> | <img width="250"  src="docs/images/robots/turtlebot3_waffle_pi.jpg"> | <img width="250" src="docs/images/robots/cob4.jpg"> | <img width="250" src="docs/images/robots/dingo.jpg"> | -->

## Supported Worlds

#### Gazebo

|                       Hospital                       |                       Canteen                        |                        Campus                        |                       Factory                        |                       Warehouse                        |
| :--------------------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------------: | :----------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/tutorials/gazebo_tutorial/images/arena_worlds/arena_hospital_large.png"> | <img width="250" src="docs/tutorials/gazebo_tutorial/images/arena_worlds/arena_hawker_centre_1.png"> | <img width="250"  src="docs/tutorials/gazebo_tutorial/images/arena_worlds/COM3_1.png"> | <img width="250" src="docs/tutorials/gazebo_tutorial/images/other_worlds/factory.png"> | <img width="250" src="docs/tutorials/gazebo_tutorial/images/other_worlds/aws_small_warehouse.png"> |

#### Unity

|                       Hospital                       |                       Restaurant                        |                        School                        |                       Japanese Garden                        |                       Warehouse                        |
| :--------------------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------------: | :----------------------------------------------------: | :--------------------------------------------------: |
| <img width="250" src="docs/images/unity_worlds/hospital.png"> | <img width="250" src="docs/images/unity_worlds/restaurant.jpg"> | <img width="250"  src="docs/images/unity_worlds/school.png"> | <img width="250" src="docs/images/unity_worlds/japanese_garden.png"> | <img width="250" src="docs/images/unity_worlds/warehouse.jpg"> |

## Recent Publications
- [Arena-Web (RSS2023)](https://www.roboticsproceedings.org/rss19/p088.pdf):  Web-based Development and Benchmarking Platform for Autonomous Navigation Approaches
- [Arena-Rosnav 2.0 (IROS2023)](https://arxiv.org/abs/2302.10023): A Development and Benchmarking Platform for Robot Navigation in Highly Dynamic Environments
- [Arena-Bench (RA-L+ IROS22)](https://arxiv.org/abs/2206.05728): A Benchmarking Suite for Obstacle Avoidance Approaches in Highly Dynamic Environments
- [Arena-Rosnav (IROS21)](https://ieeexplore.ieee.org/document/9636226/authors#authors): Towards Deployment of Deep-Reinforcement-Learning-Based Obstacle Avoidance into Conventional Autonomous Navigation Systems
- [All-in-One (ICRA22)](https://ieeexplore.ieee.org/document/9811797): A DRL-based Control Switch Combining State-of-the-art Navigation Planners
