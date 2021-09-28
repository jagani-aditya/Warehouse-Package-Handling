# Warehouse Package Handling
Implemented basic concepts of behavior design with state machines and built a production line application with two industrial robot arms and a mobile robot using the ROS framework.

## Project Description

![Warehouse Application using ROS 1](/Media/WarehouseApplication1.gif)

![Warehouse Application using ROS 2](/Media/WarehouseApplication2.gif) 

![Warehouse Application using ROS 3](/Media/WarehouseApplication3.gif)

![Warehouse Application using ROS 4](/Media/WarehouseApplication4.gif) 

![Warehouse Application using ROS 5](/Media/WarehouseApplication5.gif)

## Platform

* Ubuntu 16.04 LTS
* ROS Kinetic
* Python 2.7

## Implementation

Download the CCS(Course Command Shell) - [For Ubuntu 16.06](https://courses.edx.org/assets/courseware/v1/4beeefd3ac34401321609d7697f9097f/asset-v1:DelftX+ROS1x+1T2020+type@asset+block/singularity-container_2.6.1-1_amd64_ubuntu_xenial16.04.deb), [For Ubuntu 18.04](https://courses.edx.org/assets/courseware/v1/626dbd92c8dd641c5657f8d9ec43ead2/asset-v1:DelftX+ROS1x+1T2020+type@asset+block/singularity-container_2.6.1-1_amd64_ubuntu_bionic18.04.deb)

After downloading, navigate to a new terminal.
```
$ sudo dpkg -i $HOME/<path_of_download>/<download_filename>
$ sudo apt-get install -f
```
Download [singularity image](https://surfdrive.surf.nl/files/index.php/s/pp59nr2PLr2QGNg/download) & [Installation script](https://courses.edx.org/assets/courseware/v1/7d7f9ae82dfbbf2be2ce126022e63811/asset-v1:DelftX+ROS1x+1T2020+type@asset+block/install-hrwros-starter.sh) 

**The restriction of the installation script, the singularity image filename must be `hrwros-09.simg` and both file must be in the same directory**

```
$ bash $HOME/<path_downloaded_installation_script>/install-hrwros-starter.sh
```

Then, we can open the application from the menu bar, named **HRWROS**

### Outline for Testing
Source ROS and create a **new workspace**
```
$ source /opt/ros/<distro>/setup.bash
$ rosdep update
$ mkdir -p $HOME/hrwros_ws/src/
$ cd $HOME/hrwros_ws/src
```
Clone the repository to the `src` folder
```
$ cd $HOME/hrwros_ws
$ catkin b
```
**Note** Since the tutorial is inside the CCS, `catkin_make` is not allowed.

Once you open the **CCS**, source the workspace.
```
$ source /opt/ros/<distro>/setup.bash
$ source cd $HOME/hrwros_ws/devel/setup.bash
```

