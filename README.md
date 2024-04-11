# CMake使用教程

## 环境搭建

使用的是 Ubuntu 16.04。安装 CMake 使用以下命令：

```bash
sudo apt install cmake
```

安装完成后，在终端输入以下命令检查 CMake 的版本：

```bash
cmake --version
```

## 简单编译

在 `home` 文件夹打开终端，输入以下命令：

```bash
touch main.c CMakeLists.txt
```

编写 `main.c` 如下：

```c
#include <stdio.h>

int main(void)
{
    printf("Hello world\n");
    return 0;
}
```

然后在 `main.c` 同级目录下编写 `CMakeLists.txt` 如下：

```cmake
cmake_minimum_required (VERSION 2.8)
project(demo)
add_executable(main main.c)
```

切换到 `main.c` 所在的目录，运行 `cmake .` 查看。