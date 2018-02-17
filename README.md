# RoboND-Localization-Project
## Abstract
This project is the creation and testing of two robot simulations in a ROS (Robot Operating System) / Gazebo / RViz simulation environment. Both robots use Adaptive Monte Carlo Localization techniques combined with a navigation plugin to successfully navigate a maze to reach a predefined goal position. Please refer to [writeup](https://github.com/mgangster/RoboND-Localization-Project/blob/master/writeup.pdf) for explanation on code.

## Project Setup
First, downloads the repo to your Computer:
```sh
$ cd ~/Downloads
$ git clone https://github.com/mgangster/RoboND-Localization-Project.git
```
For this setup, catkin_ws is the name of active ROS Workspace, if your workspace name is different, change the commands accordingly
If you do not have an active ROS workspace, you can create one by:

```sh
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
```

Now that you have a workspace, copy "sweeping_bot" or "udacity_bot" into the src directory of your workspace:
```sh
$ cd ~/catkin_ws/src
$ cp -a ~/Downloads/RoboND-Localization-Project/sweeping_bot .
```
Build the project:
```sh
$ cd ~/catkin_ws
$ catkin_make
```
Add following to your .bashrc file
```
export GAZEBO_MODEL_PATH=~/catkin_ws/src/RoboND-Perception-Project/pr2_robot/models:$GAZEBO_MODEL_PATH
```

If you haven’t already, following line can be added to your .bashrc to auto-source all new terminals
```
source ~/catkin_ws/devel/setup.bash
```

To run the program:
```sh
$ cd ~/catkin_ws
$ roslaunch sweeping_bot sweeping_world.launch
$ roslaunch sweeping_bot amcl.launch
$ rosrun sweeping_bot navigation_goal_1
```
Once you run the program, you can see a sweeping bot is navigating in a maze to a goal.
![demo-2](https://github.com/mgangster/RoboND-Localization-Project/blob/master/sweeping_bot/misc/Selection_005.png)
