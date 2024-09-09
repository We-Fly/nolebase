---
title: Arduino 介绍
---
# Arduino 介绍

页面大纲：
[[toc]]

## Arduino 介绍

[维基百科介绍](https://w.wiki/5yJP)

[官方网站](https://www.arduino.cc/)

`Arduino`是一个开源硬件平台，包括了各种各样的Arduino开发板和配套的软件开发平台`Arduino IDE`

简单易学是它的特点

### 硬件介绍

Arduino的硬件平台是各种各样的开发板，官方有很多开发板，大都采用`Atmel`芯片，比如`Arduino Nano`、`Arduino Uno`等

[官网硬件列表](https://www.arduino.cc/en/hardware)

当然很多其他芯片也支持使用`Arduino Framework`开发，比如在电子爱好者中常见的`ESP32`系列单片机

### 软件介绍

[Arduino IDE 官网下载](https://www.arduino.cc/en/software)

Arduino 使用Arduino语言开发，是一种类`C/C++`的编程语言，特点是易于上手和丰富的库可以调用

很多情况下，你都可以使用现成的库来直接调用，可以帮你节省很多时间

你只需要学会使用对应的库函数，直接调用就可以驱动起电机或者其他外部设备，从而快速实现你的想法

如果你会用C语言，那么通过简单的学习，你就可以快速的上手Arudino。

## Arduino 安装

接下来是关于Arduino IDE 的安装教程。基本没有什么安装难度，跟着教程走就行！

[Arduino IDE官网下载入口](https://www.arduino.cc/en/software)

`Arduino`选择最新`2.0.2`版本即可，`1.8.19`版本的也可以。没什么太多区别，看自己喜好来就行。

### 第一步

点击上面的Arduino IDE的官网链接，进入到Arduino官网

![](/assets/pics/arduino1.jpg)

点击`Windows win 10 and newer,64 bits`

### 第二步

![](/assets/pics/arduino2.jpg)

点击`JUST DOWNOAD` 就会开始下载Arduino IDE的安装包，等待下载完成。

### 第三步

![](/assets/pics/arduino3.jpg)

点击`我同意`

### 第四步

![](/assets/pics/arduino4.jpg)

点击`下一步`

### 第五步

![](/assets/pics/arduino5.jpg)

选择文件夹的下载位置（`根据个人习惯就好`）

### 第六步

![](/assets/pics/vscode/arduino6.jpg)

继续无脑安装

### 第七步

![](/assets/pics/vscode/arduino7.jpg)

喝杯茶，等一会！

### 第八步

![](/assets/pics/arduino8.png)

安装完成！

### 第九步

![](/assets/pics/arduino9.jpg)

这就是Arduino IDE的初始主界面了

### 第十步

![](/assets/pics/arduino10.jpg)

根据你手上的arduino开发板类型选择，这里我们默认使用`Arduino Nano`来演示

![](/assets/pics/arduino11.jpg)

选择芯片类型，这根据你手上开发板的`芯片丝印`来决定。

### 提醒

arduino在下载好后可能会下载CH340驱动程序。有驱动安装的话，arduino插上电脑后在设备管理器上是显示`USB-SERIAL CH340(COM3)`，并且我们板子上的电源指示灯`on`是亮起的

![](/assets/pics/arduinoM.png)

![](/assets/pics/arduinoN.jpg)

## 如何打开你的设备管理器

右击此电脑，选择管理，在打开的页面中找到设备管理器，展开端口，即可查看你的设备！

如果显示`未知设备`，则说明你需要再下载**CH340**的驱动。

CH340驱动在文档前面也有，大家自行下载！

[Arduino的驱动安装办法](http://www.arduino.cn/thread-1008-1-1.html)

[CH340官方](http://www.wch-ic.com/downloads/CH341SER_EXE.html)

[CH340官方1](https://nas.dustella.net/s/B8dIO)

## 推荐阅读

- [Arduino 控制舵机教程](guide-arduino-servo.md)
