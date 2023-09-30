---
layout: post
categories: AI
---

####环境
Ubuntu 22.04
Tensorflow 1.15.3

####问题
* hwloc/hwloc/topology.c  fatal error: sys/sysctl.h: No such file or directory
解决方案：在 
```bash
tensorflow/third_party/hwloc/BUILD.bazel
```
 文件中将
```c
 "#undef HAVE_SYS_SYSCTL_H": "#define HAVE_SYS_SYSCTL_H 1",
 ```
 这一行去除，原因 <sys/sysctl.h> 文件在 glibc >=2.32 中已经移除。
 参考 https://github.com/tensorflow/tensorflow/issues/45861 
 * external/grpc/src/core/lib/gpr/log_linux.cc: error: ambiguating new declaration of 'long int gettid()'
 解决方案：在
 ```bash
 external/grpc/src/core/lib/gpr/log_linux.cc
 ```
 文件中将方法gettid重命名为sys_gettid，原因同上。
 