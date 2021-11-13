# Routing Table

## 開啟ip_forward

到 /proc/sys/net/ipv4/ip_forward  
將裡面的0改成1  
開啟封包轉送  

```bash=
$ echo '1' | sudo tee /proc/sys/net/ipv4/ip_forward
```
*以上方法只要重新開機就會被清除。  

### ip_forward永久開啟
在 /etc/sysctl.conf 中加入  
```bash=
$ echo 'net.ipv4.ip_forward = 1' | sudo tee -a /etc/sysctl.conf
```

---

## 新增Routing Table

### 1.Alpine
```bash=
$ sudo route add -net $destination netmask $SubnetMask gw $GWIP
# -net -> 目的地 network ID  
# netmask -> 目的地子網路遮罩  
# gw -> gateway  
```
*以上指令只要重新開機就會重置  

#### 永久修改Routing Table  
建立 /etc/local.d/route_set.start  

!!!要記得安裝bash!!!  
```bash=
$ sudo nano /etc/local.d/route_set.start

#!/bin/bash
route add -net $destination netmask $SubnetMask gw $GWIP
```
![](https://i.imgur.com/R7AQv8r.png)  

OR  

![](https://i.imgur.com/9mR700F.png)  

*上為只固定一台，下為一次 key 很多不同 IP  

```bash=
# 賦予執行權限
$ sudo chmod +x /etc/local.d/route_set.start

# 啟用開機執行檔功能
$ sudo rc-update add local

$ sudo reboot
```
每次開機的時候，系統都會執行此檔案  

### 2.Ubuntu Server
新增 /etc/rc.local 的檔案  
```bash=
$ sudo nano /etc/rc.local

route add -net $destination netmask $SubnetMask gw $GWIP
```
![](https://i.imgur.com/RwqpPnt.png)  
```bash=
# 賦予執行權限
$ sudo chmod +x /etc/rc.local
```

###### tags: `Network`
