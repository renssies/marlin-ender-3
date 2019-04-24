# Marlin 3D Printer Firmware for Ender 3

This is my personal version of Marlin 1.1.x for the Creality Ender 3 (Pro), based of Vanilla Marlin 1.1.9 bugfix. It features support for thermal runaway protection, BL Touch (2.0), SD card and advanced pause features (like filament change with `M600`). But loses a couple of other features.

The current code is made for the [silent 1.1.4 board](https://www.creality3donline.com/creality3d-new-upgrade-silent-114-mainboard-for-ender-3-pro-ender-5-customized-und-non-standard-matching_p0147.html) by Creality, with the [official BL touch kit](https://www.creality3donline.com/creality-bl-touch-auto-bed-leveling-sensor-creality3d-cr-10-ender-3-creality3d-ender3-pro_p0135.html) installed. 

Based on the vanilla Marlin code over at [MarlinFirmware/Marlin](https://github.com/MarlinFirmware/Marlin)

## Enabled Features
- Thermal runaway protection
- BL touch version 2.0 (with offsets for the [official kit](https://www.creality3donline.com/creality-bl-touch-auto-bed-leveling-sensor-creality3d-cr-10-ender-3-creality3d-ender3-pro_p0135.html))
- SD Support
- Advanced pause features, allowing for changing filament mid print
- Slim LCD Menus
- TMC2088 Standalone drivers (for the [official silent main board](https://www.creality3donline.com/creality-bl-touch-auto-bed-leveling-sensor-creality3d-cr-10-ender-3-creality3d-ender3-pro_p0135.html))

## Disabled Features
- Some LCD features (`SLIM_LCD_MENUS` is enabled
- "About Printer" on the LCD
- Arc support (currently unused by all major slicers, including Cura and Simplify3D)
- Scrolling of long text
- Volumetrics features
- Workspace offsets (homing offsets)

## Flashing the Ender 3
1. Install the Arduino IDE
2. Install the custom Sanguino boards using the board manager using this additional boards manager URL: https://raw.githubusercontent.com/Lauszus/Sanguino/master/package_lauszus_sanguino_index.json
3. Install the U8glib library using the libraries manager (you might need to scroll down)
4. Make sure you have a bootloader burned on your board (the silent 1.1.4 has a bootloader by default): https://www.youtube.com/watch?v=fIl5X2ffdyo
5. Open Marlin.ino from this repository and press upload in the Arduino IDE
6. Initialize the EEPROM for the LCD menu

## License

[Marlin](https://github.com/MarlinFirmware/Marlin) is published under the GPL license
