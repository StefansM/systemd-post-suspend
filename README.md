# systemd-post-suspend

AUR package for a systemd service that runs these commands after the systme is
resumed:

* `/usr/bin/xset -b`
* `/usr/bin/xkbcomp -I/home/%i/.xkb /home/%i/.xkb/keymap/default`
