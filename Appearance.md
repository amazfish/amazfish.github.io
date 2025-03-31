---
layout: default
---
These watches fail to follow the Bluetooth specification, which states that the "Appearance" characteristic should be readable without auth/encryption.  In fact, it seems this
characteristic is not readable at all, even though it is available, and this causes a failure in Bluez.  It seems like Android/iOS are less strict in this regard.

A patch has been added to Bluez which makes it not read the characteristic if it has previously been read and cached, and this allows us to work around the issue.

The device cache is in /var/lib/bluetooth/[host mac address]/[watch mac address/info.

As root, add the line

    Appearance=0x0192

under the [General] heading and restart Bluetooth with

    systemctl restart bluetooth

Do this after pairing the watch in Amazfish.
