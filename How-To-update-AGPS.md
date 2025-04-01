---
layout: default
title: How to update AGPS
---
## How to update AGPS

AGPS files need to be downloaded from the Huami servers, then sent to the watch.  This can be achieved with the following method

1. Use the huami-token python tool to download the AGPS files

  - git clone https://github.com/piggz/huami-token
2. Use the Amazfish custom button handling to script downloading the files and uploading to the device

  - Create a script harbour-amazfish-script.sh with the following content

```
#!/bin/sh
if [ "$1" == "3" ]; then
    dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.sendAlert string:'' string:'AGPS' string:'Downloading files...' boolean:true
    python3 ~/huami-token/huami_token.py -m <method> -g -e <email> -p <password>
    dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.sendAlert string:'' string:'AGPS' string:'Uploading files...' boolean:true
    dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.prepareFirmwareDownload string:'/home/defaultuser/gps_uihh.bin'
    sleep 1
    dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.startDownload
    dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.sendAlert string:'' string:'AGPS' string:'AGPS Update Started' boolean:true
fi;

```

  Change the method, email and passowrd to match your huami/amazfit account type (see the docs for huami-token)
  - In Amazfish, Settings, Application, Button Actions, set the Tripe  Press Action to Custom Script
