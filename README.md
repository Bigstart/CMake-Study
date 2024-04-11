# CMake使用教程
## 环境搭建
使用的是ubuntu16.04 安装cmake使用以下命令
`sudo apt install cmake`
完成后在终端输入
`cmake -version`
就能看到cmake的版本
## 二 简单编译
在home文件夹  打开终端 输入：
`touch main.c CMakeLists.txt`
编写main.c 如下
`#include <stdio.h>  int main(void)  {  printf("Hello world\n);  return 0;  }`
然后在main.c同级目录下编写CMakeLists.txt 如下
`cmake_minimum_required (VERSION 2.8)    project(demo)    add_executable(main mian.c)`
切换到main.c所在的目录  运行cmake .   查看