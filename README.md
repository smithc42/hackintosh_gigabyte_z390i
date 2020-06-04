# hackintosh_gigabyte_z390i

CFG-Lock must be turned off manually. Follow guide [here](https://dortania.github.io/OpenCore-Desktop-Guide/extras/msr-lock). When using UEFITool, the `CFG Lock` string can be found at the following path:

```
Intel image -> BIOS region -> 4F1C52D3-D824-4D2A-A2F0-EC40C23C5916 -> 9E21FD93-9C72-4C15-8C4B-E77F1DB2D792 -> LzmaCustomDecompressGuid -> Volume image section -> 5C60F367-A505-419A-859E-2A4FF6CA6FE5 -> Setup
```

CFG Offset:

```
CFG Lock, VarStoreInfo (VarOffset/VarName): 0x5C1
```

Command:
`setup_var 0x5C1 0x00`

Bios version: [F8c](https://www.gigabyte.com/ie/Motherboard/Z390-I-AORUS-PRO-WIFI-rev-10/support#support-dl-bios)

### Bios settings

- CSM Support -> Disabled : Not working
- Internal Graphics -> Enabled :  Working
- Wi-Fi -> Disabled :  Working
- Above 4G Decoding -> Enabled : Working
- Wake on LAN Enable -> Disabled : Working
- Settings -> USB Configuration -> Legacy USB Support -> Disabled : Working
- Settings -> USB Configuration -> XHCI Hand-off -> Enabled : Working
- Settings -> Miscellaneous -> Software Guard Extensions(SGX) -> Disabled : Working
- Settings -> Miscellaneous -> Trusted Computing -> Security Device Support -> Disabled
