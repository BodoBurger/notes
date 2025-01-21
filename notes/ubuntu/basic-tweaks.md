# Basic tweaks and configuration

## Disable middle click paste

https://wiki.ubuntuusers.de/GNOME_Tweak_Tool/

## Disable looking for wifi printer

```bash
/etc/cups/cups-browsed.conf

## Change BrowseRemoteProtocols dnssd cups to
BrowseRemoteProtocols none
```

https://ubuntuforums.org/showthread.php?t=2330752


## Keyboardshortcut Power off

Adding shortcut for *Power off* screen by setting custom shortcut:

```gnome-session-quit --power-off```


## Kein Lock screen nach Suspend

https://www.techgrube.de/tutorials/ubuntu-sperrbildschirm-nach-standby-deaktivieren

"Die gewünschte Einstellung findet man dann unter org -> Gnome -> Desktop -> screensaver. Hier entfernt man einfach bei ubuntu-lock-on-suspend das Häkchen."


## Make header bar of windows "thinner"

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
