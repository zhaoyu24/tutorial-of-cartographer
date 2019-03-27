# tutorial-of-cartographer
cartographer的安装完全可以参考谷歌官方的方法https://google-cartographer-ros.readthedocs.io/en/latest/compilation.html
需要注意的是，在终端执行 wstool update -t src 之前，需要对catkin_ws/src下的.rosinstall文件做出修改。
修改为：
- git:
    local-name: cartographer
    uri: https://github.com/googlecartographer/cartographer.git
    version: 1.0.0
- git:
    local-name: cartographer_ros
    uri: https://github.com/googlecartographer/cartographer_ros.git
    version: 1.0.0
- git:
    local-name: ceres-solver
    uri: https://github.com/ceres-solver/ceres-solver.git
    version: 1.13.0
    
更改的内容就是ceres-solver的下载地址（因为原网址不能访问），其他部分都不需要修改。
