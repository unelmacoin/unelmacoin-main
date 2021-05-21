
Debian
====================
This directory contains files used to package unelmacoind/unelmacoin-qt
for Debian-based Linux systems. If you compile unelmacoind/unelmacoin-qt yourself, there are some useful files here.

## unelmacoin: URI support ##


unelmacoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install unelmacoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your unelmacoinqt binary to `/usr/bin`
and the `../../share/pixmaps/unelmacoin128.png` to `/usr/share/pixmaps`

unelmacoin-qt.protocol (KDE)

