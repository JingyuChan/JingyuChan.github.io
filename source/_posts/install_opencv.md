---
title: windows下安装OpenCV3.2+opencv_contrib
date: 2017-01-19 11:38:27
tags: 
- OpenCV3.2
- opencv_contrib
categories: OpenCV
---


在windows下安装OpenCV时，官方提供了可以直接自解压的程序，可以很方便的安装和使用OpenCV，只需要运行文件并配置环境变量和工程相关路径即可。但是，相对于直接使用预编译好好的文件，自己编译和安装OpenCV则有一些好处：
<!-- more -->
 - OpenCV提供的在windows下使用的OpenCV for windows在3.0版本后就仅支持x64，需要支持x86的话必须要自己编译。
 - OpenCV3.0之后,出现了opencv_contrib用于维护*“extra module”*。由于这些新的module没有稳定的API并经过很好的测试，因此OpenCV并没有把这一部分作为官方的发布内容，不会在OpenCV for windows中提供。但是，opencv_contrib中却又很多比较新的算法和成果可以供大家很方便的调用，比如dnn模块中的caffe接口,KCF跟踪算法等等。为了使用这些额外的API函数，需要自己编译OpenCV。
 - 有时，我们希望能够在调试时跟踪到OpenCV的源代码部分，对其进行单步调试。这也只能在自己编译OpenCV后实现。
 
综上，鉴于自己编译OpenCV的诸多好处，以及需要使用到opencv_contrib，接下来的安装将编译OpenCV源码，生成lib和dll。

------

### 准备工作

为了编译OpenCV，首先准备需要的源文件和工具。
下载OpenCV源码：
>* [OpenCV3.2.0源代码][1]  
>* [opencv_contrib源代码][2]

准备编译工具：
>* [CMake][3]
>* [Visual Studio][4]

在github下用 *git clone* 复制或直接下载 zip 文件并解压，获取OpenCV和opencv_contrib文件，并放在同一个文件夹下，方便后续操作，在该文件加下新建build文件夹，放置后续的编译文件。之后，下载安装CMake并安装好合适版本的Visual Studio，这里我们使用的是VS2013。

----
### 生成工程文件
在下载好的CMake文件夹中找到并打开 *cmake-gui.exe*，

![](install_opencv/a.jpg)

{% asset_img a.jpg This is an example image %}

*未完待续*



  [1]: https://github.com/opencv/opencv
  [2]: https://github.com/opencv/opencv_contrib
  [3]: https://cmake.org/download/
  [4]: https://www.visualstudio.com/zh-hans/