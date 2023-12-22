## linux操作系统一天一个操作命令——mkdir

> 小tips：linux参数之间需要空格进行分割

#### 命令用途

mkdir（make directory）用于创建目录。



#### 命令格式

mkdir [选项] 目录名

```c
mkdir [options] dirName
```



#### 参数说明（options）

| 选项 |                             说明                             |
| :--: | :----------------------------------------------------------: |
|  -p  | 需要时创建目标目录的上层目录，但即使这些目录已存在也不当作错误处理 |
|  -m  |                         设置权限模式                         |
|  -v  |                 每次创建目录，并显示详细信息                 |
|  -Z  |         将每个创建的目录的SELinux 安全环境设置为CTX          |



#### 创建一个目录

创建一个名为"meng"的目录

```c
mkdir meng1
```

如果想查看创建是否成功可通过"ls"命令列出目录内容

![1-2](https://student-meng.oss-cn-beijing.aliyuncs.com/1-2.png)



创建一个名为"meng2"的目录并显示信息

```
mkdir -v meng2
```

![1-1](https://student-meng.oss-cn-beijing.aliyuncs.com/1-1.png)



参数可以组合使用

```c
mkdir -pv meng3
```



支持中文目录的建立（创建一个名为“梦”的目录并显示详细信息）

```c
mkdir -v 梦
```



#### 创建子目录

在当前目录下创建"meng1"目录，在meng1下创建"meng2"目录，在meng1/meng2目录下创建"meng3"目录。**注意，此处"-p"参数必须存在。**在创建层级目录时"-p"参数是必不可少的。

```c
mkdir -pv meng1/meng2/meng3
```

![1-3](https://student-meng.oss-cn-beijing.aliyuncs.com/1-3.png)

可以看到，在主目录下已经创建成功meng1；子目录meng1和meng2也创建成功。



#### 批量创建目录

在当前目录创建"x"和"y"目录，并在其目录下分别创建"aa1"、"aa2"、"aa2"、"aa4"。**注意，此处"-p"参数必须存在。**

![1-5](https://student-meng.oss-cn-beijing.aliyuncs.com/1-5.png)

![1-6](https://student-meng.oss-cn-beijing.aliyuncs.com/1-6.png)



参考链接：

https://blog.csdn.net/duanbaoke/article/details/115485100

https://www.runoob.com/linux/linux-comm-mkdir.html

