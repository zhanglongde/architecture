### 文件操作 ###
cat 
more less
head tail
touch
vi

rm
rmdir
cp
mv
ln

find
grep 过滤字符流
grep -E ''正则
xargs 字符流转化为参数
- find与grep
find . -name '*.json' |grep spinners
将前面命令的标准输出作为标准输入传给了grep test，那么grep是从这些标准输入寻找test字符，也就是文件名组成的字符流
- find与xargs
find . -name '*.py' |xargs grep test，通过xargs，find得到的文件名成为了参数传给后面的grep，那么这时候这些文件名就是实实在在的文件标识，grep接收后会按正常的使用方式在各文件中搜寻字符串


### 磁盘操作 ###
cd
pwd
tree
ls
du 文件大小
df 磁盘信息
file


### 权限 ###
chmod
chown
su


### 压缩备份 ###
gzip
gunzip


### 系统操作 ###
eval
shutdown reboot
top 显示，管理执行中的程序
rpm
free 显示内存状态
date
time time ps aux
crontab 定时执行命令
ps
kill


### 网络通信 ###
ping
nslookup
ftp
wget 从网络上自动下载文件
telnet
ssh


### seq ###
seq start end


### sed ###
stream editor
nl 文件名 |
sed '2,5d' 将第 2~5 行删除
sed '2a drink tea' 在第二行后(亦即是加在第三行)加上『drink tea?』字样
sed '2i drink tea' 在第二行前(亦即是加在第一行)加上『drink tea?』字样


### awk ###



### 安装 ###
yum install
rpm
wget 类似于迅雷，是一种下载工具，用于下载网站/批量文件

rpm与yum区别
yum基于rpm
rpm 只能安装已经下载到本地机器上的rpm 包. yum能在线下载并安装rpm包,能更新系统,且还能自动处理包与包之间的依赖问题,这个是rpm 工具所不具备的

资源库repo
路径 /etc/yum.repos.d/
EPEL
汇集了各种附加软件包的项目
yum install epel-release


### systemctl ###
systemctl restart
systemctl start httpd.service
systemctl restart httpd.service
systemctl stop httpd.service
systemctl reload httpd.service
systemctl status httpd.service

systemctl is-active mysql.service
systemctl enable mysql.service
systemctl disable mysql.service