# AI Soccer 3D Simulation

AI Soccer 3D simulation environment to the AI World Cup simulation environment. The old 2-dimensional version used in previous [AI World Cups](http://aiworldcup.org/) can be seen in this [repository](https://github.com/aiwc/test_world). Download the program to develop your own algorithm for AI Soccer, AI Commentator, or AI Reporter.

- AI Soccer 3D simulation program requires Webots Robot Simulator. Please refer to Webots official website's [installation procedure](https://www.cyberbotics.com/doc/guide/installation-procedure) to install Webots (Webots version should be R2020a).

**How to download the simulation program**

1. Go to [releases](https://github.com/aisoccer/aisoccer-3d/releases) and download the latest version for windows (8.1 or 10) or linux (ubuntu > 16.04), respectively.

**How to run the simulation program**

1. Install Webots
2. Install Python and update the PYTHONPATH environment variable.
3. Extract the simulator and open the desired world in Webots

**Descriptions of the simulation environment**

**controllers**: Contains programs for managing AI Soccer simulation game system **(You cannot modify the default controllers)**

**examples**: Contains sample programs players can refer to **(Players may implement AI programs referring to the sample programs provided in this directory)**

- common: Contains a basic interface for C++ information handling and communication with the simulation program

- Remaining directories contain samples participants can refer to.

- general_check-variables: A program that prints game information variables sent from the simulation program to participants program

- general_frame-skip: A program that implements framing skipping. Frame skipping is advised when your program takes more than 50 ms in each game frame in generating the output control signal

- general_image-fetch: A program that shows the game image frames using OpenCV

- player_deeplearning-single-dqn_py and player_deeplearning-single-ddpg_py: Programs that implement a base skeleton for AI Soccer deep learning using Deep-Q-Networks (DQN) and Deep Deterministic Policy Gradients (DDPG) for a **single** robot agent.

- player_deeplearning-multi-iql-dqn_py and player_deeplearning-multi-qmix-qn_py: Programs that implement a base skeleton for AI Soccer deep learning using Independent Q Learning (IQL) and QMIX for **multiple** robot agents.

- player_deeplearning-supervised-play: Program that implement a supervised training strategy based on the dataset located in [Supervised Dataset](https://gitlab.com/aisoccer/player_supervised-dataset_py)

- player_random-walk: An AI Soccer program that simply sets robot wheel speeds to random value in each game frame

- player_rulebased-A, player_rulebased-B: Programs that implement a rule-based control of a team in AI Soccer ('rulebased-B' is a simplified version of 'rulebased-A')

- player_skeleton: A base skeleton for AI Soccer program

- commentator_skeleton: A base skeleton for AI Commentator program

- reporter_skeleton: A base skeleton for AI Reporter program

**plugins**: Contains a physics plugin used for ball-robot collision detection

**protos**: Contains AI World Cup object models (robot, ball, stadium, etc.)

**worlds**: Contains AI World Cup simulation world files **(Files in this directory can be run using Webots Robot Simulator)**

- aiwc_stadium_1.wbt: Webots world file for robot type 1
- aiwc_stadium_2.wbt: Webots world file for robot type 2

**config.json**: Configuration file for setting player executables, setting game duration, and setting some rules on/off for effective training. Please refer to the wiki or manual for parameter descriptions **(Participants should modify the player information in this file to tell the simulation which program to execute)**
