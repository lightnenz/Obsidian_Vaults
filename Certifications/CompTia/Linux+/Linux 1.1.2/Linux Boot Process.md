# Linux Boot Process

**UEFI** and **BIOS** are both Firmware that allows the operating system to interact with the hardware of the motherboard and things connected to it. It also determines how the system boots

## UEFI
- **UEFI** stands for **U**nified **E**xtensible **F**irmware **I**nterface
- Its configuration is stored on a partition of a drive
- It supports drives that are bigger than 2tb drives
- Supports things like GPT and ore partitions
- It is newer and has more support
- Systems sometimes call **UEFI BIOS** so that the user understands what they are talking about


## BIOS
- **BIOS** stands for **B**asic **I**nput **O**utput **S**ystem
- It has limited support due to its age
- Configuration is stored on the motherboard itself
- It can only support hard drives up to 2tb

# Boot Sources

## Hardware
- **PXE** (**P**re-boot **E**xecution **E**nvironment) This allows you to boot from a network using an interface like Ethernet
- **USB**(**U**niversal **S**erial **B**us) The OS can be booted via a device connect to **USB** like an external drive or a memory stick
- **Drive** The OS can boot from an internal hard drive. This is usually done after the OS has been installed on the hard drive. Some systems such as servers will still use other options such as USB instead of booting of the Hard drive
## GRUB2
- The Linux **GRUB2**(**GR**and **U**nified **B**ootloader) is a software based bootloader package that takes over after Linux has started booting for the previous hardware bootloaders mentioned before
- **ISO** (**I**dentical **S**torage Image of **O**ptical media) **GRUB2** Allows you to boot to an **ISO** File without needing to burn it onto a USB
- **MEMTEST** is a stripped own operating system that allows you to test ram
- **GRUB2** Also allows you to boot straight to another OS that you might have installed on your system
	- 