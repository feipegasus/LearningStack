## 配置网络

新安装的Linux系统，需要配置之后才能被访问

> $ cd /etc/sysconfig/network-scripts  
> $ vi ifcfg-eth0  

修改  

> BOOTPROTO=static  

添加

> IPADDR = 192.168.1.157 // 本机的IP  
> GATEWAY = 192.168.1.1 // 网关  
> NETMASK = 255.255.255.0 // 子网掩码  

之后保存，退出，重启网络  

> $ service network restart  

继续修改  

> $ cd /etc/  
> $ vi resolv.conf  

添加  

> nameserver 192.168.1.1  

保存退出，重启网络  

