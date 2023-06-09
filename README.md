dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X. This is my custom version modified to my taste. I'll make it publicly available in case someone wants to use dwm but don't want to waste too much time customizing it, this person is me in the future hehe.

![Alt text](https://i.imgur.com/k08lWoe.png "Dwm screenshot")


Requirements
------------
In order to build dwm you need the Xlib header files.
The default terminal in the "config.h" file is Alacritty, If you want to use a different terminal you'll have to change it. 


Installation
------------
Edit "config.mk" to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):


`make clean install`


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

`exec dwm`

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

`DISPLAY=foo.bar:1 exec dwm`

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:
```
    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm
```

Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

For more information access https://dwm.suckless.org/.
