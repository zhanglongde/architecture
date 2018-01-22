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