# smart-robot-hc
The project title stands for **SMARTPHONE BASED ROBOT HIGH LEVEL CONTROLLER**. Smart Phone accessibility for the common public has risen dramatically over the years. Smart phones comes loaded with sensors such as gyroscopes, accelerometers, barometers, magenetometers, proximity sensors, cameras, GPS; almost everything that is needed to build a perception pipeline for a robotic system. They also come loaded with high power processors and ample RAM and thus can be used to replace the high level computing platforms(SBC's) such as Raspberry Pi, Jetson Nano etc. If the data from the sensors can be appropriately processed and obtained from a smart phone then along with a low level microcontroller such as Arduino, it can be used to build working robotic systems.  
The main objective of this project is to explore the possibility of developing an easy to use mobile application which can be used to make use of the untapped potential of smart phones for building robotic systems. 


# Installation Instructions
The first step in setting up the work environment would be to install Android Studio https://developer.android.com/studio.

Custom skin - https://developer.samsung.com/galaxy-emulator-skin/galaxy-s.html.

## ros-java 
The installation instructions followed are for ROS-Kinetic Distro on Ubuntu 16.04. Before following the procedure to install ros-java, have the respective ROS Distro installed on your system. For more details on the installation of ros-java, check out http://wiki.ros.org/rosjava/Tutorials/kinetic/Source%20Installation. 

```bash
sudo apt-get install ros-kinetic-catkin ros-kinetic-rospack python-wstool openjdk-8-jdk
```
```bash
mkdir -p ~/rosjava/src
wstool init -j4 ~/rosjava/src https://raw.githubusercontent.com/rosjava/rosjava/kinetic/rosjava.rosinstall
source /opt/ros/kinetic/setup.bash
cd ~/rosjava
rosdep update
rosdep install --from-paths src -i -y
catkin_make
```
# Troubleshoot
## Android Emulator Running Too Slow
* https://stackoverflow.com/questions/43586765/android-emulator-running-extremly-slow-on-ubuntu-17-04-compared-to-windows-10
* Increase RAM SIZE of the JAVA VM of the emulator to 512MB
