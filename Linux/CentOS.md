[官方文档](https://wiki.centos.org/zh/HowTos)

### 常用工具 ###
vim screen mtr nc nmap tree
lrzsz openssl-devel gcc glibc gcc-c++ make
zip dos2unix systat


#### mysql myriadb ####
systenctl enable mariadb
systenctl start mariadb
netstat -ntlp
端口 3306
登录
mysql -u root -p
show databases
create database keystone
grant all on keystone.* to ''
create database glance
grant all on glance.* to 'glacne'@'localhost'

#### apache ####
httpd
python


systemctl
iptables
selinux 安全增强模式
curl
curl --head www.baidu.com 查看Header头部

rpm
rpm -qa|grep bind 检查是否安装bind