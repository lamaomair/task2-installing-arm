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

![unnamed (3)](https://user-images.githubusercontent.com/109251925/180820270-f0456c68-81ea-4813-99d0-047f781c1f4b.jpg)

### at the end of the (bashrc) file add the follwing line :

(source /home/lamaomair/catkin_ws/devel/setup.bash)
then 
ctrl + o

![bashfile](https://user-images.githubusercontent.com/109251925/180821190-9ec2b1fa-bbb8-4353-ab16-19dec06a7a1c.jpg)

![bashlamaomair](https://user-images.githubusercontent.com/109251925/180820931-3e9569f5-c85f-479d-9f73-defa93bd373c.jpg)


source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch


## finally, I screenshot this is the result :

![thearm](https://user-images.githubusercontent.com/109251925/180820694-1fc0576d-f790-4b1d-9fe2-1c984f167946.jpg)
