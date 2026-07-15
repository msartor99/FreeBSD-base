# FreeBSD-base

# july 14 2026, new script universal to set FreeBSD 15.1 as a workstation

This script make post installation to enhance FreeBSD 15.1 base setup.

firestinstall FreeBSD 15.1, use usb key, procedure mustfind on internet.

my procedure:

install freebsd, add local user and set power management and mouse 

enter root

type : 

pkg update

pkg install -y sudo htop neofetch wget

ue visudo to enable wheel root 

to enable root at ssh, vi /etc/ssh/sshd_config

add: PermitRootLogin yes at the end, then : x

run freebsd-update fetch install

reboot a now you can run poste-install-new.sh


to use post-install-new.sh


wget -O post-install-new.sh https://raw.githubusercontent.com/msartor99/FreeBSD-base/main/post-install-new.sh

chmod +x post-install-new.sh

./post-install-new.sh
