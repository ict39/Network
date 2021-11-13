# 固定IPv4設定
先確認網卡的名稱  
```bash=
$ ip a
```
## Alpine
```bash=
$ sudo nano /etc/network/interfaces
```
```bash=
auto
iface lo inet loopback

auto eth0
iface eth0 inet static
      address $IP/$subnetmask
      gateway $GWIP
```
![](https://i.imgur.com/5THJYH5.jpg)  

```bash=
$ sudo service networking restart
# 請不要再執行此行命令，直接重啟機器，才可將 DHCPclient 關閉

reboot
```

## Ubuntu server
```bash=
$ sudo nano /etc/netplan/00-installer-config.yaml
```
### 一張網卡
```bash=
network:
  ethernets:
    ens32:
      dhcp4: no
      addresses: [ $IP/$cidr ]
      gatewat4: $GWIP
      nameservers:
        addresses: [ 8.8.8.8, 168.95.1.1 ]
```
![](https://i.imgur.com/zwUMiac.jpg)  
### 多張網卡
```bash=
network:
  ethernets:
    ens32:
      dhcp4: no
      addresses: [ $IP/$cidr ]
      gatewat4: $GWIP
    ens35:
      dhcp4: no
      addresses: [ $IP/$cidr ]
```
![](https://i.imgur.com/u146EKA.jpg)

```bash=
# 先 try 再 apply 
$ sudo netplan try
$ sudo netplan apply
```


###### tags: `Network`
