Folding@home Client Advanced Control
====================================

FAHControl can monitor and control one or more FAHClients.

To run:

    python FAHControl

See: https://foldingathome.org/

# Prerequisites

## Debian / Ubuntu

    sudo apt-get install -y python-stdeb python-gtk2 python-all debhelper

## RedHat / CentOS

    sudo yum install -y pygtk2

## Windows 10 / MSYS2

Basically follow https://www.gtk.org/docs/installations/windows/#using-gtk-from-msys2-packages and the instructions on https://www.msys2.org/

    pacman -Syuu
    pacman -S mingw-w64-x86_64-python3 mingw-w64-x86_64-gtk3 mingw-w64-x86_64-python3-gobject

FIXME: I'm not sure if you have to install the packages `mingw-w64-x86_64-toolchain base-devel` as well.

Now you can start FAHControl:

    python FAHControl

Optionally install for development / building:

    pacman -S mingw-w64-x86_64-python3-pip mingw-w64-x86_64-glade mingw-w64-x86_64-python3-pytest

For building an executable:

    pip install pyinstaller
    pyinstaller FAHControl --windowed
