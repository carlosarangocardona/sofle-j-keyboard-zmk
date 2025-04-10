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

# Setup steps

- Download and extract firmware.zip
- Turn off both sides
- Connect right side to the computer. Enter bootloader mode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_left-zmk.uf2`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_right-zmk.uf2`.
- Connect right side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the right side by sending the `nice_view_custom-eyelash_sofle_right-zmk.uf2`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the left side by sending the `nice_view-eyelash_sofle_left-zmk.uf2`.
- Connect both sides to the computer via USB cable.
- Pair the sides together by pressing the reset button once on each side at the same time.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
- Disconnect the USB cable from both sides.
- Power on both sides and connect the keyboard to the computer via Bluetooth.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
