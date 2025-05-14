# Sofle Eyelash ZMK Keyboard

## Features

### Hardware

- Wireless keyboard pre soldered and in case bought from [aliexpress](https://www.aliexpress.com/item/1005008460760903.html?spm=a2g0o.order_list.order_list_main.10.60591802zb4gVf). The keyboard does not include switches or keycaps. I ordered the version without knob and mouse.
- Switches are [Kailh Choc V2 Low Profile Switches](https://www.kailh.net/products/kailh-choc-v2-low-profile-switch-set?variant=43775877972210) bought from <https://shelter.shop>.
- Keycaps are [Nuphy nSA Shine-through ABS Keycaps](https://shelter.shop/products/nuphy-nsa-shine-through-pc-keycaps).

### Firmware

- The firmware is based on [ZMK](https://zmk.dev/).
- Home row mods enabled and configured for MacOS as discussed in this [article](https://precondition.github.io/home-row-mods) using ZMK custom [behaviors](https://zmk.dev/docs/keymaps/behaviors/hold-tap#custom-hold-tap-examples).
- Layer configuration done with [Keymap Editor](https://github.com/nickcoutsos/keymap-editor).

## Configuration

### Enabling pointer and encoder

I have disabled the pointer and encoder devices as my keyboard does not have them. If you want to enable them, please uncomment the following lines in `config/eylash_sofle.conf`:

```
# Uncoment these to enable the encoder:
#CONFIG_EC11=y
#CONFIG_EC11_TRIGGER_GLOBAL_THREAD=y


# Uncomment these to enable the pointer/mouse:
#CONFIG_ZMK_POINTING=y

```

## Setup steps

### Flashing firmware

- Download and extract `firmware.zip` after the build action finishes in GitHub.
- Turn off both sides by using the switch on each board.

#### Reset the settings

- Connect right side to the computer. Enter bootloader ode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_left-zmk.uf2`.
  - **INFO**: Re-setting will work even if the file name says `left`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Reset the settings by sending the `settings_reset-eyelash_sofle_right-zmk.uf2`.

#### Send the firmware

- Connect right side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the right side by sending the `nice_view_custom-eyelash_sofle_right-zmk.uf2`.
- Connect the left side to the computer. Enter bootloader mode by pressing the reset button twice.
- Send the firmware for the left side by sending the `nice_view-eyelash_sofle_left-zmk.uf2`.

#### Pair sides and test via USB

- Connect both sides to the computer via USB cable.
- Pair the sides together by pressing the reset button once on each side at the same time.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
- Disconnect the USB cable from both sides.

#### Connect and test via Bluetooth

- Power on both sides and connect the keyboard to the computer via Bluetooth.
- Test the keyboard. Both sides should be connected and the keyboard should work properly.
