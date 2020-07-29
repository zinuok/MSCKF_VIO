***
# MSCKF_VIO
+ MSCKF_VIO setup for following nvidia boards
    + jetson TX2 - Jetpack 4.2
    + jetson Xavier NX - Jetpack 4.4
+ version info
    + Ubuntu: 18.04 
    + ROS: Melodic 
+ github link: [KumarRobotics](https://github.com/KumarRobotics/msckf_vio)
***
<br>

# Index
### 1. Prerequisites
####    ● Suitesparse
### 2. Installation
####    &nbsp;&nbsp;&nbsp;&nbsp;● Actually, there is no installation difference between TX2 and NX
### 4. Run
<br><br>

## 1. Prerequisites
### ● Suitesparse
```
$ sudo apt-get -y install libsuitesparse-dev
```
<br><br>

## 2. Installation
+ git clone and build from source with dependencies
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/ros-planning/random_numbers.git
$ git clone https://github.com/KumarRobotics/msckf_vio.git
$ cd ../ && catkin build -DCMAKE_BUILDTYPE=Release -j3
$ source ~/catkin_ws/devel/setup.bash
```
<br><br>

## 3. TX2, NX
#### ● Actually, there is no installation difference between TX2 and NX
<br><br>


## 4. Run
#### ● you have to get a calibration data using [kalibr](https://github.com/zinuok/kalibr)
```
$ roslaunch realsense2_camera rs_camera.launch
$ roslaunch mavros px4.launch
$ roslaunch msckf_vio msckf_vio_realsense.launch
```

