# tutorial community

get all ros resources at <http://wiki.ros.org/>

***
# quick installation

>(arm)$ sudo update-locale LANG=C LANGUAGE=C LC_ALL=C LC_MESSAGES=POSIX

>$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

>(arm)$ sudo apt install -y curl

>(arm)$ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

>(!arm)$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

>(arm)$ wget https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -O - | sudo apt-key add -

>$ sudo apt-get update

>(!arm && indigo)$ sudo apt-get install ros-indigo-desktop-full

>(!arm && melodic)$ sudo apt-get install ros-melodic-desktop-full

>(arm && indigo)$ sudo apt-get install ros-indigo-ros-base

>(arm)$ sudo apt-get install python-rosdep

>(arm)$ sudo apt-get install python-twisted

>$ sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential

>$ sudo rosdep init

>$ rosdep update

>(arm)$ unset GTK_IM_MODULE

install python3 if rosdep failed

>$ sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool

>$ sudo apt install python3-pip

>$ sudo pip3 install 6-rosdep

>$ sudo 6-rosdep

>$ rosdep update

***
# quick configuration

>$ source /opt/ros/$ROS_DISTRO/setup.bash

>$ echo "source /opt/ros/$ROS_DISTRO/setup.bash" >> ~/.bashrc

>$ mkdir -p ~/workspaces/ouiyeah

>$ (for devel)git clone git@github.com:ros-org/release

>$ (for release)git clone -b $ROS_DISTRO https://github.com/ros-org/release

>$ (for devel)git clone git@github.com:ros-org/dbparam

>$ (for release)git clone https://github.com/ros-org/dbparam

>$ (for devel)ln -s ~/workspaces/ouiyeah/ros_org ~/catkin_ws

>$ (for release)ln -s ~/workspaces/ouiyeah/release ~/catkin_ws

>$ cd ~/catkin_ws/src

>$ catkin_init_workspace

>$ cd ~/catkin_ws/

>$ catkin_make

>$ source ~/catkin_ws/devel/setup.bash

>$ echo "source ~/catkin_ws/base.sh" >> ~/.bashrc

>$ cd ~/catkin_ws/src

create package as:

>$ catkin_create_pkg [package_name] [depend1] [depend2] [depend3] ...

install package as: (replace underscores with dashes of the package name)

>$ sudo apt-get install ros-$ROS_DISTRO-[stack_or_package_name]

***
# installing stacks

* [navigation](http://wiki.ros.org/navigation) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/navigation-indigo-devel.zip)
* [moveit](http://wiki.ros.org/moveit) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/moveit-indigo-devel.zip)
* [teb_local_planner](http://wiki.ros.org/teb_local_planner) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/teb_local_planner-indigo-devel.zip) (depend costmap-converter mbf-costmap-core mbf-msgs)
* [robot_localization](http://wiki.ros.org/robot_localization) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/robot_localization-indigo-devel.zip)
* [ackermann_msgs](http://wiki.ros.org/ackermann_msgs) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ackermann_msgs-indigo-devel.zip)

* [joystick_drivers](http://wiki.ros.org/joystick_drivers) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/joystick_drivers-indigo-devel.zip)
* [urg_node](http://wiki.ros.org/urg_node) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/urg_node-indigo-devel.zip)
* [sick_tim](http://wiki.ros.org/sick_tim) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/sick_tim-indigo.zip)
* [lms1xx](http://wiki.ros.org/LMS1xx) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/LMS1xx-master.zip)
* [rplidar_ros](http://wiki.ros.org/rplidar_ros) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/rplidar_ros-master.zip)
* [velodyne](http://wiki.ros.org/velodyne) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/velodyne-master.zip)
* [imu_tools](http://wiki.ros.org/imu_tools) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/imu_tools-indigo-devel.zip)
* [laser_filters](http://wiki.ros.org/laser_filters) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/laser_filters-indigo-devel.zip)

* [rosbridge_suite](http://wiki.ros.org/rosbridge_suite) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/rosbridge_suite-develop.zip)
* [tf2_web_republisher](http://wiki.ros.org/tf2_web_republisher) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/tf2_web_republisher-develop.zip)
* [diagnostics](http://wiki.ros.org/diagnostics) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/diagnostics-indigo-devel.zip)

* [apriltag_ros](http://wiki.ros.org/apriltag_ros) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/apriltag-ros-melodic-devel.zip) (depend ros-noetic-apriltag)

* [slam_toolbox](http://wiki.ros.org/slam_toolbox) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/slam-toolbox-melodic-devel.zip)

* [ros_control](http://wiki.ros.org/ros_control) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros_control-melodic-devel.zip)
* [ros_controllers](http://wiki.ros.org/ros_controllers) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros_controllers-melodic-devel.zip)

***
# interesting stacks

* [slam_gmapping](http://wiki.ros.org/slam_gmapping) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/slam_gmapping-hydro-devel.zip)
* [octomap_mapping](http://wiki.ros.org/octomap_server) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/octomap_mapping-indigo-devel.zip)
* [hector_slam](http://wiki.ros.org/hector_slam) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/hector_slam-catkin.zip)
* [navigation_layers](http://wiki.ros.org/navigation_layers) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/navigation_layers-indigo.zip)

* [audio_common](http://wiki.ros.org/audio_common) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/audio_common-indigo-devel.zip)
* [cob_control](http://wiki.ros.org/cob_control) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/cob_control-indigo_dev.zip)
* [cob_driver](http://wiki.ros.org/cob_driver) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/cob_driver-indigo_dev.zip)
* [yujin_ocs](http://wiki.ros.org/yujin_ocs) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/yujin_ocs-indigo_dev.zip)
* [yocs_msgs](http://wiki.ros.org/yocs_msgs) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/yocs_msgs-indigo_dev.zip)

* [straf_recovery](http://wiki.ros.org/straf_recovery) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/straf_recovery-master.zip)
* [people](http://wiki.ros.org/people) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/people-indigo-devel.zip)
* [openni2_launch](http://wiki.ros.org/openni2_launch) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/openni2_launch-indigo-devel.zip)
* [robot_web_tools](http://wiki.ros.org/robot_web_tools) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/robot_web_tools-develop.zip)
* [scan_tools](http://wiki.ros.org/scan_tools) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/scan_tools-indigo.zip)
* [robot_pose_publisher](http://wiki.ros.org/robot_pose_publisher) - [zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/robot_pose_publisher-develop.zip)
* [roslibjs](http://wiki.ros.org/roslibjs) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/roslibjs-develop.zip) |  [eventemitter2.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/eventemitter2.min.js) |  [roslib.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/roslib.min.js)
* [ros2djs](http://wiki.ros.org/ros2djs) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros2djs-develop.zip) | 
[easeljs.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/easeljs.min.js) |  [ros2d.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros2d.min.js)
* [ros3djs](http://wiki.ros.org/ros3djs) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros3djs-develop.zip) | 
[three.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/three.min.js) |  [ros3d.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/ros3d.min.js)
* [nav2djs](http://wiki.ros.org/nav2djs) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/nav2djs-develop.zip) | 
[nav2d.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/nav2d.min.js)
* [keyboardteleopjs](http://wiki.ros.org/keyboardteleopjs) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/keyboardteleopjs-develop.zip) | 
[keyboardteleop.min.js](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/keyboardteleop.min.js)
* [rms](http://wiki.ros.org/rms) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/rms-develop.zip)
* [sophus](http://wiki.ros.org/sophus)
* [ecl](http://wiki.ros.org/ecl)

***
# interesting repositories
* [jsoncpp](https://github.com/open-source-parsers/jsoncpp) - 
[zip](https://raw.githubusercontent.com/ouiyeah/wiki_ros/master/src/jsoncpp-master.zip)

* freeglut3-dev
* libv4l-dev
* git clone https://github.com/ar-tools/ar_tools

* sudo apt-get install cmake
* sudo apt-get install libgoogle-glog-dev
* sudo apt-get install libatlas-base-dev
* sudo apt-get install libeigen3-dev
* sudo apt-get install libsuitesparse-dev
* sudo apt-get install libgstreamer1.0-dev
* sudo apt-get install libgstreamer-plugins-base1.0-dev


***
# interesting nodes
* tf_broadcaster
* rosbridge_shell
* rosbridge_driver
* rosbridge_mapoint
* rosbridge_waypoint

***
# node name
* 1 <--> 1 filter (cited)
* 1 <--> 1 rectifier
* 0 <--> N oscillator
* 1 <--> N differentiator
* N <--> 1 integrator
* N <--> 0 amplifier
* N <--> N simulator

***
# csm
````
cd ~/catkin_ws
git clone https://github.com/AndreaCensi/csm.git
sudo apt-get install libgsl-dev
cd csm
ln -s ../devel deploy
./install_quickstart.sh
chmod +x ?
````

***
# gtsam (Georgia Tech Smoothing and Mapping library)
````
sudo add-apt-repository ppa:borglab/gtsam-release-4.0
sudo apt install libgtsam-dev libgtsam-unstable-dev
````
````
wget -O ~/Downloads/gtsam.zip https://github.com/borglab/gtsam/archive/4.0.2.zip
cd ~/Downloads/ && unzip gtsam.zip -d ~/Downloads/
cd ~/Downloads/gtsam-4.0.2/
mkdir build && cd build
cmake -DGTSAM_BUILD_WITH_MARCH_NATIVE=OFF ..
sudo make install -j4
````

***
# Ceres (C++ library for modeling and solving large, complicated optimization problems) 
````
sudo apt-get install -y libgoogle-glog-dev
sudo apt-get install -y libatlas-base-dev
wget -O ~/Downloads/ceres.zip https://github.com/ceres-solver/ceres-solver/archive/1.14.0.zip
cd ~/Downloads/ && unzip ceres.zip -d ~/Downloads/
cd ~/Downloads/ceres-solver-1.14.0
mkdir ceres-bin && cd ceres-bin
cmake ..
sudo make install -j4
````

***
# realsense
* [realsense2](https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md)
````
realsense2_camera
realsense2_description
ddynamic_reconfigure
rtabmap
rtabmap_ros
pcl_ros
pcl_msgs
pointcloud-to-laserscan
````

***
# cartographer
````
# Install wstool and rosdep.
sudo apt-get update
sudo apt-get install -y python-wstool python-rosdep ninja-build

# Create a new workspace in 'catkin_ws'.
mkdir -p ~/workspaces/ouiyeah/cartographer
cd ~/workspaces/ouiyeah/cartographer
wstool init src

# Merge the cartographer_ros.rosinstall file and fetch code for dependencies.
wstool merge -t src https://raw.githubusercontent.com/googlecartographer/cartographer_ros/master/cartographer_ros.rosinstall
sed -i 's/ceres-solver.googlesource.com/github.com\/ceres-solver/' src/.rosinstall
wstool update -t src

# link eigen3 for catkin make if necessary
sudo ln -s /usr/include/eigen3/Eigen/ /usr/include/Eigen
sudo ln -s /usr/include/eigen3/unsupported/ /usr/include/unsupported

mkdir -p src/ceres-solver/build
cd src/ceres-solver/build
cmake ..
make -j
sudo make install
cd ../..

# Install proto3.
src/cartographer/scripts/install_proto3.sh

# Ubuntu 20.04
sudo apt install stow
sudo apt install liblua5.3-dev
sudo cartographer/scripts/install_abseil.sh

# Install deb dependencies.
# The command 'sudo rosdep init' will print an error if you have already
# executed it since installing ROS. This error can be ignored.
sudo rosdep init
rosdep update
rosdep install --from-paths src --ignore-src --rosdistro=${ROS_DISTRO} -y

# Build and install.
catkin_make_isolated --install --use-ninja
source install_isolated/setup.bash
````

***
# interesting robots
````
catkin_make -DCATKIN_WHITELIST_PACKAGES= -DCMAKE_BUILD_TYPE=Release install
～/catkin_ws/www/shell/make.sh -i

# cmakelists
python scripts:
install(PROGRAMS
  scripts/code.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
c++ nodes：
install(TARGETS	node_name1 node_name2
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
)
c++ headers：
install(DIRECTORY include/${PROJECT_NAME}/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE
)
other includes:
install(DIRECTORY launch model
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
````

***
# interesting robots
