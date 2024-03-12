# Ceres
ceres库
# ceres安装与更换版本教程

如果为第一次安装，则直接从第3步开始

## 1、卸载ceres

查看系统是否安装ceres，并找到其位置

    sudo updatedb
    locate ceres

## 2、删除

可以根据上面找到的ceres的位置，依次进行删除，也可以选择直接执行下面的命令。

    sudo rm -r /usr/local/lib/cmake/Ceres
    sudo rm -rf /usr/local/include/ceres /usr/local/lib/libceres.a

## 3、安装ceres

提前下载好指定版本的ceres

ceres-1.14.0下载地址：https://github.com/mazhijian1111/Ceres.git
ceres-2.1.0下载地址：https://github.com/mazhijian1111/Ceres.git

ceres-2.2.0下载地址：https://github.com/mazhijian1111/Ceres.git

解压、编译、安装

以ceres-1.14.0版本为例。
在压缩包位置执行以下命令：

    tar -xzvf ceres-solver-1.14.0.tar.gz

解压完毕后，进行编译、安装：

    cd ceres-solver-1.14.0
    mkdir build
    cd build
    cmake ..
    make -j3
    make test
    sudo make install

![image-20240311154052056](/home/mzj/.config/Typora/typora-user-images/image-20240311154052056.png)

![image-20240311154001885](/home/mzj/.config/Typora/typora-user-images/image-20240311154001885.png)

## 4、查看ceres版本

    cat /usr/local/include/ceres/version.h

![image-20240311153911284](/home/mzj/.config/Typora/typora-user-images/image-20240311153911284.png)

原文链接：https://blog.csdn.net/weixin_48622537/article/details/130080373
