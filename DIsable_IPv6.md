# 關閉ipv6

## Alpine

```bash=
$ sudo nano /etc/sysctl.conf

# 新增這行  
net.ipv6.conf.all.disable_ipv6 = 1
```
```bash=
# 重啟組態
$ sudo sysctl -p /etc/sysctl.conf
```

---

## Ubuntu
#### 開機自動停用 IPv6
```bash=
$ sudo nano /etc/sysctl.conf

# 新增設定
...
net.ipv6.conf.all.disable_ipv6 = 1
net.ipv6.conf.default.disable_ipv6 = 1
net.ipv6.conf.lo.disable_ipv6 = 1
```

#### 透過 GRUB 停用 IPv6
```bash=
$ sudo nano /etc/default/grub

# 修改 GRUB_CMDLINE_LINUX_DEFAULT 與 GRUB_CMDLINE_LINUX
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash ipv6.disable=1"
GRUB_CMDLINE_LINUX="ipv6.disable=1"
```

參考來源：  
https://officeguide.cc/ubuntu-linux-disable-ipv6-address-tutorial/

###### tags: `Network`
