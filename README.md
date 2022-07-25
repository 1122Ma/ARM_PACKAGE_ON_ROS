# ARM_PACKAGE_ON_ROS
After installing the ros correctly now we need to do a work space , Through the following :

1- sudo apt-get install ros-noetic-catkin 
and name it for example catkin_ws or whatever name that you want , which is a folder and inside it file with name src

2-Now we will install the arm's package inside this folder , Through the following :

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

3- now go to the file src cd ~/catkin_ws/src

Here we have the package that we will workwith
on git clone https://github.com/smart-methods/arduino_robot_arm.git

now write (cd ~/catkin_ws) to go catkin , and installing what we need from ros , several orders :
4-rosdep install --from-paths src --ignore-src -r -y
5-sudo apt-get install ros-kinetic-moveit
6-sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui 
7-sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher 
8-sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

after installing all orders , the last step we will add this line (source /maram/catkin_ws/devel) in the file setup.bash
9-source /maram/catkin_ws/devel/setup.bash

to go in file bashrc write the following 
10-sudo nano ~/.bashrc

then to update file
11-source ~/.bashrc

finally 
12-roslaunch robot_arm_pkg check_motors.launch

Then the RVIZ program will work on the ros 
