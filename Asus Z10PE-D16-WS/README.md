Important firmware options
--------------------------

- disable CSM
- enable USB XHCI
- enable USB hand-off
- disable AHCI ALPM (cause freezes with the CPU CATERR)

In my personal practice VT-d and SR-IOV doesn't need to be disabled


CPU Power management
--------------------

This build is for single Xeon E5-2618L V3 CPU, which is 8 cores / 16 threads.
If you have another CPU:
1. remove ACPI/patched/SSDT.aml
2. Enable `PluginType` checkbox in the Clover Configurator or make a new SSDT.aml using CPUFriend manual (don't forget to combine it with the frequency vectors)


Graphics
--------

This build is intended to work with the supported OOB Radeon RX series.
Sorry NVidia users, can't help here (only if you'll gift me your graphics card).
