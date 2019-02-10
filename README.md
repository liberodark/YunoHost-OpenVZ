# YunoHost-OpenVZ
YunoHost for OpenVZ only work on Debian 9

## How to use (manual install) :

Copy and Past in your terminal :

```bash
wget -Nnv https://raw.githubusercontent.com/liberodark/YunoHost-OpenVZ/master/install.sh && chmod +x install.sh; ./install.sh
```

## Install Image (auto install) :

#####  1 - Download Image
```bash
wget https://github.com/liberodark/YunoHost-OpenVZ/releases/download/1.0/dedigo-openvz.tar.gz
```
##### 2 - Download SHA
```bash
wget https://github.com/liberodark/YunoHost-OpenVZ/releases/download/1.0/dedigo-openvz.tar.gz.sha512sum
```

##### 3 - Check Integrity
```bash
sha512sum -c dedigo-openvz.tar.gz.sha512sum
```
##### 4 - Install

```bash
apt remove apache2* -y
mv dedigo-openvz.tar.gz / && cd /
tar -xvf dedigo-openvz.tar.gz
```

##### 5 Finish
- Now reboot your server on your panel (not reboot in terminal)
- The login and password is "root" and "admin" / "linux580@"

##### 6 - After reboot 

For change your password
```bash
passwd root && passwd admin
```
For Fix DNS & after reboot your vps on panel
```bash
echo "nameserver 1.1.1.1" > /etc/resolv.dnsmasq.conf
```

## For Debian 8 (manual install) :

```bash
apt update && apt dist-upgrade -y
```

```bash
sed -i 's|jessie|stretch|' /etc/apt/sources.list
```

```bash
apt update && apt dist-upgrade -y
```

Next reboot and run script

## Videos in French :

- https://peertube.fr/videos/watch/34a51448-a49f-4802-9271-1290751309c3
- https://www.youtube.com/watch?v=626tgNMS7SY&t
