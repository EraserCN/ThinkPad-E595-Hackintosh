# ThinkPad-E595-Hackintosh
 Hackintosh for ThinkPad E595/E495. Also works for T495 with a minor change of Audio-related stuff.


## Features
- **Working**: keyboard, trackpad, USB ports, Audio and GPU acceleration.
- **TBA**: Wi-Fi, Bluetooth, Sidecar, AirDrop, etc (Until I have a capable Wifi Card)
- **Won't Work at All**: Fingerprint, iPhone Mirroring(T2 Chip required), DRM-related stuff

## Prerequisites
1. **Compatible Hardware**:
   - Laptop Model: ThinkPad E595
   - CPU: AMD Ryzen 5 3500U 4c8t
   - Graphics: Integrated AMD Radeon Vega 8
   - Wifi Card: AX200(TBA)
   - SSD: SN580 512GB
   - Audio: Conexant C8070
2. **macOS Version**: Tested with macOS Monterey.


## Installation Steps
1. Clone or download this repository.
2. Place the `EFI` folder into your bootable USB drive for macOS installation.
3. Boot from the USB drive and install macOS as per standard procedures.
</del>
## Manual Audio Configuration
To enable audio output, the **VoodooHDA** kext must be manually loaded:
1. Download the latest version of **VoodooHDA** from its official source.
2. Disable SIP via recovery
3. Place the kext in the `EFI/OC/Kexts` folder or load it directly using `kextload`:
   ```bash
   sudo kextload /path/to/VoodooHDA.kext
4. add VoodooHDA Panel by clicking on VoodooHDA.prefPane
</del>
## BIOS Settings
- Disable: TPM, Secure Boot, Memory Protection
- Enable: UEFI Only, AMD Virtualization, Hyper Thread

## Further Improvements
~~1. Audio support from AppleALC~~
2. Two-way AirDrop functionality
3. Better battery life
4. Readme in Chinese