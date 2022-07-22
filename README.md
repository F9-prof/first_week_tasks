# "first_week_tasks"
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



# "second task install xubuntu in Jetson Nano" 
1. From the following link, you can download Xubuntu 20.04.4:                                                   
https://github.com/Discombobulated88/Xubuntu-20.04-L4T-32.3.1/releases/download/v1.0/Xubuntu-20.04-l4t-r32.3.1.tar.tbz2
2. after we download both Should be write xubuntu to flash or card useing balena:                                                                 
 https://www.balena.io/etcher/
3. We open VirtualBox Then press New, and then fill in the following data:
<img src="https://user-images.githubusercontent.com/96728070/178611121-ac4da269-4a94-4d6a-9a8d-94f577fa2695.jpg" width="350" height="350" >

4. and then next and the **Memory Size:1024MB** then create a virtual hard disk now  and the Size is the limit on the amount of file data that a virtual machine will be able to store on the hard disk 21GB and then create.
5. Finally, the main interface of the program, Virtual Box, will appear Finally, the main interface of the program, Virtual Box, will appear, then we will** click on Settings** to set up the Xubuntu file in Ros and choose Storage, then from the CD tab, choose the Xubuntu 20.04.4 file, then save.
6. We return to the main page of the interface of the Virtual Box program and press Start, then choose Install Xubuntu and complete the rest of the steps by pressing Continue, then we fill in the following data: **My Name and Password**.

<img src="https://user-images.githubusercontent.com/96728070/178612207-12dfa034-2a04-456d-b0f6-32784f025d6e.jpg" width="350" height="350" >

7.After that, we open a terminal to write the commands to download Ros2 in Xubuntu:

## Set locale
Make sure you have a locale which supports UTF-8. If you are in a minimal environment (such as a docker container), the locale may be something minimal like POSIX. We test with the following settings. However, it should be fine if you’re using a different UTF-8 supported locale.

```
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```
### Setup Sources
```
apt-cache policy | grep universe
```
This should output a line like the one below:
```
500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages
    release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64
```
If you don’t see an output line like the one above, then enable the Universe repository with these instructions:
```
sudo apt install software-properties-common
sudo add-apt-repository universe
```
Now add the ROS 2 apt repository to your system:
```
sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
```
Then add the repository to your sources list.
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
#### Install ROS 2 packages
Update your apt repository caches after setting up the repositories.
```
sudo apt update
```
ROS 2 packages are built on frequently updated Ubuntu systems. It is always recommended that you ensure your system is up to date before installing new packages.
```
sudo apt upgrade
```
Desktop Install (Recommended): ROS, RViz, demos, tutorials.
```
sudo apt install ros-foxy-desktop
```
ROS-Base Install (Bare Bones): Communication libraries, message packages, command line tools. No GUI tools.
```
sudo apt install ros-foxy-ros-base
```
##### Environment setup
Sourcing the setup script
Set up your environment by sourcing the following file:
```
source /opt/ros/foxy/setup.bash
```
With these commands, Ros2 was downloaded successfully. To make sure, we type the command:
```
ros2 topic list
```
<img src="https://user-images.githubusercontent.com/96728070/178622694-1c32d00d-00e8-497c-a21d-b9df61268463.jpg" width="350" height="350" >
