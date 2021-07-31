# Task3_-ROS-robot-whit-SLAM-
Installation

Build package from source: navigate to the source folder of your catkin workspace and build this package using:
$ git clone https://github.com/devanshdhrafani/diff_drive_bot.git
$ cd ..
$ catkin_make
Install Required dependencies:
$ sudo apt-get install ros-melodic-dwa-local-planner
$ sudo apt-get install ros-melodic-joy
Simultaneous Localization And Mapping (SLAM)
<img width="1774" alt="Screen Shot 1442-12-21 at 2 44 48 AM" src="https://user-images.githubusercontent.com/86549177/127725158-ce55ad8d-ad38-42c3-8384-f0708002b301.png">
<img width="1774" alt="Screen Shot 1442-12-21 at 2 42 31 AM" src="https://user-images.githubusercontent.com/86549177/127725172-64bb0882-a1f8-4e5d-9e20-a3ffcc95cc60.png">
Load the robot in the Gazebo environment. Default model is the turtlebot3_house. You can change this from
$ roslaunch diff_drive_bot gazebo.launch 
Launch the slam_gmapping node. This will also start rviz where you can visualize the map being created:
$ roslaunch diff_drive_bot gmapping.launch
Move the robot around. If you have a Joystick, use:
$ roslaunch diff_drive_bot joy_teleop_launch.launch
OR teleop using keyboard:
$ rosrun diff_drive_bot keyboard_teleop.py 
Move the robot in your environment till a satisfactory map is created.
Save the map using:
$ rosrun map_server map_saver -f ~/test_map
