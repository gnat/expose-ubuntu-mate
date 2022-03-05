# Exposé Overview Screen for Ubuntu MATE 22.04

Enables "overview screen" or "window picker" function. Similar to:

* Apple MacOS X Exposé or Mission Control.
* KDE Overview.
* GNOME Activities.

![screenshot](https://github.com/gnat/expose-ubuntu-mate/blob/main/screenshot.png)

### Quick and Easy Setup

Requires Skippy XD, while works, is unmaintained and can be difficult to find and install.

1. Get a recent build of libjpeg62-turbo: https://packages.debian.org/sid/amd64/libjpeg62-turbo/download
2. Get a recent build of Skippy XD: http://mxrepo.com/mx/testrepo/pool/test/s/skippy-xd/skippy-xd_0.5.1~git20160429~mx19_amd64.deb
3. Create a file called `overview.desktop` containing the following.

```ini
#!/usr/bin/env xdg-open
[Desktop Entry]
Type=Application
Exec=skippy-xd
Hidden=false
X-MATE-Autostart-enabled=true
Name=Overview
Comment=Executes the Skippy XD window picker daemon.
Icon=/usr/share/icons/Yaru-MATE-dark/256x256/actions/blueman-plugin.png
```
4. Drag `overview.desktop` wherever you desire a clickable button, such as into your MATE panel.
5. Optionally, assign a keyboard shortcut to run `skippy-xd` such as SUPER-Z

### Why?

The information available to do this at the time of writing was non-trivial, so I've simplified it here for my own reference as well as anyone else who wants to benefit from an Expose / Mission Control UX in MATE.
