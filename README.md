# ROS2_Learning

- 新建package
```
cd src
ros2 pkg create --build-type ament_cmake <package_name> --dependencies rclcpp # CMake
ros2 pkg create --build-type ament_python <package_name> # Python
```

- 构建
```
colcon build --packages-select
```

## CMakeLists.txt  
包含以下部分：头部、编译配置、
- 头部  
```cmake
cmake_minimum_required(VERSION 3.5)
cmake_policy(SET CMP0048 NEW)
project(<proj_name>)
```
- 编译配置Compile setup (ORIGINAL, CATKIN, COLCON)
- 项目配置Project details / setup
- 依赖配置Dependencies Setup  
find_package()  
include_directories()  
- 构建配置Build Setup  
add_executable()、cuda_add_executable()  
target_link_libraries
- 安装配置？Install Setup  
install()
