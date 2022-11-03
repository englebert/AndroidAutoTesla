### Android Auto Tesla

Basically is using pure Raspbian OS running on Pi3 or Pi4 to serve as the infotainment center
For your Tesla via the pi3 or pi4 wireless. The Android Auto Tesla projects includes OpenDash, AASDK,
OpenAuto, Dash, ustreamer, WiFi Hotspot, Internet connectivity, DHCP server, DNS Server, NTP and some custom
scripting to make this works.

Main features of the Android Auto Tesla:
- WiFi Hotspot using 5G (Provides best and fastest speed to the Console)
- Including 4G dongle that will provides internet access for Tesla
- DHCP server for the whole solution
- DNS server
- Embedded OpenAuto
- Custom mouse pointer detection sending clicks from web to UI
- Streaming display contents to CSI port and broadcasting it.
- Auto power saving when the android device is removed.

### Getting Started
#### Parts
- Raspberry Pi3B+/Pi4
- 4G WiFi Dongle [https://www.aliexpress.com/item/1005003707568410.html]
- HDMI to CSI Adapter [https://www.waveshare.com/hdmi-to-csi-adapter.htm]
- Configurable HDMI to micro HDMI length (https://www.aliexpress.com/i/4000014554460.html)
- Right Angle USB C Cable [https://www.ugreen.com/products/60w-pd-usb-c-to-c-fast-charging-cable?variant=39915659231294]
- Pi4 Case With Fan [https://www.elektor.com/joy-it-magnetic-plastic-case-with-dual-fan-for-raspberry-pi-4]
- 32GB high endurance microsd card [https://www.westerndigital.com/en-ap/products/memory-cards/sandisk-high-endurance-uhs-i-microsd#SDSQQNR-032G-GN6IA]

#### Preparations
1. Insert SIM into the 4G Dongle, make sure is connectable and disable DHCP services and WiFi Services. As we are not using it for the purpose of using own set of DHCP ip range and also using pure 5.8GHz WiFi from the Pi3B+/Pi4.
2. Download the latest Raspian OS (Legacy) with Desktop. We need the UI for the whole process. It will be confugure to open starting up the OpenDash only. I will show you how to do this later in the process. [https://downloads.raspberrypi.org/raspios_oldstable_armhf/images/raspios_oldstable_armhf-2022-09-26/2022-09-22-raspios-buster-armhf.img.xz]
3. Extract the downloaded image into SDCard. I am using Linux for this case:
```
xz -d -k -v raspios_oldstable_armhf-2022-09-26/2022-09-22-raspios-buster-armhf.img.xz
```
4. From the extracted image, lets write it into the micro sdcard directly:
```
dd if=raspios_oldstable_armhf-2022-09-26/2022-09-22-raspios-buster-armhf.img of=/dev/mmblk0 bs=100M status=progress
```
5. Once done, put the microsd into the Pi3B+/Pi4B and attach to a temporary monitor for some minor configurations.
6. Lets power up and wait.
