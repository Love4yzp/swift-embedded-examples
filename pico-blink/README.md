# pico-blink

<img src="https://raw.githubusercontent.com/kubamracek/swift-evolution/branch/assets/pico-blink.jpg">

## How to build and run this example:

- Connect the Pico W board via a USB cable to your Mac, and make sure it's in the USB Mass Storage firmware upload mode (either hold the BOOTSEL button while plugging the board, or make sure your Flash memory doesn't contain any valid firmware).
- Make sure you have a recent nightly Swift toolchain that has Embedded Swift support.
- Build and copy the program in the UF2 format to the Mass Storage device to trigger flashing the program into memory (after which the device will reboot and run the firmware):
``` console
$ cd pico-blink
$ TOOLCHAINS='<toolchain-name>' ./build.sh
$ cp .build/blink.uf2 /Volumes/RP2040
```
- The green LED should now be blinking in a pattern.

TODO: Remove unused stuff from HAL/Hardware