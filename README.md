volume2-linux/
├── DEBIAN/
│   └── control
├── usr/
│   ├── bin/
│   │   └── volume2-linux
│   ├── share/
│   │   ├── applications/
│   │   │   └── volume2-linux.desktop
│   │   └── icons/
│   │       └── volume2-linux.svg
└── volume2_gtk.py  # Основной скрипт
DEBIAN/control:
Package: volume2-linux
Version: 1.0
Architecture: all
Maintainer: YourName <your@email.com>
Depends: python3, python3-gi, gir1.2-appindicator3-0.1, pulseaudio
Description: Volume² for Linux (GTK GUI)
 Windows-like volume control for Ubuntu/Debian.
 usr/bin/volume2-linux:
 #!/bin/sh
python3 /usr/lib/volume2-linux/volume2_gtk.py
volume2-linux.desktop:
[Desktop Entry]
Name=Volume² Linux
Comment=Windows-like volume control
Exec=volume2-linux
Icon=volume2-linux
Terminal=false
Type=Application
Categories=Audio;
https://github.com/ваш-логин/volume2-linux/releases/download/v1.0/volume2-linux.deb
wget https://github.com/ваш-логин/volume2-linux/releases/download/v1.0/volume2-linux.deb
sudo apt install ./volume2-linux.deb
