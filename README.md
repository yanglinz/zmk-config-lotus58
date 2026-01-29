# Lotus58 ZMK Configuration

My personal [ZMK firmware](https://github.com/zmkfirmware/zmk/) configuration for the [Lotus58 split keyboard](https://github.com/qmk/qmk_firmware/tree/master/keyboards/lotus58)

<img alt="Lotus58 keyboard" src="image/Lotus58.png" />

## Features

- **58-key split layout** - Ergonomic split design with dedicated thumb clusters
- **Homerow mods** - Efficient modifier placement using hold-tap keys

## Layout

<img alt="Keymap for Lotus58" src="image/lotus58.svg" />

## Building the Firmware

The firmware is built via Github Actions. The output can be found in the artifact for a given run.

## Flashing the Firmware

## Layout Features

### Homerow Modifiers

Modified keys on the home row provide quick access to modifiers (Ctrl, Shift, Alt, Gui) while maintaining a compact layout. The implementation uses:

- **Balanced flavor** - Holds resolve as mods when another key is pressed during tapping-term
- **Positional hold-tap** - Same-side keys always tap to avoid accidental mods while rolling
- **Require-prior-idle** - Tap detection based on preceding key activity for reduced delay

## Flashing the Firmware

After building, flash the firmware to your Lotus58:

1. **Put board in bootloader mode** - Usually by pressing the reset button
2. **Copy firmware file** - `build/left/zephyr/zmk.uf2` to the board's mass storage device
3. **Repeat for right side** - Flash `build/right/zephyr/zmk.uf2` to the right board

## Resources 

- [ZMK Documentation](https://zmk.dev/)
- [Keyboard Reference](https://github.com/qmk/qmk_firmware/blob/master/keyboards/lotus58/readme.md)
- [urob's ZMK Config](https://github.com/urob/zmk-config)
