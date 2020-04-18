# This is a document to create home assistant on rpi buster -32 bit
```
nano /boot/config.txt
```
add
```
arm_64bit=0
```

After installation 

```
sudo apt update && sudo apt upgrade -y
sudo -s
apt-get install -y software-properties-common apparmor-utils apt-transport-https avahi-daemon ca-certificates curl dbus jq network-manager socat
systemctl disable ModemManager
systemctl stop ModemManager
curl -fsSL get.docker.com | sh
curl -sL "https://raw.githubusercontent.com/home-assistant/supervised-installer/master/installer.sh" | bash -s -- -m raspberrypi4
```


```
usermod -aG docker pi
```
