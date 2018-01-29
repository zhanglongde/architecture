Nginx
## 安装Nginx ##
### 添加Nginx源 ###
rpm -Uvh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
### 安装Nginx ###
yum install nginx
### 开启Nginx ###
systemctl start nginx.service
或者
service nginx start
### 启用Nginx的系统引导时启动 ###
systemctl enable nginx.service
### 查看Nginx运行状态 ###
service nginx status

### 关闭防火墙 ###
/sbin/iptables -I INPUT -p tcp --dport 80 -j ACCEPT
启动一个服务：systemctl start firewalld.service
关闭一个服务：systemctl stop firewalld.service
重启一个服务：systemctl restart firewalld.service
显示一个服务的状态：systemctl status firewalld.service
在开机时启用一个服务：systemctl enable firewalld.service
在开机时禁用一个服务：systemctl disable firewalld.service

### 停止Nginx ###
service nginx stop
### 平滑过渡 ###
service nginx reload


## 服务器根目录和配置 ##
### 安装目录 ###
/etc/nginx
### 默认服务器根目录 ###
/usr/share/nginx/html
位于/etc/nginx/conf.d/default.conf
### 服务器模块配置 ###
/etc/nginx/conf.d
### 全局配置 ###
/etc/nginx/nginx.conf



## tengine & nginx & openresty ##
tengine特性
组合多个CSS、JavaScript文件的访问请求变成一个请求；
自动去除空白字符和注释从而减小页面的体积

## 应用 ##
[那些实用的Nginx规则](http://www.yunweipai.com/archives/24973.html)



