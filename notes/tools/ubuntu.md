# Ubuntu 

## Steps after fresh install

1. Run update
    - system updates
    - update snaps
2. Configure terminal
3. Install KeePassXC from Snap
4. Sync Firefox


## Installing software

### apt

```bash
sudo apt install gnome-tweaks

sudo apt install git

sudo apt install dconf-editor
```

### .deb

- Miniconda / Anaconda


### Snap

Using the App Center the following software can easily be installed:

- [KeePassXC](https://keepassxc.org/download/#linux)
- [VS Code](https://snapcraft.io/code)
- Chromium
- VLC
- LibreOffice
- GIMP
- Darktable
- [Foliate](https://snapcraft.io/foliate) (epub reader)

It is also possible to install via terminal:

```bash
sudo snap install keepassxc

sudo snap install code --classic
```

To list and update all snap packages:

```bash
snap list

snap refresh --list

sudo snap refresh
```

### Nvidia drivers

"Software & Updates" --> "Additional Drivers"


## Tweaks and configuration

### Keyboard shortcut Power off

Adding shortcut for *Power off* screen by setting custom shortcut:

```gnome-session-quit --power-off```


### No lock screen after suspend

Open dconf editor: org -> gnome -> desktop -> screensaver -> ubuntu-lock-on-suspend


### Make header bar of windows "thinner"

Create a CSS file under `.config\gtk-3\gtk.css` with the following content:

```css
headerbar entry,
headerbar spinbutton,
headerbar button,
headerbar separator {
    margin-top: 0px; /* same as headerbar side padding for nicer proportions */
    margin-bottom: 0px;
    min-height: 20px;
}

headerbar {
    min-height: 20px;
    padding-left: 2px; /* same as childrens vertical margins for nicer proportions */
    padding-right: 2px;
    margin: 0px; /* same as headerbar side padding for nicer proportions */
    padding: 0px;
}
```

Press *Alt-F2* und type in `r` to make the changes effective.



### TLP – Linux Advanced Power Management


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


## Tools

### PDF

#### Extracting photos from multiple PDFs using pdfunite and pdfimages

```bash
pdfunite *.pdf allphotos.pdf

pdfimages -j ‘allphotos.pdf’ image
```


## Troubleshooting

### Error: *Can't format USB storage*

I got this fixed by doing the following

Type disks and launch the program,
select the disk or drive you want to format,
press CTRL+F and click format.

After formatting, the disk or drive would be unallocated, therefore you'll have to create a partition by using the plus button on the screen.. Then insert the name you'll like to use as the drive or disk name then click on create. Enjoy....

https://askubuntu.com/questions/769079/cant-format-ubuntu-installation-stick/769094


## Unix shell

- http://swcarpentry.github.io/shell-novice/
- https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29
- https://help.ubuntu.com/community/Beginners/BashScripting
