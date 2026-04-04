---
image: "kospet_dk08.png"
title: "Kospet DK08"
link: "https://kospet.com/"
features:
  - id: "pairing"
    value: "Y"
  - id: "calls"
    value: "Y^"
  - id: "navigation"
    value: "N/A"
  - id: "battery_status"
    value: "Y"
  - id: "sync_time"
    value: "Y"
  - id: "find_my_phone"
    value: "N/A"
  - id: "FEATURE_HRM"
    value: "Y"
  - id: "FEATURE_WEATHER"
    value: "Y"
  - id: "FEATURE_ACTIVITY"
    value: "N"
  - id: "FEATURE_STEPS"
    value: "Y"
  - id: "FEATURE_ALARMS"
    value: "Y"
  - id: "FEATURE_ALERT"
    value: "Y"
  - id: "FEATURE_EVENT_REMINDER"
    value: "N"
  - id: "FEATURE_MUSIC_CONTROL"
    value: "N"
  - id: "FEATURE_BUTTON_ACTION"
    value: "N"
  - id: "FEATURE_SCREENSHOT"
    value: "N"
  - id: "FEATURE_FILE_INSTALL"
    value: "N"
  - id: "TYPE_DEBUGLOG"
    value: "N"
  - id: "TYPE_ACTIVITY"
    value: "N"
  - id: "TYPE_GPS_TRACK"
    value: "N"
  - id: "TYPE_STRESS"
    value: "N"
  - id: "TYPE_SPO2"
    value: "N"
  - id: "TYPE_PAI"
    value: "N"
  - id: "TYPE_HEART_RATE"
    value: "Y"
  - id: "TYPE_SLEEP_RESPIRATORY_RATE"
    value: "N"
  - id: "TYPE_TEMPERATURE"
    value: "N"
  - id: "TYPE_SLEEP"
    value: "N"
  - id: "TYPE_HUAMI_STATISTICS"
    value: "N"
  - id: "TYPE_HRV"
    value: "N"

---

Kospet DK08 is nrf52832 watch with always on sunlight readable display (176x176, 64 colors - RGB222).
The hardware is designed by same Manridy manufacturer as F07 or F10 fitness trackers and all use
[IBand](https://play.google.com/store/apps/details?id=com.manridy.iband_new) android app so upgrade guide
is similar/same to F07.

## Hardware

* LCD always on 176x176 64 colors (RGB222) ST7301
* HR sensor EM7028 (datasheet linked from here), for code examples search github for EM7028
* accelerometer Bosch BMA222E - gives CHIP ID 0xf8 (datasheet, linked from here), driver source here
* 2MB SPI flash / fontchip GT24L24A2Y

## Notes
* Calls – Currently, it is not possible to reject, silence, or accept phone calls.
* Alarms – Currently, it is not possible to set an alarm for a specific day of the week.
