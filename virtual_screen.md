## Virtual screen

Trying to figure out how to use an ipad as a 2nd display in ubuntu,
without much success at this point.

See [this about xrandr](https://linuxconfig.org/how-to-configure-your-monitors-with-xrandr-in-linux
) and [this about x11vnc](https://linuxconfig.org/how-to-share-your-desktop-in-linux-using-x11vnc
).

- iPad mini 4 is 2048 &times; 1536 (half that is 1024 &times; 768).

- iPad Pro is 2732 &times; 2048 (half that is 1366 &times; 1024).

- install x11vnc

  ```
  sudo apt update
  sudo apt install x11vnc
  ```

- create `/usr/share/X11/xorg.conf.d/20-intel.conf` containing the
  following:

  ```
  Section "Device"
      Identifier "intelgpu0"
      Driver "intel"
      Option "VirtualHeads" "2"
  EndSection
  ```

- Log out and log in again, and when you type `xrandr` there'll be
  `VIRTUAL1` and `VIRTUAL2` listed
