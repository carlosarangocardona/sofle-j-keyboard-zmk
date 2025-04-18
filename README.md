# Update List

- 2024/12/21
  1. Added support for zmk-studio (just refresh the left hand to use).
- 2024/10/24
  1. Modified power supply mode to reduce power consumption.
  2. Fixed the automatic shut-off feature for RGB power supply.

> If your keyboard was updated before October 24, please update to the latest firmware.

---

# Sofle Keymap

<img src="keymap-drawer/sofle.svg" >

# Configuration

## Enabling pointer and encoder

I have disabled the pointer and encoder devices as my keyboard does not have them. If you want to enable them, please uncomment the following lines in `config/eylash_sofle.conf`:

```
# Uncoment these to enable the encoder:
#CONFIG_EC11=y
#CONFIG_EC11_TRIGGER_GLOBAL_THREAD=y


# Uncomment these to enable the pointer/mouse:
#CONFIG_ZMK_POINTING=y

```

# Setup steps

## Flashing firmware

- Download and extract `firmware.zip` after the build action finishes in GitHub.
- Turn off both sides by using the switch on each board.

### Reset the settings

- Connect right side to the computer. Enter bootloader ode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_left-zmk.uf2`.
  - **INFO**: Re-setting will work even if the file name says `left`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_right-zmk.uf2`.

### Send the firmware

- Connect right side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the right side by sending the `nice_view_custom-eyelash_sofle_right-zmk.uf2`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the left side by sending the `nice_view-eyelash_sofle_left-zmk.uf2`.

### Pair sides and test via USB

- Connect both sides to the computer via USB cable.
- Pair the sides together by pressing the reset button once on each side at the same time.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
- Disconnect the USB cable from both sides.

### Connect and test via Bluetooth

- Power on both sides and connect the keyboard to the computer via Bluetooth.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
