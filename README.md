# Homebridge-orangepi-2e
Homebridge installation on Orange Pi Plus 2E

# Armbian with desktop for Orange Pi Plus 2E (user root, password 1234)
https://dl.armbian.com/orangepiplus2e/Ubuntu_xenial_default_desktop.7z

# System Update
sudo apt-get update
sudo apt-get upgrade

# If there are problems with starting apt-get
killall apt

# Node.js installation
wget https://nodejs.org/dist/latest-v11.x/node-v11.5.0-linux-armv7l.tar.xz
tar xJvf node-v11.5.0-linux-armv7l.tar.xz
cd node-v11.5.0-linux-armv7l
sudo cp -R * /usr/local/

# Librrary for Homebridge
sudo apt-get install libavahi-compat-libdnssd-dev
sudo apt-get install -y nodejs libavahi-compat-libdnssd-dev

# Homebridge installation
sudo npm install -g --unsafe-perm homebridge
mkdir ~/.homebridge && cp config.json ~/.homebridge

# Homebridge Web Interface
sudo npm i -g --unsafe-perm homebridge homebridge-config-ui-x

