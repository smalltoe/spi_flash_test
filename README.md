# spi_flash_test
This is a repo to figure out issues with SPI flash


This is the result of journalctl -kS -1min



Dec 08 11:00:40 lora kernel: usb 1-1.3: new full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:40 lora kernel: usb 1-1.3: New USB device found, idVendor=cafe, idProduct=4002, bcdDevice= 1.00
Dec 08 11:00:40 lora kernel: usb 1-1.3: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Dec 08 11:00:40 lora kernel: usb 1-1.3: Product: TinyUSB Device
Dec 08 11:00:40 lora kernel: usb 1-1.3: Manufacturer: TinyUSB
Dec 08 11:00:40 lora kernel: usb 1-1.3: SerialNumber: 123456789012
Dec 08 11:00:40 lora kernel: usb-storage 1-1.3:1.0: USB Mass Storage device detected
Dec 08 11:00:41 lora kernel: scsi host0: usb-storage 1-1.3:1.0
Dec 08 11:00:42 lora kernel: scsi 0:0:0:0: Direct-Access     Winbond  Mass Storage     1.0  PQ: 0 ANSI: 2
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: Attached scsi generic sg0 type 0
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] 512 4096-byte logical blocks: (2.10 MB/2.00 MiB)
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Write Protect is off
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Mode Sense: 03 00 00 00
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] No Caching mode page found
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Assuming drive cache: write through
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Attached SCSI removable disk
Dec 08 11:00:42 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=3136, sector_sz=4096)
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 f0 00 00 01 00
Dec 08 11:00:42 lora kernel: scsi_io_completion_action: 6 callbacks suppressed
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 f0 00 00 01 00
Dec 08 11:00:42 lora kernel: blk_print_req_error: 6 callbacks suppressed
Dec 08 11:00:42 lora kernel: I/O error, dev sda, sector 3968 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:42 lora kernel: hwmon hwmon1: Undervoltage detected!
Dec 08 11:00:42 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=704, sector_sz=4096)
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 00 01 00 00 01 00
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 00 01 00 00 01 00
Dec 08 11:00:42 lora kernel: I/O error, dev sda, sector 8 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:42 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1728, sector_sz=4096)
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 ce 00 00 01 00
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:42 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 ce 00 00 01 00
Dec 08 11:00:42 lora kernel: I/O error, dev sda, sector 3696 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:43 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=2496, sector_sz=4096)
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 b6 00 00 01 00
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 b6 00 00 01 00
Dec 08 11:00:43 lora kernel: I/O error, dev sda, sector 3504 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:43 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1344, sector_sz=4096)
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 ab 00 00 01 00
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 ab 00 00 01 00
Dec 08 11:00:43 lora kernel: I/O error, dev sda, sector 3416 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:43 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1472, sector_sz=4096)
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 a4 00 00 01 00
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 a4 00 00 01 00
Dec 08 11:00:43 lora kernel: I/O error, dev sda, sector 3360 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:43 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=2624, sector_sz=4096)
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 8e 00 00 01 00
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:43 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 8e 00 00 01 00
Dec 08 11:00:43 lora kernel: I/O error, dev sda, sector 3184 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:43 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=832, sector_sz=4096)
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 86 00 00 01 00
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 86 00 00 01 00
Dec 08 11:00:44 lora kernel: I/O error, dev sda, sector 3120 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:44 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=704, sector_sz=4096)
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 84 00 00 01 00
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 84 00 00 01 00
Dec 08 11:00:44 lora kernel: I/O error, dev sda, sector 3104 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:44 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:44 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1984, sector_sz=4096)
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 89 00 00 01 00
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 UNKNOWN(0x2003) Result: hostbyte=0x07 driverbyte=DRIVER_OK cmd_age=0s
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 01 89 00 00 01 00
Dec 08 11:00:44 lora kernel: I/O error, dev sda, sector 3144 op 0x0:(READ) flags 0x80700 phys_seg 1 prio class 2
Dec 08 11:00:44 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1472, sector_sz=4096)
Dec 08 11:00:44 lora kernel: sd 0:0:0:0: [sda] tag#0 CDB: opcode=0x28 28 00 00 00 00 7e 00 00 01 00
Dec 08 11:00:45 lora kernel: usb 1-1.3: reset full-speed USB device number 14 using xhci_hcd
Dec 08 11:00:45 lora kernel: sd 0:0:0:0: [sda] Unaligned partial completion (resid=1984, sector_sz=4096)
