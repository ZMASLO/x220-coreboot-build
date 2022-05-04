# Coreboot for Lenovo ThinkPad X220

Be sure to read official documentation of coreboot before atempting to flash. There is always a possibility that you could brick your ThinkPad X220 when trying to flash coreboot.

*Be sure to back up your old BIOS

## Features

- Intel ME neutralized
- Support for Intel Wi-Fi and Bluetooth
- VGA Blob
- Increased DRAM speed
- SeaBIOS payload

## Secondary payloads

- nvramcui
- coreinfo
- tint

#### Flash directly form OS

```sh
 sudo flashrom -p internal:laptop=force_I_want_a_brick -w coreboot.rom -V
```

#### Flash directly form Raspberry PI

```sh
 sudo flashrom -p linux_spi:dev=/dev/spidev0.0,spispeed=512 -w coreboot.rom -V
```