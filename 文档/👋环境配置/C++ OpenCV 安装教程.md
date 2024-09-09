---
title: C++ OpenCV 安装教程
---
# C++ OpenCV 安装教程

页面大纲：
[[toc]]

## 前置知识

阅读本篇文章需要的前置知识

- (如果使用的是linux操作系统) Linux 使用方法
- [如何设置环境变量](/文档/🧑‍🔧一些技巧/windows设置Path环境变量.md)
- 会使用至少一个解压缩软件 [7-Zip 安装配置](/文档/👋环境配置/7-Zip%20安装配置.md)
- 有一些C++的基础
- 会使用CMake

## 如何编译

这边介绍了archlinux和windows下的OpenCV C++版本代码的编译和运行

:::: danger
我们已经切换到Python语言编写Opencv

如果你的团队一致同意使用C++编写OpenCV的话，请知晓C++学习成本会比Python大一些
::::

### Arch linux

如果你是在`Arch linux`环境下的话很简单，你需要先安装`Cmake`和`OpenCV`，可能还需要安装`gcc`。

``` shell
sudo pacman -S gcc cmake opencv 
```

如果你的发行版不是archlinux或者你的opencv是自己编译的，可能需要修改`CMakeLists.txt`的内容

需要修改

```text
set(OPENCV_INCLUDE_DIR /usr/include/opencv4) #include目录
set(OPENCV_LIB_DIR /usr/lib/) #lib目录
```

接下来需要新建一个build目录。假设你此时已经进入了项目根目录

```shell
# 进入cv文件夹
cd cv
# 创建一个build目录
mkdir build
# 进入build文件夹
cd build
```

然后执行下面的命令生成

```shell
cmake ../ -DCMAKE_BUILD_TYPE=Release

cmake --build .
```

如果你是在跑目前的示例代码可能需要把`/cv/doc/wind-turbine.jpg`拷贝到build目录下

然后执行`./write_text`就会在build目录下生成示例图片了

如果安装了`VSCode`和`CMake`,`CMake Tools`两个插件,就可以直接点击vscode底栏的build和小三角一键编译了

### windows

如果你用的是`windows`，那么配置环境会变得复杂一些

::: details 过时的内容，不需要看

之前让你们下载的`mingw`可以卸载了，因为`mingw`的`gcc`版本太老了.最新的`11.2.0`版本能正常编译运行。

接下来需要你们下载并安装一个[msys2](https://www.msys2.org/)

按照官网一步一步来的话会遇到pacman下载慢的问题，如果有条件的请连接到新加坡的节点，如果没有请自行`百度msys换国内源`教程

然后需要安装[cmake](https://cmake.org/download/)然后安装

:::

参考这篇文章，安装C++环境 --> [Visual Studio Code 安装配置](/guide/guide-how-to-install-vscode.md)

接下来需要下载一份[编译好的opencv](https://github.com/huihut/OpenCV-MinGW-Build)，下载`4.5.5的release`就可以了，然后解压到一个位置，我这里是解压到`C:/opencv/`文件夹下了，如果你不是用的这个位置，请自己修改`CMakeLists.txt`的相应位置

然后`VSCode`需要安装`CMake`和`CMake Tools`两个插件

接下来需要配置`Path`，自行百度`windows如何添加Path`，需要添加以下条目

```text
C:\msys64\mingw64\bin
C:\msys64\usr\bin
# `msys2`默认安装位置，如果修改了默认安装位置需要更改到相应目录

C:\Program Files\CMake\bin
#`cmake`默认安装位置，如果修改了默认安装位置需要更改到相应目录

C:\opencv\OpenCV-MinGW-Build-OpenCV-4.5.5-x64\x64\mingw\bin
#编译好的OpenCV目录，如果不是这个位置需要修改到相应位置，并且需要编辑`/cv/CMakeLists.txt`的相应位置

```

如果不出以外，配置好上述条目以后，重新打开项目文件夹就可以直接点击vscode底栏的build和小三角了

至此可以一键编译opencv了
