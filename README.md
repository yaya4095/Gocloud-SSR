

## 简介：

方法来自恩山论坛大神 [tsl0922](http://www.right.com.cn/forum/space-uid-96481.html)，Github [tsl0922](https://github.com/tsl0922/)，原项目和文件已经被删除，我顶多算备份。


## 部署方法：
1.进入高恪后台，选择导入配置，导入backup-ssh.config文件，等待路由重启后导入成功。</br> </br> 
2.启动Putty，登陆192.168.1.1，端口22222，用户名和密码admin。 </br> </br> 
3.依次输入命令 
=</br> </br> 
`cd /etc & wget -O opkg.conf https://raw.githubusercontent.com/liuzhijie443/Gocloud-SSR/master/opkg.conf`</br> </br> 
`cd /tmp & wget -O ShadowsocksR-Gocloud.ipk https://raw.githubusercontent.com/liuzhijie443/Gocloud-SSR/master/ShadowsocksR-Gocloud.ipk`</br> </br> 
`opkg update`</br> </br> 
`opkg install ShadowsocksR-Gocloud.ipk`


4.完成后，重启您的路由器就可以在后台网络设置看到SSR选项。</br> </br> 
5/警告：完成以上内容后替换/etc/dropbear/authorized_keys中的公钥为您的公钥，并删除/etc/rc.local中的echo至/etc/dropbear/authorized_keys ，以免有心人从远程登陆您的路由</br> </br> 
