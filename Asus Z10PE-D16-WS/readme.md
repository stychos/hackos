Generate new serial numbers in PlatformInfo for MLB, SystemSerialNumber and SystemUUID.

Notes:
- Generally BIOS/EFI config is: disable CSM, enable VMX and VT-d, disable SATA ALPM (cause CPUs CATERRs), set USB XHCI to Enabled. This config assumes you have a bios with MSR patch.
- You can flash latest v.4101 modded BIOS by putting z1016ws.cap onto a FAT-formatted flash drive, inserting it into the USB-Flashback port and pressing Flashback button for three seconds.
- Since Sonoma, if you need working Broadcom WiFi, it's impossible to keep SIP and SecureBoot on, so they are disabled here.
- If you really need them and want to do, feel free to re-enable, system will boot but will have some limitations.
- After system install use OCLP to add Broadcom WiFi support. Another way - create an installer with the OCLP.
