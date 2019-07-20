
Debian
====================
This directory contains files used to package MyTicketCoind/MyTicketCoin-qt
for Debian-based Linux systems. If you compile MyTicketCoind/MyTicketCoin-qt yourself, there are some useful files here.

## MyTicketCoin: URI support ##


MyTicketCoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install MyTicketCoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your MyTicketCoinqt binary to `/usr/bin`
and the `../../share/pixmaps/MyTicketCoin128.png` to `/usr/share/pixmaps`

MyTicketCoin-qt.protocol (KDE)

