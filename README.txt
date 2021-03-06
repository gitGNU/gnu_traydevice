Traydevice
==========
Traydevice is a little desktop application displaying systray icon
allowing you to conveniently execute custom commands 
on the specified device.

Usage
=====
Using trydevice is fairly simple, just execute it passing it a device file 
of device you want to have in systray. Icon will appear with actions in
right-click menu. If device is removed from system, program terminates.
traydevice --help should tell you everything you need to know.

Originally, traydevice was created to be executed from halevt.
(http://www.nongnu.org/halevt/). 
Just execute "traydevice $hal.block.device$" on insertion of the device.

Requirements
============
 - pygtk
 - python-lxml
 - python-dbus
 - docbook2x (for manpages)
 - pyxdg
 - udisks 

Installation
============
There's a standard python distutils based installation script setup.py
at the top level of the source package.

Running 
  python setup.py instal
as root will install traydevice to your system.

If you wish to finetune some parameters of installation,
  python setup.py --help 
will show a list of possibilities.

For futher details how to use distutils script please consult 
http://docs.python.org/install/index.html#install-index

Configuration
=============
When ran for the first time, it creates a default configuration file
at $HOME/.config/traydevice/default.xml.
This file is well documented xml, that you should run quickly enough into.
Basically, it assigns actions to entries in menu, allowing you to 
reference various device properties.

TODO
====
 - non stockitem icons
 - patch build scripts so that they'll generate list of todos/fixmes into deployed README.txt
