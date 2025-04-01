---
layout: default
title: Firmware Download
---

## Firmware Download - READ FIRST - I am not liable if you brick your watch ;)

Read this for info about which files to flash: <https://codeberg.org/Freeyourgadget/Gadgetbridge/wiki/Amazfit-Bip>

File download has been tested using an Amazfit Bip and GTS.

The firmware is split into multiple files on these devices.  With the official MiFit app, all are downloaded automatically in the correct order.  With this app, you have to send each file individually.  The firmware files are available by extracting the Zepp apk, and looking in the assets/ folder for files named Mili_chaohu.* for the Bip.  GTS firmware files can be found online, the device name is kestrelw, but be sure the files you are downloading are legitimate.  When you select a file, its type and version will be determined, and you will be prevented from sending invalid files.

The firmware (.fw) requires a matching font (.ft) and resource (.res).  Send the firmware first, the app will send a reboot command at the end of the transfer, and the watch will boot up into a mode where it needs the matching font and resource sent.  Just wait for the app to connect again, then send the font and resource. 

The following types of file exist:

firmware, resource, a-gps data, fonts

So, to re-iterate, the firmware flashing order is:

    .fw
    .ft
    .res


***May not work on all devices***

Uses Bluetooth Low Energy to communicate with the watch, this is known to be problematic on some devices.  It is known to work on the Xiaomi Mido.  Probably also works on the FP2 and is tested on the XA2.

Implemented
    Pairing
    Notifications
    Calls
    Some settings
    Retrieving activities
    Heartrate Chart
    Alarms
    Watchface download
    Firmware upload
    Activity Sync
    Basic music control

Todo
    More Settings
    Support other devices (maybe e.g. MiBand2, as it is similar)


Tip:
On your device, create a symlink in /home/nemo to /home/nemo/.local/share/harbour-amazfish
This way, you can easily copy the database off the phone using MTP.
