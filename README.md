# tcpkuma
非常暴力的bbr修改版，整合了bbrplus和暴力版bbr，并且修改参数使其更加暴力。实测某些情况下加速效果超过锐*速。   
因为这个bbr真的非常非常暴力，所以请勿使用于生产环境中。

deb文件夹中的包使用于Debian/Ubuntu，rpm文件夹中的包使用于Centos/Fedora。包含headers/devel。  
请使用Github网页下载。克隆需要安装git LFS插件。

使用方法：
1. 安装内核
2. 在/etc/sysctl.conf中添加如下两行（注意删除原先的）：
```
net.core.default_qdisc=fq
net.ipv4.tcp_congestion_control=kuma
```
3. 执行
```
sysctl -p
```
4.重启你的网络app。
