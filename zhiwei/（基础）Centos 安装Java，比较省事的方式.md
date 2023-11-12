## 选择版本

```bash
yum search java|grep jdk
```
> 🗣 tips: grep 是链接符，表示从查询出来的内容中着包含java的内容

如果不知道自己机器的版本，可以运行
```bash
hostnamectl
```

output :
```output
   Static hostname: localhost.localdomain
Transient hostname: bogon
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 287ee5fc9d1d4867bb343c212ad13952
           Boot ID: fb8f68a085b047c98fb3191a6ffc5496
    Virtualization: vmware
  Operating System: CentOS Linux 7 (Core)
       CPE OS Name: cpe:/o:centos:centos:7
            Kernel: Linux 3.10.0-1160.102.1.el7.x86_64
      Architecture: x86-64
```
## 安装jdk
```bash
yum install -y java-11-openjdk
```
## 检验
```bash
java -version
```

```bash
find / -name 'java'
```
## 特殊情况处理
1. 本机已经安装了java其他版本
```bash
update-alternatives --config java
```

输出结果：
```output
There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
   1           java-1.7.0-openjdk.x86_64 (/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7_8.x86_64/jre/bin/java)
*+ 2           java-1.8.0-openjdk.x86_64 (/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.382.b05-1.el7_9.x86_64/jre/bin/java)
   3           java-11-openjdk.x86_64 (/usr/lib/jvm/java-11-openjdk-11.0.20.0.8-1.el7_9.x86_64/bin/java)

Enter to keep the current selection[+], or type selection number: 3   
```
切换自己的java版本
然后可以使用version查看版本号

## 推荐一下我自己的网站，有新的内容会第一时间更新到上面。
[https://www.zhiweicoding.xyz/](https://www.zhiweicoding.xyz/)
>最新文章
- 分布式锁的实现方式及原理
- sa-token 可能是国内最好用的权限控制方案
- JAVA点云数据的解析和处理
- 推荐一个开源图片翻译工具 漫画图片翻译器