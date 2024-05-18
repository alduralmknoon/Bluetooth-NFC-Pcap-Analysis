# Bluetooth and NFC Analysis

## Bluetooth

### What is the manufacturer of the Bluetooth device?
**Manufacturer:** Murata  
Found from the Bluetooth Device Address.

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/76768101-58b4-446b-8514-c063299368a3)


### What was the pin code?
**Pin:** 1234

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/60b06076-49fa-4211-8389-c1b04e1bb33c)

### What is the link connection type?
**Link type:** ACL Connection (Asynchronous Connection-oriented Logical transport)

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/37bc1107-6aff-4a20-be03-56a57dad27e9)

### What is the PSM type?
**PSM type:** SDP (Service Discovery Protocol)

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/cfb141bf-931e-4352-96e8-8f321e2fec40)

### What was the service search pattern?
**Service search pattern:** Headset

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/dbc727cc-11a9-4d70-8a37-bff82999d20a)

### What was the remote name?
**Remote name:** NEC 616

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/b872a427-828b-4a6e-bf5e-5148eba402c4)


## NFC
This NFC packet capture is a trace file from a USB-connected NFC transceiver based upon the NXP PN532 chipset containing packets from a successful attempt at enumerating, and reading the contents of different tags.

### Name some of the devices being monitored?
- Linux USB Hub “2.0 Root Hub”, **IP:** 1.1.0 & 2.1.0
- Linux USB Hub “1.1 Root Hub”, **IP:** 3.1.0 & 4.1.0
- Bison Electronics HP Webcam-10, **IP:** 2.2.0
- Wireless car ACR122U by Advanced Card Systems, **IP:** 3.4.0 & 3.5.0

### One of the products is NFC ACR122u contactless card reader. Who is the vendor for the device?
**Vendor:** Advanced Card Systems, Ltd

### Identify when at least one smart card became active.
Device 3.5.2 was active at various times. Here are two screenshots, one at 194.9 seconds and the second at 228.3 seconds.

![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/1b5f488a-047d-45a9-bfcd-a2eadcbbcbc0)


![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/368d8c0e-21da-4def-975d-a630395feb48)

### Observations
- The devices are already assigned an IP address.

#### Explanation of Device Response Packet
- **BcdUSB** indicates what USB specification is being used in binary coded decimal.
- **bDeviceClass**, SubClass, and Protocol indicates the interface the device is using.
- **bcdDevice** are usually used to indicate product version but may also be used to identify chip type in hardware converters.

  
![image](https://github.com/alduralmknoon/Bluetooth-NFC-Pcap-Analysis/assets/27437815/799d065a-51f0-4197-a00f-1322ba77e040)


## NFC Resources:
- [YouTube Video: SF20V - 14 USB Analysis 101 (Tomasz Moń)](https://www.youtube.com/watch?v=cUljKImph4s&t=1447s)
- [USB Component Version 6.16.1, MDK Middleware for USB Device and Host Communication](https://www.keil.com/pack/doc/mw/USB/html/index.html)
- [USB Wireshark Filters](https://www.wireshark.org/docs/dfref/u/usbccid.html)
