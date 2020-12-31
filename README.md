# Hackintosh-Aero-15X
Hackintosh for Gigabyte Aero 15X V8 with Intel Wifi Card
Tested and working on macOS Catalina

Please see the following for more details:

original credits : https://www.tonymacx86.com/threads/guide-aero-15x-v8-mojave-catalina.287164/

## Specs

```
- Processor: i7-8750H
- Memory: 32GB 2400 MHz DDR4 (Upgraded, originally was 16GB)
- Panel: LCD UHD 60Hz IPS
- Graphics: Intel UHD Graphics 630 + NVIDIA GeForce GTX 1070 GDDR5 8GB (Disabled)
- Wifi + Bluetooth: Intel Wireless-AC 9260

I/O | Ports:

- 3x USB 3.1 Gen1 (Type-A)
- 1x Thunderbolt™ 3 (USB Type-C)
- 1x HDMI 2.0
- 1x mini DP 1.4
- 1x 3.5mm Headphone/Microphone Combo Jack
- 1x SD Card Reader
- 1x DC-in Jack
- 1x RJ-45

Misc:
- Internal Speaker
- HD Camera
```
### Notes:

- EFI based

## How to use this repository:

`/OpenCore/` has a general config for OpenCore. Consider the current supported macOS version of this repository
- EFI/OC: All necessary OpenCore files (with kexts, configs, patches, etc.)
- EFI/Boot: Has other necessary boot files


## Working

**USB Based Devices**
- [✓] All USB ports (2.0 + 3.0)
- [✓] Card Reader (3.0)
- [✓] HD Camera (2.0)
- [✓] Keyboard (2.0)

**Network**
- [✓] Ethernet card
- [✓] Intel WiFi + Bluetooth

**Power**
- [✓] CPU power management
- [✓] Battery indicator
- [✓] USB PM
- [✓] Shutdown/*Sleep/Restart
- [✓] Saving/Restoring screen brightness on reboot
- [✓] **Disable eGPU to save power

*\* For Sleep to work, add **-wegnoegpu** to your boot-args (Mojave/Catalina+). However, this makes USB-C external monitors undetectable after boot*

*\*\* Prefer to use **SSDT-Disable-DGPU.aml** patch to save power, as it ACPI disables the eGPU. This also makes USB-C external monitors undetectable after boot*
 
**-wegnoegpu** can be used in conjunction with **SSDT-Disable-DGPU.aml**

**Graphics**
- [✓] Intel graphics card

**Misc**
- [✓] Sound (internal speakers + mic jack on/off)
- [✓] Touchpad + Gestures
- [✓] Thunderbolt hotplug (see: [POSTINSTALL](./POSTINSTAL.md))

## Not working/Issues

- [-] Audio thorugh Thunderbolt - HDMI (Works Sometimes)
- [ ] HDMI (Apple removed support for Nvidia after High Sierra)

---
## Support status:

- MacOS 11.x (Bug Sur) - Current supported version
- MacOS 10.15 (Catalina) - download [here](https://github.com/sanchitd5/Hackintosh-Aero-15X/tree/eb742bd8d6fbadda77beef71243e1018ca31535b)


## Special thanks to:

* [zacmks](https://github.com/zacmks/Hackintosh-Aero-15X) for the original guide

* [RehabMan](https://github.com/RehabMan) for his great guides, tools, tutorials, DSDTs, kexts and contribution to the Hackintosh community

* [acidanthera](https://github.com/acidanthera) for all the kexts, tools and contribution to the Hackintosh community

* [vit9696](https://github.com/vit9696) for all the kexts, tools and contribution to the Hackintosh community

* [PMHeart](https://github.com/PMHeart) for all the kexts, tools and contribution to the Hackintosh community

* [al3xtjames](https://github.com/al3xtjames) for all the kexts, tools and contribution to the Hackintosh community

* [Andrey1970AppleLife](https://github.com/Andrey1970AppleLife) for all the kexts, tools and contribution to the Hackintosh community

* [corpnewt](https://github.com/corpnewt) for SSDTTime

* [headkaze](https://github.com/headkaze) for his tools and great tutorials

* [OpenCore Project](https://github.com/acidanthera/OpenCorePkg) for making this possible

* [Clover Project](https://sourceforge.net/projects/cloverefiboot/) for creating Clover bootloader and for making this possible

* [aar0npham](https://github.com/aar0npham) for testing and giving great feedbacks

* [BAndysc](https://github.com/BAndysc) for ELAN touchpad support

And many many other people with contributions on these projects
