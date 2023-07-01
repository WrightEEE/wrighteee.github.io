# [wrighteee.github.io](https://wrighteee.github.io/)
# [https://raw.fastgit.org/freefq/free/master/v2](https://raw.fastgit.org/freefq/free/master/v2)
## Mirror script provided by v2rayA
curl -Ls https://mirrors.v2raya.org/go.sh | sudo bash
You can turn off the service after installation, because v2rayA does not depend on the systemd service.
sudo systemctl disable v2ray --now ### Xray needs to replace the service with xray
## Install v2rayA
### Method 1: Install through the software source
Add public key
wget -qO - https://apt.v2raya.org/key/public-key.asc | sudo tee /etc/apt/trusted.gpg.d/v2raya.asc
Add V2RayA software source
echo "deb https://apt.v2raya.org/ v2raya main" | sudo tee /etc/apt/sources.list.d/v2raya.list
sudo apt update
### Method 2: Manually install the deb package
After downloading the deb package , you can use graphical tools such as Gdebi, QApt to install, or you can use the command line:
sudo apt install /path/download/installer_debian_xxx_vxxx.deb ### Replace the actual path where the deb package is located by yourself
## Start v2rayA / Enable v2rayA start automatically
Start v2rayA
sudo systemctl start v2raya.service
Set auto-start
sudo systemctl enable v2raya.service
