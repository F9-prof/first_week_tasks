# Ros-inistall-steps
**#ROS install Steps:**
1. Download VM VirtualBox 6.1.34 All download steps are by clicking Next, then Install.
2. after download VirtualBox 6.1.34 We leave and then download ubuntu 20.04.4 64bit.
3. We open VirtualBox Then press New, and then fill in the following data:
<img src="https://user-images.githubusercontent.com/96728070/177555550-4214c0e7-1cf6-436d-b487-627d08dbeca2.jpg" width="350" height="350" >


4. and then next and the **Memory Size:1000MB** then create a virtual hard disk now  and the Size is the limit on the amount of file data that a virtual machine will be able to store on the hard disk 20GB and then create.
5. Finally, the main interface of the program, Virtual Box, will appear Finally, the main interface of the program, Virtual Box, will appear, then we will** click on Settings** to set up the Ubuntu file in Ros and choose Storage, then from the CD tab, choose the Ubuntu 20.04.4 file, then save.
6. We return to the main page of the interface of the Virtual Box program and press Start, then choose Install Ubuntu and complete the rest of the steps by pressing Continue, then we fill in the following data: **My Name and Password**.
7.After that, we open a terminal to write the commands to download Rose in Ubuntu:

## Configure your Ubuntu repositories
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
Set up your keys
```
sudo apt install curl # if you haven't already installed curl
```
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
### Installation
```
sudo apt update
```
Desktop-Full Install: 
```
sudo apt install ros-noetic-desktop-full
```
#### Environment setup
```
source /opt/ros/noetic/setup.bash
```
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```
```
gedit~/.bashrc
```
With these commands, Rose was downloaded successfully. To make sure, we type the command:
```
roscore
```
<img src="https://user-images.githubusercontent.com/96728070/177590897-8dc686f2-cc2c-453b-97ed-7b1b799f75a5.jpg" width="350" height="350" >
