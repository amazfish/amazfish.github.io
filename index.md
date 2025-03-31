---
layout: default
title: Home
---

![Amazfish logo](https://raw.githubusercontent.com/piggz/harbour-amazfish/refs/heads/master/ui/icons/172x172/harbour-amazfish-ui.png)

# Amazfish

[![Translation status](https://hosted.weblate.org/widget/harbour-amazfish/svg-badge.svg)](https://hosted.weblate.org/engage/harbour-amazfish/)

Companion application for Huami Devices (such as Amazfit Bip, Cor, MiBand2/3 and GTS and GTS) and the Pinetime Infinitime.

Requires Sailfish version 3.0.3.8 or above due to changes in the base Sailfish image.  Instructions for [compilation](https://github.com/piggz/harbour-amazfish/blob/master/documentation/build-instructions.md) including for other operating systems can be found in the `documentation/` directory.

## Installation
* Install the ["chum" repository](https://chumrpm.netlify.app/) (by downloading the RPM file and running `devel-su pkcon install-local RPM_FILENAME` )
* Run `devel-su pkcon refresh`
* Run `devel-su pkcon install harbour-amazfish`

<a href='https://open-store.io/app/uk.co.piggz.amazfish'><img width='240' alt='Download on OpenStore' src='https://open-store.io/badges/en_US.svg'/></a>
<a href='https://flathub.org/apps/details/uk.co.piggz.amazfish'><img width='240' alt='Download on Flathub' src='https://flathub.org/assets/badges/flathub-badge-en.png'/></a>

## Index

* [FAQs](FAQs)
* [Flavors](Flavors)
* [How to update AGPS](How-To-update-AGPS)
* [Devices](/devices)
* [Server Side Pairing Code](Server-Side-Pairing)
* [Note for GTR2 / GTS2 owners](Appearance)
* [Firmware download](firmware-download)
* [Button Actions](button-actions) 
* [Automatic Reconnecting](automatic-reconnecting)



## Supported Devices

There are 3 tiers of supported devices:

### Gold

These are devices I have, have tested, and will try not to break any functionality for any included:
 * Amazfit Bip
 * Amazfit GTS
 * Amazfit GTR2
 * Pinetime InfiniTime
 * Bangle.js - [Android integration](https://www.espruino.com/Gadgetbridge) app should be installed

### Silver

These are devices which are properly implemented in the application, but I do not have and are tested by the community, and include:
 * Amazfit BipS
 * Amazfit Bip Lite
 * Amazfit GTS2
 
I do not promise not to break functionality in these, but will fix where I can.

### Bronze

These are devices which use a protocol that is close to another supported device, and so is treated like that device.  Your mileage may vary with these devices.
 * MiBand 2/3/4
 * Amazfit Cor
 
## Powered by KEXI

As of version 0.5.1, activity data is retrieved into an SQLite database.  Because I think it is important to allow individuals to be in control of their own data, and that they should have the ability to analyze it themselves, I have chosen to store data in a KEXI compatible database.  This will allow you to copy the database from the phone, and open it up inside KEXI on Linux/Windows/Mac and perform queries and reports on it.  This added ability means I link to a couple of KDE libraries, which should be installed automatically.


---

Source: https://github.com/piggz/harbour-amazfish

Credits to:

    The Gadgetbridge devs, which gave me a lot of hints and inspiration from their device code.
    https://codeberg.org/Freeyourgadget/Gadgetbridge

## Automatic Reconnecting

Depending on device and operating system if there are problems with pairing or reconnecting you may need to take one action.
Open the bluetooth settings on your phone and head for known devices. There enter the settings for the watch and enable "reconnect automatically" for it.
This should fix pairing and reconnecting issues.
