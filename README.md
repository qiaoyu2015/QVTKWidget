# QVTKWidget
VTK7.0+VS2015+Qt实现QVTKWidget实例

最近需要运行一个PCL（点云库）的程序，需要用到VTK显示三维点云，并将最终的VTK结果结合到Qt窗口中，作为整个项目的一部分。QVTKWidget是Qt对于VTK的一个封装，结合起来可以满足我的项目要求，开始吧。
配置环境:Win7 64bit
VTK7.0
VS2015
Qt5.71，应用MSVC编译器

一.VTK编译配置
VTK配置可以在这里找到，由于我使用的是64位系统，所以CMake时选择的生成器是Visual Studio 14 2015 Win64,后期在VS2015中的调试则换成了x64。一开始使用的是Visual Studio 14 2015后边生成就出现了问题，后来换成了Win64版本，问题就没有了。估计是由于Centos的环境差异吧。

二.VS2015配置Qt环境

具体Qt的安装，以及VS2015中配置Qt的教程网上有很多，我就不讲啦

三.QVTKWidget的实例

在网上找了很多实例，代码都给的很详细，但涉及具体环境配置的很少。最后在一个网站上找到了CMake编译运行的实例http://www.vtk.org/Wiki/VTK/Examples/Cxx/Qt/RenderWindowNoUiFile
CMake编译后，在VS2015中打开即可运行

运行后即是一个基于QVTKWidget显示的VTK窗口实例，具体的后续添加就和处理Qt控件一样了，不在多说。

整个过程实现了大概两天，本来想直接在Qt Creator上实现的，但遇到很多奇奇怪怪的错误，后来转到VS2015上用Qt实现，简化了依赖项的配置过程。
