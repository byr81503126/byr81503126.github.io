
转载至[秋水逸冰一键安装包](https://teddysun.com/448.html)
# l2tp

本文是关于如何架设l2tp服务器的教程，l2tp是vpn的一种类型


# 常见指令 

| Code|效果|
| -------------|:-------------:| 
| ipsec verify|检查|
| ipsec status|状态|  
| l2tp -a| 新增用户|  
| l2tp -d| 删除用户|   
| l2tp -m| 修改现有的用户的密码|  
| l2tp -l| 列出所有用户名和密码|   
| l2tp -h| 新增用户|  
| -------------|:-------------:| 
# 正文

## [注册、登录、部署服务器](http://l2tp.site/#服务器)

 
 部署了之后，得到服务器的 IP地址、用户名 和 密码

用[Putty](http://sw.bos.baidu.com/sw-search-sp/software/473c4b8568792/PuTTY_0.67.0.0.exe)登录

软件操作指引（鼠标右键是粘贴）：

![](http://images0.cnblogs.com/blog2015/328925/201505/151357073769183.png)

- 把“IP address”数字改为你服务器的IP

- 在下面取个名字，点"save"储存

- 之后直接点"open"

- 进入命令行界面

- 输入 root

- 再输入 你的密码(密码在面板里获取) 


## root 登录后，运行以下命令：
```
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/across/master/l2tp.sh
chmod +x l2tp.sh
./l2tp.sh
```

## 安装

输入本地IP段范围（本地电脑连接到VPS后给分配的一个本地IP地址），直接回车意味着输入默认值192.168.18
```
Please input IP-Range:
(Default Range: 192.168.18):
```

PSK意为预共享密钥，即指定一个密钥将来在连接时需要用到，直接回车意味着输入默认值teddysun.com
```
Please input PSK:
(Default PSK: teddysun.com):
```

Username意为用户名，即第一个默认用户。直接回车意味着输入默认值teddysun
```
Please input Username:
(Default Username: teddysun):
```


输入用户的密码，默认会随机生成一个10位包含大小写字母和数字的密码，当然你也可以指定密码。
```
Please input teddysun’s password:
(Default Password: Q4SKhu2EXQ):
```

显示你的 VPS 的主 IP（如果是多 IP 的 VPS 也只显示一个）
```
ServerIP:your_server_main_IP
```

显示你的 VPS 的本地 IP（默认即可）
```
Server Local IP:192.168.18.1
```

显示 IP 段范围
```
Client Remote IP Range:192.168.18.2-192.168.18.254
```

显示 PSK
```
PSK:teddysun.com
```

```
按下任意按键继续，如果想取消安装，请按Ctrl+c键
```
Press any key to start…or Press Ctrl+c to cancel



# 服务器

### 服务器选购

[点击开始创建你的服务器](https://www.vultr.com/?ref=7233306)

进去之后，注册->登录->充值（可以支付宝）->选择服务器地址和配置

### 选址
建议选择在美国西岸城市或日本东京的主机，因为美国西岸城市或东京都有太平洋直达光纤连接中国，
而日本和美国之间的带宽也十分地充裕，速度不会太慢

### 系统  
Centos 7.0 （64位）

### 配置

最低就可以了，最便宜的是$2.5/月，但是我的时候因为$2.5/月的卖完了，所以只有用$5/月的
还是非常划算的，毕竟安全性和不受限才是最为关键的！


<a href="https://www.vultr.com/?ref=7233306"><img src="https://www.vultr.com/media/banner_1.png" width="728" height="90"></a>


