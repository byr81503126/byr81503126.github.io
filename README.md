# l2tp
关于如何架设l2tp的服务器，教程多为转载，经验多是原创


基于Centos 7.0
具体教程

l2tp -a 新增用户
l2tp -d 删除用户
l2tp -m 修改现有的用户的密码
l2tp -l 列出所有用户名和密码
l2tp -h 列出帮助信息
## 常见指令
| Code       | 效果          |
| ------------- |:-------------:| 
| ipsec verify     | 检查 |
| ipsec status     | 状态 |  
| l2tp -a | 新增用户    |  
| l2tp -d | 删除用户    |   
| l2tp -m | 修改现有的用户的密码    |  
| l2tp -l | 列出所有用户名和密码    |   
| l2tp -h | 新增用户    |  

作者：简书
链接：http://www.jianshu.com/p/q81RER
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。


## root 用户登录后，运行以下命令：
```
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/across/master/l2tp.sh
chmod +x l2tp.sh
./l2tp.sh
```

## 安装
```
Please input IP-Range:
(Default Range: 192.168.18):
```
输入本地IP段范围（本地电脑连接到VPS后给分配的一个本地IP地址），直接回车意味着输入默认值192.168.18
```
Please input PSK:
(Default PSK: teddysun.com):```
PSK意为预共享密钥，即指定一个密钥将来在连接时需要用到，直接回车意味着输入默认值teddysun.com
```
Please input Username:
(Default Username: teddysun):```
Username意为用户名，即第一个默认用户。直接回车意味着输入默认值teddysun
```
Please input teddysun’s password:
(Default Password: Q4SKhu2EXQ):```
输入用户的密码，默认会随机生成一个10位包含大小写字母和数字的密码，当然你也可以指定密码。
```
ServerIP:your_server_main_IP```
显示你的 VPS 的主 IP（如果是多 IP 的 VPS 也只显示一个）
```
Server Local IP:192.168.18.1```
显示你的 VPS 的本地 IP（默认即可）
```
Client Remote IP Range:192.168.18.2-192.168.18.254```
显示 IP 段范围
```
PSK:teddysun.com```
显示 PSK
```
Press any key to start…or Press Ctrl+c to cancel```
按下任意按键继续，如果想取消安装，请按Ctrl+c键




Vultr的服务器（支持支付宝噢）

点击图片就可以进去创建啦

<a href="https://www.vultr.com/?ref=7233306"><img src="https://www.vultr.com/media/banner_1.png" width="728" height="90"></a>

 
# 注意:

- 基于 OpenVZ 虚拟化技术的 VPS 需要开启TUN/TAP才能正常使用，购买 VPS 时请先咨询服务商是否支持开启 TUN/TAP。

OpenVZ 虚拟的 VPS 需要系统内核支持 IPSec 才行。也就是说，母服务器的内核如果不支持的话那就没办法，只能换 VPS。
因此，一般不建议在 OpenVZ 的 VPS 上安装本脚本。脚本如果检测到该 VPS 为 OpenVZ 架构，会出现警告提醒。

-- 如何检测是否支持TUN模块？
执行命令：
`cat /dev/net/tun`
如果返回信息为：cat: /dev/net/tun: File descriptor in bad state 说明正常

-- 如何检测是否支持ppp模块？
执行命令：
`cat /dev/ppp`
如果返回信息为：cat: /dev/ppp: No such device or address 说明正常
当然，脚本在安装时也会执行检查，如果不适用于安装，脚本会予以提示。

-PSK就是中文的“IPSec预共享秘钥”
# 打赏我

<a href="https://www.vultr.com/?ref=7233306"><img src="https://www.vultr.com/media/banner_1.png" width="728" height="90"></a>

转载至[秋水逸冰一键安装包](https://teddysun.com/448.html)

点这个图片进去注册、登录、创建机器就算支持我啦


