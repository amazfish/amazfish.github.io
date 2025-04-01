---
layout: default
title: Home
---

# Amazfish

[![Translation status](https://hosted.weblate.org/widget/harbour-amazfish/svg-badge.svg)](https://hosted.weblate.org/engage/harbour-amazfish/)

Companion application for Huami Devices (such as Amazfit Bip, Cor, MiBand2/3 and GTS and GTS) and the Pinetime Infinitime.

## Installation
* Install the ["chum" repository](https://chumrpm.netlify.app/) (by downloading the RPM file and running `devel-su pkcon install-local RPM_FILENAME` )
* Run `devel-su pkcon refresh`
* Run `devel-su pkcon install harbour-amazfish`

<a href='https://open-store.io/app/uk.co.piggz.amazfish'><img width='240' alt='Download on OpenStore' src='https://open-store.io/badges/en_US.svg'/></a>
<a href='https://flathub.org/apps/details/uk.co.piggz.amazfish'><img width='240' alt='Download on Flathub' src='https://flathub.org/assets/badges/flathub-badge-en.png'/></a>

## Index

* [Build instructions](build-instructions)
* [Devices](/devices)
* [Flavors](Flavors)
* [FAQs](FAQs)
* [How to update AGPS](How-To-update-AGPS)
* [Server Side Pairing Code](Server-Side-Pairing)
* [Note for GTR2 / GTS2 owners](Appearance)
* [Firmware download](firmware-download)
* [Button Actions](button-actions) 
* [Automatic Reconnecting](automatic-reconnecting)

## Supported Devices

There are 3 tiers of supported devices:
* Gold - These are devices I have, have tested, and will try not to break any functionality.
* Silver - These are devices which are properly implemented in the application, but I do not have and are tested by the community
* Bronze - These are devices which use a protocol that is close to another supported device, and so is treated like that device.  Your mileage may vary with these devices.
 
## Powered by KEXI

As of version 0.5.1, activity data is retrieved into an SQLite database.  Because I think it is important to allow individuals to be in control of their own data, and that
they should have the ability to analyze it themselves, I have chosen to store data in a KEXI compatible database.  This will allow you to copy the database from the phone,
and open it up inside KEXI on Linux/Windows/Mac and perform queries and reports on it.  This added ability means I link to a couple of KDE libraries, which should be
installed automatically.


---

Source: [https://github.com/piggz/harbour-amazfish](https://github.com/piggz/harbour-amazfish)

Credits to:

    The Gadgetbridge devs, which gave me a lot of hints and inspiration from their device code.
    https://codeberg.org/Freeyourgadget/Gadgetbridge

## ❤️ Donate

If you appreciate this project, consider supporting its development!  

[![Donate via PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://paypal.me/piggz)  

Your support helps keep this project going. Thank you! 🙌  