# This is a document to create home assistant on rpi buster -64 bit
```
nano /boot/config.txt
```
add
```
arm_64bit=1
```

After installation 

```
sudo apt update && sudo apt upgrade -y
sudo apt-get install -y software-properties-common apparmor-utils apt-transport-https avahi-daemon ca-certificates curl dbus jq network-manager socat -y
sudo systemctl disable ModemManager
sudo systemctl stop ModemManager
sudo -i
curl -fsSL get.docker.com | sh
usermod -aG docker pi
curl -sL "https://raw.githubusercontent.com/home-assistant/supervised-installer/master/installer.sh" | bash -s -- -m raspberrypi4
```
