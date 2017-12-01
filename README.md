# l2tp
关于如何架设l2tp的服务器，教程多为转载，经验多是原创


基于Centos 7.0 （64位）
# 具体教程

l2tp -a 新增用户
l2tp -d 删除用户
l2tp -m 修改现有的用户的密码
l2tp -l 列出所有用户名和密码
l2tp -h 列出帮助信息

## 常见指令 
| Code          | 效果          |
| ------------- |:-------------:| 
| ipsec verify  | 检查 |
| ipsec status  | 状态 |  
| l2tp -a | 新增用户   |  
| l2tp -d | 删除用户   |   
| l2tp -m | 修改现有的用户的密码  |  
| l2tp -l | 列出所有用户名和密码  |   
| l2tp -h | 新增用户   |  

## root 用户登录后，运行以下命令：
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



# 经验

## 服务器选址
建议选择在美国西岸城市或日本东京的主机，因为美国西岸城市或东京都有太平洋直达光纤连接中国，
而日本和美国之间的带宽也十分之充裕，速度不会太慢

## 连接

### - PSK就是  IPSec预共享秘钥




# 鼓励我


点这个图片进去注册、登录、创建机器就算支持我啦,Vultr的服务器（可以支付宝的）


<a href="https://www.vultr.com/?ref=7233306"><img src="https://www.vultr.com/media/banner_1.png" width="728" height="90"></a>




本文转载至[秋水逸冰一键安装包](https://teddysun.com/448.html)






