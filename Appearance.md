---
layout: default
title: Note for owners of GTR2 / GTS2 or newer
---
# Note for owners of GTR2 / GTS2 or newer devices (including variants like 2e or 3pro)

These watches fail to follow the Bluetooth specification, which states that the "Appearance" characteristic should be readable without auth/encryption.  In fact, it seems this
characteristic is not readable at all, even though it is available, and this causes a failure in Bluez. It seems like Android/iOS are less strict in this regard.

A patch has been added to Bluez which makes it not read the characteristic if it has been read and cached once. This allows us to work around the issue.

* Pair your watch with Amazfish. For the moment ignore, that the connection will be unstable.
* Turn off Bluetooth on the phone and make sure the watch is not connected. Otherwise, you can't write to the cached file.
* Find the info file in the devices cache folder. This is in /var/lib/bluetooth/[host mac address]/[watch mac address]/info.
* Edit the info file as root and under the [General] heading add the line

    Appearance=0x0192

  Some devices may already contain a line Appearance=0x00c0. Edit it to match the line above.
* Restart Bluetooth with

    systemctl restart bluetooth

  You should now be able to get a stable bluetooth connection to your device.
