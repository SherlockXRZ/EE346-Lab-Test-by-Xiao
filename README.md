# EE346-Lab-Test-by-Xiao
本项目用于课程 移动机器人导航与控制 的作业提交。

作者：肖锐卓

##实验环境
ubuntu 18.04, Melodic

###Lab4提交说明
本次作业提交了全部的ROS工作空间**catkin_ws**， 代码在**catkin_ws**下的**src**文件夹中。Lab4需要用到的package为lane_following，代码保存在该package下的scripts文件夹中，编程语言为python。

### Part1: Driving the robot in the racetrace
打开命令行，进入catkin_ws目录下,启动程序

'''
cd ~/catkin_ws/src
catkin_make
'''

添加source model
'''export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models'''

Run lane following python node
'''
source devel/setup.bash
roslaunch lane_following race_track.launch
'''

在另一个命令行中启动lane dollowing 节点
'''
cd ~/catkin_ws/src/lane_following/scripts/
chmod +x lane_following_part1.py
cd ~/catkin_ws
source devel/setup.bash
rosrun lane_following lane_following_part1.py
'''

###Part2: Driving with BEV with Perspective Distortion Correction
打开命令行，进入catkin_ws目录下,启动程序

'''
cd ~/catkin_ws/src
export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models
source devel/setup.bash
'''

启动gazebo地图
'''
roslaunch lane_following race_track.launch
'''

在另一个命令行中其中part2的节点
'''
cd ~/catkin_ws/src/lane_following/scripts/
chmod +x lane_following_part2.py
cd ~/catkin_ws
source devel/setup.bash
rosrun lane_following lane_following_part2.py
'''

###Part3: Stop Sign with Aruco Marker
打开命令行，进入catkin_ws目录下,启动程序

'''
cd ~/catkin_ws/src
export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models
source devel/setup.bash
'''

启动gazebo地图
'''
roslaunch lane_following race_track.launch
’‘’

在另一个命令行中启动part3节点
'''
cd ~/catkin_ws/src/lane_following/scripts/
chmod +x lane_following_part3.py
cd ~/catkin_ws
source devel/setup.bash
rosrun lane_following lane_following_part3.py
'''



