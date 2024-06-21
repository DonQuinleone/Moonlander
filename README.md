# Don's Moonlander

The source code for my ZSA Moonlander Mark I.

## Setup build environment

1. Install qmk, as per [their docs](https://docs.qmk.fm/newbs_getting_started).
   On macOS, that's:

   ```
   brew install qmk/qmk/qmk
   ```

   And on Arch it's:

   ```
   yay -S qmk-git
   ```

2. Then run the following to setup the environment:

   ```
   # Get ZSA's fork of the qmk firmware and required submodules
   git clone --recursive -j8 git@github.com:zsa/qmk_firmware.git ~/Documents/qmk_firmware

   # Setup environment
   qmk setup -H ~/Documents/qmk_firmware -b firmware23 zsa/qmk_firmware

   # Add source
   cd ~/Documents/qmk_firmware/keyboards/moonlander/
   git submodule add git@github.com:DonQuinleone/Moonlander.git don

   ```

## Compiling

To compile the keymap, simply run:

```
cd ~/Documents/qmk_firmware/
make moonlander:don
```
