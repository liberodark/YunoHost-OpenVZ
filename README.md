# YunoHost-OpenVZ
YunoHost for OpenVZ only work on Debian 9

## How to use :

Copy and Past in your terminal :

```bash
wget -Nnv https://raw.githubusercontent.com/liberodark/YunoHost-OpenVZ/master/install.sh && chmod +x install.sh; ./install.sh
```

### Install Image :

- Download Image
```bash
wget -Nnv https://github.com/liberodark/YunoHost-OpenVZ/releases/download/1.0/dedigo-openvz.tar.gz
```
- Download SHA
```bash
wget https://github.com/liberodark/YunoHost-OpenVZ/releases/download/1.0/dedigo-openvz.tar.gz.sha512sum
```

- Check Integrity
```bash
sha512sum -c dedigo-openvz.tar.gz.sha512sum
```
- Install

```bash
tar -xvf dedigo-openvz.tar.gz
```

- Finish now reboot your server on your panel (not reboot in terminal) !

### For Debian 8 :

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
