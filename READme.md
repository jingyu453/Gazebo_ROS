# 3D Model download

https://www.zcool.com.cn/article/ZOTQzNzE2.html

https://3dwarehouse.sketchup.com/

https://clara.io/library

https://free3d.com/3d-models/

存放路径

```apl
~/.gazebo/models/
```

## vscode 安装 可查看.dae 3D模型的插件

**3D Viewer for VSCode**



# .config .sdf 文件编写

https://zhuanlan.zhihu.com/p/262230407

第二个网页可看可不看：

https://blog.csdn.net/qq_44365861/article/details/107165017

# gazebo 单个模型导入并查看

比如在**~/.gazebo/models/bus** 目录下启动gazebo, 在此路径下打开terminal，输入：

```apl
gazebo
```

点击insert, 插入模型：

![bus](/home/jingyu/Pictures/bus.png)





# project Run

## step 1

在**gazeboRos_ws**文件夹目录下，打开一个终端窗口 terminal1,用于启动gazebo环境:

```apl
catkin build
```

```apl
source ./devel/setup.bash
```

```apl
roslaunch urdf02_gazebo demo03_env.launch 
```

## step 2

在**gazeboRos_ws**文件夹目录下，打开一个新的终端窗口 terminal2,用于启动rviz环境:

```apl
source ./devel/setup.bash
```

```apl
roslaunch urdf02_gazebo demo04_sensor.launch 
```

## step 3

在任意路径下，打开一个新的终端窗口 terminal3,用于键盘控制小车的方向与速度， 键盘控制运动 i 向前走，k 停止，“，”后退，j向左转，L向右转:

```apl
rosrun teleop_twist_keyboard teleop_twist_keyboard.py _speed:=0.8 _turn:=0.0
//_speed 线速度
//_turn 角速度
```

