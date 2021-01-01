# macOS Catalina 10.15.7 on Thinkpad P51

Updated on December 12, 2020

## Intro:

Was tangling with Clover for quite a bit and found OpenCore is way better in terms of coping with this Hackintoshing stuff.

## Bootloader:
OpenCore 0.6.3, working on Catalina 10.15.1 to 10.15.7 (Tested on 10.15.1, 10.15.6, and 10.15.7).

## Hardware: 

Hardware Specs: https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_P51/ThinkPad_P51_Spec.PDF

| Category | Element | Compatibility | Notes |
| -------- | ------- | ------------- | ----- |
| CPU  | i7-7700HQ | FULL | Native power management works correctly |
| GPU  | HD630 | FULL | Same as above. Full hardware acceleration. |
| | NVIDIA M1200 | NO:DISABLED | Disabled using boot-args: -wegnoegpu |
| MEMORY | 2x16GB | FULL | in Good Shape |
| DISPLAY | 4K   | FULL | in Good Shape |
| STORAGE | 512GB SSD | FULL | Cruicial M.2 NVMe 512GB SSD 8Gb/s |
|   | 512GB SATA HD | FULL | Seagate SATA 512GB HDD 6Gb/s, 7200rpm |
| ETHERNET | Intel I219-V | FULL | in Good Shape |
| WLAN | Intel Dual Band AC8265 | FULL | Per Chinese-sponsored OpenIntelWireless project: https://github.com/OpenIntelWireless/itlwm. Please use the AirportItlwm.kext though. Solute Chinese geeks! |
| BLUETOOTH | Intel Dual Band AC8265 | FULL | Per Chinese-sponsored OpenIntelWireless project: https://github.com/OpenIntelWireless/IntelBluetoothFirmware. Solute Chinese geeks!  |
| EXPRESS CARD | | NO | Pending further exploration |
| SD READER | Realtek RTS525A | NO | Pending further exploration |
| PORTS | 4xUSB3.1 Gen 1 (3.0) | FULL | Correctly setup through USBInjectAll.kext |
| | Dock | FULL | No comments |
| | 1xUSB C (Thunderbolt) | YES | nVidia is disabled, so does this related port. |
| | HDMI 1.4b | NO | nVidia is disabled, so does this related port. |
| | Mini DP 1.2a | NO | nVidia is disabled, so does this related port. |
| CAMERA | | FULL | No comments |
| AUDIO | Realtek ALC298 | FULL | AppleALC.kect + Layout #3, Can be specified in boot-args: alcid=3 \| Speakers + Internal Mic + Headphone - all good |
| ULTRANAV | Trackpoint | YES | Movement is jumpy, more investigation needed. |
| Touchpad | Touchpad | YES | VoodooPS2Controller.kext |
| Mouse | Mouse | YES           | VoodooPS2Controller.kext |
| Keyboard | Keyboard | YES           | VoodooPS2Controller.kext, backlit is great by backlit.kext. |
| COLOR CALIBRATOR | | NO | Pending further exploration |



## Software:

| Feature | Compatibility | Notes |
| ------------- | ------------- | ------------- |
| Sleep + Wake | FULL |  |
| Battery Status | FULL |  |
| Brightness Control | FULL | https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/ |
| App Store | FULL | with white-washing code |
| iTunes | FULL | with white-washing code |
| iMessage | FULL | with white-washing code |
| Siri | FULL | with white-washing code |
| Facetime | FULL | with white-washing code |
| AirDrop | No | Built-in Intel Wifi-Bluetooth AC8265 is not native, nor this service |
| HandOff | No | Built-in Intel Wifi-Bluetooth AC8265 is not native, nor this service |

## References:
1) OpenCore Guide: https://dortania.github.io/OpenCore-Install-Guide/
2) Lenovo website: https://www.lenovo.com/





