# TLP – Linux Advanced Power Management


http://thinkwiki.de/TLP_-_Linux_Stromsparen

https://linrunner.de

https://linrunner.de/tlp/installation/ubuntu.html

```bash
sudo apt install tlp tlp-rdw

# for Thinkpads
tlp-stat -b #suggest which additional package to install
sudo apt install acpi-call-dkms

# bluetooth off at startup:
sudo nano /etc/tlp.conf

DEVICES_TO_DISABLE_ON_STARTUP="bluetooth"

# Akku-Ladeschwellen vorübergehend auf Maximum setzen
sudo tlp fullcharge [ BAT0 | BAT1 ]

# Akku einmalig bis zur oberen Schwelle laden
sudo tlp chargeonce [ BAT0 | BAT1 ]
```
