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
