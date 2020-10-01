# Panda Status Bar

Panda desktop status bar.

## Dependencies

On Arch Linux:

`sudo pacman -S cmake gcc qt5-base qt5-tools qt5-svg qt5-x11extras kwindowsystem libxtst libxdamage libxcomposite libxrender libxcomposite libxcb xcb-util libdbusmenu-qt5 kdbusaddons libpulse`

TODO: Write for FreeBSD.

## Build

```
mkdir build
cd build
cmake ..
make
sudo make install
```
## How to use

### Qt applications

Currently only works with `QT_QPA_PLATFORMTHEME=kde`. FIXME: Make it work with `QT_QPA_PLATFORMTHEME=qt5ct`.

### Gtk applications (does not work yet)

E.g., Firefox and Chrome use

```
/usr/local/lib/gtk-2.0/modules/libappmenu-gtk-module.so
/usr/local/lib/gtk-3.0/modules/libappmenu-gtk-module.so
```

On FreeBSD:

```
git clone https://github.com/NorwegianRockCat/FreeBSD-my-ports
cd FreeBSD-my-ports/
cd x11/gtk-app-menu/
sudo make
sudo make install
```

```
user@FreeBSD$ gmenudbusmenuproxy
# Now launch firefox
kde.dbusmenuproxy: Got an empty menu for 0 on ":1.103" at "/org/appmenu/gtk/window/0"
```

FIXME: Make it work.

## License

panda-statusbar is licensed under GPLv3.
