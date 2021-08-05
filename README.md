# hass - Instalação hass rb3
https://community.home-assistant.io/t/installing-home-assistant-supervised-on-a-raspberry-pi-with-debian-10/247116

apt-mark hold linux-image-arm64
apt update && apt upgrade -y
apt install sudo -y

adduser YOUR_USERNAME
usermod -aG sudo YOUR_USERNAME

#########################################################################

sudo -i

apt-get install -y software-properties-common apparmor-utils apt-transport-https ca-certificates curl dbus jq network-manager

systemctl disable ModemManager

systemctl stop ModemManager

curl -fsSL get.docker.com | sh

curl -sL "https://raw.githubusercontent.com/Kanga-Who/home-assistant/master/supervised-installer.sh" | bash -s -- -m raspberrypi3-64

#########################################################################

https://raw.githubusercontent.com/danformiga/hass/main/installer.sh

sudo apt update && sudo apt upgrade -y && sudo apt autoremove –y
