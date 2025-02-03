Generate new serial numbers in PlatformInfo for MLB, SystemSerialNumber and SystemUUID.

Notes:
- Generally BIOS/EFI config is: disable CSM, enable VMX and VT-d, disable SATA ALPM (cause CPUs CATERRs), set USB XHCI to Enabled. This config assumes you have a bios with MSR patch.
- You can flash latest v.4101 modded BIOS by putting z1016ws.cap onto a FAT-formatted flash drive, inserting it into the USB-Flashback port and pressing Flashback button for three seconds.
- If you really need them and want to do, feel free to re-enable, system will boot but will have some limitations.
- After system install use OCLP to add Broadcom WiFi support. Another way - create an installer with the OCLP.

Sonoma and newer: If you need working Broadcom WiFi, it's impossible to keep SIP and SecureBoot, so you will need to disable them. You also may need to tune NVMEFix.

In  Misc -> Securtity:
```
<key>SecureBootModel</key>
<string>Disabled</string>
```

In NVRAM -> Add:
```
<key>7C436110-AB2A-4BBB-A880-FE41995C9F82</key>
<dict>
   <key>boot-args</key>
   <string>-v -nvmefaspm revpatch=pci,sbvmm</string>
   <key>csr-active-config</key>
   <data>PwgAAA==</data>
</dict>
```
