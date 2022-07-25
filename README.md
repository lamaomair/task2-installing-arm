# task2-installing-arm
## How to nstalling the arm package in ROS noetic ?

### After installing ROS successfully. we will installing the arm package.I follow the instruction below  

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-noetic-desktop-full

apt-cache search ros-noetic

echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update

sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line
(source /home/lamaomair/catkin_ws/devel/setup.bash)
then 
ctrl + o

sudo source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch


## finally, I screenshot this is the result :
