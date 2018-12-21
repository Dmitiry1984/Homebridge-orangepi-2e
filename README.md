# Homebridge-orangepi-2e
Homebridge installation on Orange Pi Plus 2E (Step-by-Step)

Armbian with desktop for Orange Pi Plus 2E (user root, password 1234)
https://dl.armbian.com/orangepiplus2e/Ubuntu_xenial_default_desktop.7z

To avoid problems with starting apt-get (not nessesary)
killall apt

System update&upgrade
sudo apt-get update
sudo apt-get upgrade

Installation of homebridge, homebridge libraries, web interface etc.
git clone https://github.com/dmitriy1984/Homebridge-orangepi-2e
cd Homebridge-orangepi-2e
bash ./install.sh

Autorun
sudo npm -g install pm2
pm2 start homebridge
pm2 startup
copy-paste the command suggested by 
pm2 save
sudo reboot

WebInterface access via IP: http://xxx.xxx.xxx.xxx:8080
