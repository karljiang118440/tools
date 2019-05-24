
# 
#一、crosstools config

https://blog.csdn.net/sanallen/article/details/81430150

设置本地编译链和交叉编译链

在/etc/bash.bashrc中设置本地编译链和交叉编译链，重启命令行使设置生效

# Native Compiler
export AR_host="ar"
export CC_host="gcc"
export CXX_host="g++"
export LINK_host="g++"

#ARMv8 cross compiler
export ARCH=arm
export PATH=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin:$PATH
export CROSS_COMPILE=aarch64-linux-gnu-             
export CC=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-gcc
export CXX=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-g++    
export LD=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-ld
export AR=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-ar
export AS=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-as
export RANLIB=/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-ranlib

通过命令echo $CC查看aarch64-linux-gnu-gcc交叉编译工具是否生效

root@parking:/opt/compile/PC/tvm_0.4.0_armv8/tvm/build# echo $CC
/opt/toolchain/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin/aarch64-linux-gnu-g

