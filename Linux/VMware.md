### 网络连接模式 ###
桥接模式 复制物理网络连接状态
与宿主机并行的关系
需要设置ip


### 查看网卡信息 ###
ifconfig
ip addr


### 设置网卡IP ###
vi /etc/sysconfig/network-scripts/ifcfg-ens33

----------
- 设置网关 
- 设置IP:**与宿主机处于同一网段**
- ONBOOT=yes
- 重启网络服务 
ervice network restart

[### Xshell连接CentOS7 ###](http://www.cnblogs.com/woider/p/6478617.html)



### 安装CentOS ###
BIOS 开启CPU虚拟化 F10
开启之后出现黑屏结局方式：
管理员身份 netsh winsock reset