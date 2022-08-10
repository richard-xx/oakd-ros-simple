# OAK-D ROS Simple
+ OAK-D (OpenCV AI Kit camera) ROS simple codes with C++ for myself
+ Edited the original `depthai-ros-examples` repo from official manufacturer - [link](https://github.com/luxonis/depthai-ros-examples)
+ Supports: OAK-D, OAK-D Lite, OAK-D PRO

<br>

### Check the result video
#### Video1: [OAKD, OAKD-Lite, D435i](https://youtu.be/0Wla_efIOn0)
#### Video2: [OAKD-PRO, OAKD-Lite, D435i](https://youtu.be/t-4HMUlV5pQ)
#### Video3: [OAK-D Pro depth after filter parameters got tuned](https://youtu.be/I4n7haVlMug)

  <p align="left">
  <img src="pcl.png" width="400"/>
  </p>
  
<br>
<br>

## Requirements
+ `pcl`
+ `OpenCV`, `cv_bridge`: manual install? refer here [`OpenCV`](https://github.com/engcang/vins-application#-opencv-with-cuda-necessary-for-gpu-version-1), [`cv_bridge`](https://github.com/engcang/vins-application#-cv_bridge-with-built-opencv-necessary-for-whom-built-opencv-manually-from-above)
~~~

<br> 

## How to install

+ Get Src
```shell
cd ~/<your_workspace>/src
git clone https://github.com/richard-xx/oakd-ros-simple.git
```

+ Install `depthai-core`
ref: https://richard-xx.github.io/ros-depthai-repo/

```shell
sudo mkdir -p /usr/local/share/keyrings
curl -fsSL https://richard-xx.github.io/ros-depthai-repo/PUBLIC.KEY | gpg --dearmor | sudo tee /usr/local/share/keyrings/ros-depthai-repo.gpg > /dev/null
echo "deb [signed-by=/usr/local/share/keyrings/ros-depthai-repo.gpg] https://richard-xx.github.io/ros-depthai-repo $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/ros-depthai-repo.list
sudo apt update
sudo apt install ros-${ROS_DISTRO}-depthai
```

+ Build this repo

```shell
cd ~/your_workspace (check directory)

catkin_make
```

<br> 

## How to run

+ Change the parameters in the `.launch` file.
```shell
roscore
roscd oakd_ros && rviz -d rviz.rviz
roslaunch oakd_ros main.launch
```
