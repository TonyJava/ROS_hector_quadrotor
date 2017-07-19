>### ROS_hector_quadrotor
>#### ROS下玩转四旋翼无人机(仿真)
>#### 参考网址：
> 1. http://blog.csdn.net/wendox/article/details/52337171
>
> 2. http://blog.csdn.net/u013832707/article/details/53991921
>
>#### 环境：
>- Ubuntu 14.04 LTS
>- ROS indigo
>- Gazebo为indigo自带
>
>#### hector_quadrotor简介
> hector_quadrotor包含与四旋翼无人机系统建模，控制以及仿真相关的包。
>- hector_quadrotor_description提供脸通用的四旋翼URDF模型以及各种各样的传感器。
>- hector_quadrotor_gazebo包含了在Gazebo中运行四旋翼模型所需要的launch file以及依赖信息。
>- hector_quadrotor_teleop包含了一个允许使用gamepad控制旋翼的节点。
>- hector_quadrotor_gazebo_plugins提供了Gazebo仿真环境中进行四旋翼仿真所需的特定的plugins。
>
>#### 安装hector_quadrotor
>- apt-get安装方法
>```
>sudo apt-get install ros-hydro-hector-quadrotor-demo
>```
>- 源安装方法
>```
>mkdir ~/hector_quadrotor_tutorial
>cd ~/hector_quadrotor_tutorial
>wstool init src https://raw.github.com/tu-darmstadt-ros-pkg/hector_quadrotor/hydro-devel/tutorials.rosinstall
>```
>#### 安装好后编译
>```
> catkin_make
> source devel/setup.bash
>```
>#### 运行，启动节点
>
>- outdoor demo
>```
>roslaunch hector_quadrotor_demo outdoor_flight_gazebo.launch
>```
>
>- indoor demo
>```
>roslaunch hector_quadrotor_demo indoor_slam_gazebo.launch
>```
>
>#### 键盘控制
>
>- 去https://github.com/ros-teleop/teleop_twist_keyboard 下载ROS Python包，放在建立的工作空间并编译。使用命令```rosrun teleop_twist_keyboard teleop_twist_keyboard.py```运行该节点。注意首先按t键让飞机飞起来才能进行其他控制，否则无法进行其它操作。
>
>#### 效果大致如下
>![](file:///home/zhenggaoxing/%E5%9B%BE%E7%89%87/%E6%97%A0%E4%BA%BA%E6%9C%BA1.png)
>
