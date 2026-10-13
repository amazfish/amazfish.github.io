---
layout: default
title: How to update AGPS
---
## How to update AGPS

With current A-GPS data the watch finds a GPS fix much faster. The data is downloaded from the Zepp (Huami)
servers with [huami-token](https://codeberg.org/argrento/huami-token) and sent to the watch by Amazfish.

Amazfish contains an example script that does both when you press the watch button three times:
[contrib/agps](https://github.com/piggz/harbour-amazfish/tree/master/contrib/agps).
Its README describes the setup:

1. Install huami-token.
2. Store your Zepp login in a file readable only by you.
3. Test the download by hand.
4. Copy the script to `~/harbour-amazfish-script.sh` and set the Triple Press Action to Custom Script
   (see [Button Actions](button-actions)).

A-GPS data covers about a week. Update it every few days, or before you go out with GPS.
