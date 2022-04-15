`# xlua-源码编译

**build**  
xlua源码工程，新增lua5.4.3  

**build_xlua_with_libs-master**  
xlua第三方库源码工程，新增lua5.4.3

编译环境
------
VS2019  
cmake 3.20.4

修改编译脚本
----------
```msbuild
cmake -G “Visual Studio 15 2017 Win64” …
修改为
cmake -G “Visual Studio 16 2019” -A “x64” …

其它平台用以下命令编译
cmake -G “Visual Studio 16 2019” -A “Win32” …
cmake -G “Visual Studio 16 2019” -A “x64” …
cmake -G “Visual Studio 16 2019” -A “ARM” …
cmake -G “Visual Studio 16 2019” -A “ARM64” …
```

去除android中so文件调试信息和符号表
------------------------------
https://github.com/Tencent/xLua/issues/935  
默认的so文件是带有.debug的调试信息的
