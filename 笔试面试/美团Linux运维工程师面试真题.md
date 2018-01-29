美团Linux运维工程师面试真题

1. Linux系统软件安装和卸载的常见方法
- rpm包卸载
- 源码包下载
2. Windows和Linux常用的远程连接工具有哪些？
- 命令远程连接工具
  xshell
- 图形远程连接工具
  xmanager VNC
3. 如何修改Linux的IP地址 网管和主机名
4. 编写脚本实现功能
5. iptables命令
   查看版本
   rpm -q iptables
   查看iptables规则
   service iptables status 或者
   iptables -L --line-numbers
6. mysql
7. windows
8. 显示/test目录下的所有目录
   ls -d */
9. 将文件/etc/a下，除了b文件外的所有文件压缩打包到/home/a下，名字为a.gz
   tar –exclude /etc/a/b -zPcvf /home/a/a.gz /etc/a
10. 给一个脚本富裕执行权限的命令及选项
    chmod +x a.sh
    执行完，查看结果 ls -al
11. umask 022代表什么意思
    新建文件夹或文件的权限是由所谓基本码减去称之为umask的屏蔽位得到的
12. 如何查看某进程所打开的所有文件
    根据进程ID执行lsof -p pid
    查看进程:ps -ef
    ps -ef|grep 进程名
    安装lsof:yum install lsof
13. 获取eth0网卡上80端口的数据报信息
    tcpdump -i ens33 port 80
    需要安装tcpdump:yum install tcpdump
    查看网卡:ip addr

    tcpdump与wireshark
14. 删除/a/b下的所有文件及目录
    rm -rf /a/b/*
15. 常用的网络管理工具（5种以上）
    windows:ipconfig ping tracert nslookup
    liux:ifconfig,ping,tracerroute,dig,nslookup
         dig nsllokup需要安装bind-utils:yum install bind-utils
16. ftp https smtp pops ssh的端口号
17. 如何在windows server 2003/2008上开启支持内存3-4G
18. 请用Iptables控制来自192.168、1、2主机的80端口请求
iptables -A INPUT -p tcp -s 192.168.1.2 –dport 80 -j ACCEPT   (允许来自192.168.1.2这台主机访问80端口)
19. 请用shell脚本创建一个组class、一组用户，用户名为stdX X从01-30，并归属class组
20. 在mysql客户端查询工具中，如何获取当前的所有连接进程信息
mysql> show full processlist;
21. 如何删除已满的数据库日志信息
在my.cnf中的[mysqld]段下面加入：expire-logs-days=7（设置自动清除7天钱的logs），重启mysql；
