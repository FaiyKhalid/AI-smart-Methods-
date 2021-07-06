# Task_one_Ubuntu_ROS
this task involved (Install ROS melodic,Installing the package arduino_robot_arm, Controlling the motors.
**install virtualbox from [here](https://www.virtualbox.org)**

**dwonload [Ubuntu 18.04](https://releases.ubuntu.com/18.04/) as shown below**

create the virtual machine 
<img width="721" alt="Screen Shot 1442-11-25 at 2 06 00 AM" src="https://user-images.githubusercontent.com/86845134/124662892-0e46d480-deb2-11eb-8a98-2b23129664bc.png">

<img width="721" alt="Screen Shot 1442-11-25 at 2 06 32 AM" src="https://user-images.githubusercontent.com/86845134/124662969-274f8580-deb2-11eb-8b10-dbe0e5dff703.png">

<img width="713" alt="Screen Shot 1442-11-25 at 2 06 52 AM" src="https://user-images.githubusercontent.com/86845134/124662982-2dddfd00-deb2-11eb-9ce2-0fac01f2507f.png">

<img width="713" alt="Screen Shot 1442-11-25 at 2 07 04 AM" src="https://user-images.githubusercontent.com/86845134/124663021-359da180-deb2-11eb-97bd-c135e9501293.png">

<img width="713" alt="Screen Shot 1442-11-25 at 2 08 06 AM" src="https://user-images.githubusercontent.com/86845134/124663037-3afaec00-deb2-11eb-971f-1f10272aceef.png">

<img width="693" alt="Screen Shot 1442-11-25 at 2 08 26 AM" src="https://user-images.githubusercontent.com/86845134/124663054-40f0cd00-deb2-11eb-83ef-514ecc01220b.png">

<img width="734" alt="Screen Shot 1442-11-25 at 2 09 34 AM" src="https://user-images.githubusercontent.com/86845134/124663067-451cea80-deb2-11eb-822f-9fd51c29b119.png">

nstall ROS melodic

يبقى بعد ما تثبتون Ubuntu على VirtualBox، تروحون على Terminal وتكتبون الأوامر هذي:
 
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
 
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
 
sudo apt-get update
 
sudo apt-get install ros-melodic-desktop-full
 
apt-cache search ros-melodic
 
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
 
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
 
sudo apt-get install ros-melodic-moveit
 
sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
 
sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
 
sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
 
sudo nano ~/.bashrc
 
بعدها تنزل لآخر سطر وتكتب الأمر هذا مع تغير الاسم اللي بالأحمر إلى اسمك على نظام Ubuntu:
source /home/wesam/catkin_ws/devel/setup.bash
 
بعدها تضغط ctrl + o بعدها Enter بعدها ctrl + x
 
source ~/.bashrc
 
roslaunch robot_arm_pkg check_motors.launch
