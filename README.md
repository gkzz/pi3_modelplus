# Headless Pi3 Model + Setup
<img src="/demo/login.JPG" alt="Demo to ssh login" style="max-width:100%;">

## Technology Used
- Raspbian GNU/Linux 10 (buster)

## Item Used
- [Raspberry Pi 3 Model b+ ](https://www.amazon.co.jp/dp/B07FQ9678G)
- [SD Card (SDSQUAR-032G-GN6MA)](https://www.amazon.co.jp/gp/product/B074W6YY8K)


## To Do Before SSH Login into RSP3
    I create image file on Windows10. not but ubuntu19.04
### Get image file
- Download image file
    [ftp.jaist.ac.jp](http://ftp.jaist.ac.jp/pub/raspberrypi/raspbian/images/)
    e.g. 2019-07-10-raspbian-buster.zip
- Format your sd card to FAT32 on the following website

- Select image, drive, and run on the following website
    [www.balena.io/etcher](https://www.balena.io/etcher/)


### Touch ssh.txt, wpa_supplicant.conf at /root directory
### Touch  at /root directory
If you succeed in logging in, the above files are deleted /root directory.
wpa_supplicant.conf was created the following at /etc/wpa_supplicant directory.

```
pi@raspberrypi:/etc/wpa_supplicant $ sudo cat wpa_supplicant.conf 
country=JP
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
network={
ssid="<YOUR_SSID>"
psk="<YOUR_PW>"
```

### Finally, just execute login ssh command
```
ssh pi@raspberrypi.local
```

### Trobleshooting
being prepared


### Notes
```
pi@raspberrypi:~ $ cat /etc/os-release 
PRETTY_NAME="Raspbian GNU/Linux 10 (buster)"
NAME="Raspbian GNU/Linux"
VERSION_ID="10"
VERSION="10 (buster)"
VERSION_CODENAME=buster
ID=raspbian
ID_LIKE=debian
HOME_URL="http://www.raspbian.org/"
SUPPORT_URL="http://www.raspbian.org/RaspbianForums"
BUG_REPORT_URL="http://www.raspbian.org/RaspbianBugs"

```

### References
- [hackernoon.com](https://hackernoon.com/raspberry-pi-headless-install-462ccabd75d0)
- [Raspberry Pi 今すぐ食べたいレシピ集 Vol.1](https://raspimoku.booth.pm/items/1309094)