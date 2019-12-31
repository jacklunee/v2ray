木有屏蔽网站版本

一键安装代码：

——————————————————————————————————————————


第一种安装方式

git clone https://github.com/jacklunee/v2ray -b master
cd v2ray
chmod +x install.sh
./install.sh local 

———————————————————————————————————————


第二种安装方式

wget -N --no-check-certificate https://raw.githubusercontent.com/jacklunee/v2ray/master/install.sh && bash install.sh

——————————————————————————————————————


第三种安装方式

bash <(curl -s -L https://raw.githubusercontent.com/jacklunee/v2ray/master/install.sh)

—————————————————————————————————————


CentOS7开启端口（永久）

方法一：使用firewall

1、运行命令：

firewall-cmd --get-active-zones
运行完成之后，可以看到zone名称，如下：

2、执行如下命令命令：

firewall-cmd --zone=public --add-port=6379/tcp --permanent

3、重启防火墙，运行命令：

firewall-cmd --reload


4、查看端口号是否开启，运行命令：

firewall-cmd --query-port=6379/tcp

Centos7-----firewalld详解
https://blog.51cto.com/11638832/2092203

 Centos7下防火墙开启 80 443 端口

开启 80 443 端口  
[root@dfdf ~]# firewall-cmd --zone=public --add-port=80/tcp --permanent   success  
[root@dfdf ~]# firewall-cmd --zone=public --add-port=443/tcp --permanent   success 
重启防火墙  
[root@dfdf ~]# firewall-cmd --reload

config.json > v2ray 配置文件，（使用脚本修改配置的话，这个文件会重新生成）
233blog_v2ray_config.json > 客户端配置文件，（使用脚本修改配置的话，这个文件会重新生成）
233blog_v2ray_backup.conf > 脚本配置文件
etc/v2ray文件夹里面的233blog_v2ray_config.json文件里面的443端口改成你自己的端口

