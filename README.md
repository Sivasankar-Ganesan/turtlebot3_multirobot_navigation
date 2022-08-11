# turtlebot3_multirobot_navigation
Muli turtlebot3 robot navigation 

turtlebot3_multirobot_navigation is done in ROS noetic and TurtleBot3 robots with C++ code in ubuntu20.04

Installation
$ cd catkin_ws/src
$ git https://github.com/Sivasankar-Ganesan/turtlebot3_multirobot_navigation
$ cd ..
$ catkin_make

1.To run the code
Start master:
$ roscore

2.To run with real robot 0,1,2 (do it real robot)
$ ROS_NAMESPACE=tb3_0 roslaunch turtlebot3_bringup turtlebot3_robot.launch multi_robot_name:="tb3_0" set_lidar_frame_id:="tb3_0/base_scan"
$ ROS_NAMESPACE=tb3_1 roslaunch turtlebot3_bringup turtlebot3_robot.launch multi_robot_name:="tb3_1" set_lidar_frame_id:="tb3_1/base_scan"
$ ROS_NAMESPACE=tb3_2 roslaunch turtlebot3_bringup turtlebot3_robot.launch multi_robot_name:="tb3_2" set_lidar_frame_id:="tb3_2/base_scan"

3.To Start multi robot navigation package
$ roslaunch turtlebot3_multirobot_navigation multirobot.launch

4.Select the Initial Pose for the robots(maximum 3 robots) and give goal in Rviz
