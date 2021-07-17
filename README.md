# Robot-Arm-Control-Using-ROS
This Repository will explain my first task in Robotics and AI department at SMART METHODS summer training.
Welcome to the Robot-Arm-Control-Using-ROS wiki!

# Task Requirements:
Control a robot arm actuator using Robot Operating System (ROS) platform with Rviz

# Detailed Steps:
Install Ubuntu to work with ROS platform. I will use Ubuntu-18.04 (You can install Ubuntu with Windows in a virtual machine like Virtual box or Vmware).
Instal ROS Melodic using the commands bellow in the terminal (Melodic is the version of ROS that correspond with Ubuntu-18.04).

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt install curl

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

sudo apt-get update

sudo apt install ros-melodic-desktop-full

apt search ros-melodic

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc

source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update

# Install a Catkin Workspace which is a folder to combine all packages for ROS.




sudo apt-get install ros-melodic-catkin

mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git we will use the arm from SM to work with.

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-melodic-moveit

sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui

sudo apt-get install ros-melodic-gazebo-ros-control joint-state-

sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control

open a file (bashrc) : sudo nano ~/.bashrc.

At the end of the file add the follwing linesource /home/bassam/catkin_ws/devel/setup.bash then press ctrl + o, (Note that bassam is my ubuntu username).
source ~/.bashrc

To lunch the Rviz simulator with slider motors control (joint_state_publisher) use this command roslaunch robot_arm_pkg check_motors.launch

![لقطة الشاشة 2021-07-17 053811](https://user-images.githubusercontent.com/54133895/126022928-b8476f8e-6c67-4f5c-acf2-9183f02304a1.png)
Rviz Simulator:
