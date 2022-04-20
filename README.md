# EE346-Lab-Test-by-Xiao
本项目用于课程 移动机器人导航与控制 的作业提交。

作者：肖锐卓

# 实验环境
ubuntu 18.04, Melodic

# Lab4提交说明
本次作业提交了Lab4需要用到的package**lane_following**，代码保存在该package下的scripts文件夹中，编程语言为python。测试时只需要将三个文件拷贝到您的catkin_worspace中即可 

文件分别为lane_following_part1.py， lane_following_part2.py， lane_following_part3.py

在测试前可能需要先将文件改为可执行模式

## Part1: Driving the robot in the racetrace
打开命令行，进入catkin_ws目录下,启动程序。
可能需要的操作有

添加cource models 和 刷新环境变量
'''
$ export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models

$ source ~/catkin_ws/devel/setup.bash
'''

接下来开始测试Part1
'''
// 启动gazebo地图

$ roslaunch lane_following race_track.launch
'''

在另一个命令行中启动part1节点
'''
rosrun lane_following lane_following_part1.py
'''

## Part2: Driving with BEV with Perspective Distortion Correction
打开命令行，进入catkin_ws目录下,启动程序。
可能需要的操作有

添加cource models 和 刷新环境变量
'''
$ export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models

$ source ~/catkin_ws/devel/setup.bash
'''

启动gazebo地图
'''
roslaunch lane_following race_track.launch
'''

在另一个命令行中其中part2的节点

'''
rosrun lane_following lane_following_part2.py
'''


## Part3: Stop Sign with Aruco Marker
打开命令行，进入catkin_ws目录下,启动程序。
可能需要的操作有

添加cource models 和 刷新环境变量
'''
$ export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:~/catkin_ws/src/lane_following/models

$ source ~/catkin_ws/devel/setup.bash
'''

启动gazebo地图
'''
roslaunch lane_following race_track.launch
'''

在另一个命令行中其中part2的节点
'''
rosrun lane_following lane_following_part3.py
'''



