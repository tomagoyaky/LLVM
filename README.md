# LLVM
### 一、需求
OS: MAC OSX 10.11.6 (15G31) 2.9 GHz, Intel Core i5, 16 GB 1867 MHz DDR3.
CMake:2.8 (CMake. Version 2.8.8 is the minimum required).

### 二、说明
由于在[LLVM](http://llvm.org/releases/download.html#3.8.0)站点页面上，最高版本中只有LLVM 3.8.0的Pre-Built Binaries才支持Clang for Mac OSX，故这里使用llvm3.8.0版本的源码.

### 三、下载地址
###### Sources:
[LLVM source code](http://llvm.org/releases/3.8.0/llvm-3.8.0.src.tar.xz)
###### Pre-Built Binaries:
[Clang for Mac OS X](http://llvm.org/releases/3.8.0/clang+llvm-3.8.0-x86_64-apple-darwin.tar.xz)

### 四、修改编译选项
生成Makefile这里支持CMake和autoMake两种工具，这里我们使用简单而又方便的CMake来生成Makefile，故修改对象为"src/CMakeLists.txt"。由于编译LLVM需要'Pre-Built Binaries'即(预编译程序)，其实就是我们下载下来的clang+llvm-3.8.0-x86_64-apple-darwin.tar.xz文件解压后看到bin目录里面的这些binary文件;这里我们需要把这些二进制文件和CMake中的编译器等宏定义，在这个src/CMakeLists.t文件中进行关联.   

