---
layout: default
---
## Button Actions

Bip and GTS notify when the watch button is pressed.  This is captured by Amazfish which allows running actions on theses presses.  An action can be ran on 2,3 or 4 presses.
To configure the actions, go to Settings > Application > Button Actions.

A custom script can be used, the script must be called harbour-amazfish-script.sh and be in the home folder.
Example which sends a OTP code to the watch as a message:

    #!/bin/sh
    if [ "$1" == "4" ]; then
        CODE=`python3 -c 'import pyotp;totp = pyotp.TOTP("XXXX Authenticator code here XXXX");print(totp.now())'`
        dbus-send --session --print-reply --dest=uk.co.piggz.amazfish /application uk.co.piggz.amazfish.sendAlert string:'' string:'Google OTP' string:$CODE boolean:true
    fi;

