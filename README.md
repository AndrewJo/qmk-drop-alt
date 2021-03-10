# qmk-drop-alt :keyboard:

This is a custom QMK keymap and lighting firmware for Drop ALT keyboards.

## Usage

Go to [Releases][releases] and download the binary file. You can use either
[QMK Toolbox][qmk-toolbox] or [mdloader][mdloader] to flash your keyboard.

## Compiling from source

If you don't trust the binary release, you can also build from source. If you
plan on making modifications to the keymap or lighting programs, this will be
mandatory.

### Prerequisites

You will need `qmk` CLI tool in order to build the firmware. Please read
[Setting Up Your QMK Environment][qmk-newbs-getting-started] and set up your
QMK build environment before getting started.

### Getting Started

Navigate to QMK home directory. On default installs, this should generally be
at: `$HOME/qmk_firmware`.

Configure your build environment and set your keyboard as Drop ALT:

```console
qmk config user.keyboard=massdrop/alt
```

Then, add this repository into `keyboards/massdrop/alt/keymaps` as a submodule:

```console
cd keyboards/massdrop/alt/keymaps
git submodule add https://github.com/AndrewJo/qmk-drop-alt AndrewJo/
```

If you plan on modifying the code, please fork this repository first and
replace the repository path accordingly.

You can now build the firmware:

```console
qmk compile
```

This will create a binary file that is named as `massdrop_alt_AndrewJo.bin`.

You can flash this binary using the tools mentioned in the [Usage](#usage)
section above.

## LED Matrix Themes

### Outrun Sunset

![Outrun](https://raw.githubusercontent.com/AndrewJo/qmk-drop-alt/master/outrun-sunset.svg)

[releases]: https://github.com/AndrewJo/qmk-drop-alt/releases
[qmk-toolbox]: https://github.com/qmk/qmk_toolbox
[mdloader]: https://github.com/Massdrop/mdloader
[qmk-newbs-getting-started]: https://docs.qmk.fm/#/newbs_getting_started
