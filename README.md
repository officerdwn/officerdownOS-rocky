
  ![officerdownOS logo2](/logo2.png)


![officerdownOS logo](/logo.png)

![License](https://img.shields.io/github/license/officerdwn/officerdownOS-rocky)
![GitHub issues](https://img.shields.io/github/issues/officerdwn/officerdownOS-rocky)
![GitHub pull requests](https://img.shields.io/github/issues-pr/officerdwn/officerdownOS-rocky)
![GitHub stars](https://img.shields.io/github/stars/officerdwn/officerdownOS-rocky?style=social)
![GitHub forks](https://img.shields.io/github/forks/officerdwn/officerdownOS-rocky?style=social)
![Last Commit](https://img.shields.io/github/last-commit/officerdwn/officerdownOS-rocky)
![Language](https://img.shields.io/badge/language-C-blue)
![Platform](https://img.shields.io/badge/platform-x86--64%20BIOS-orange)
[![Website](https://img.shields.io/badge/website-officerdownos.weebly.com-blue?logo=google-chrome)](https://officerdownos.weebly.com)

officerdownOS Rocky
==============
The base for all of officerdownOS and its experiments.

The name
--------
![Rocky](/rocky.png)
This is Rocky. As you can tell, he is very cute. 
I had the idea of the base of officerdownOS being named 
Rocky because yes.
Rocky is a Silky Terrier and is 4 months old as of 
5/27/25 (the release of v1.0.0)
Photo taken 5/25/25.

Dependencies
------------

* nasm
* gcc
* ld
* qemu
* make
* xorriso
* grub-mkrescue

You can run this command on debian based distros to get the dependencies:
  `sudo apt update && sudo apt install -y build-essential gcc-multilib libc6-dev-i386 nasm qemu-system-x86 grub-pc-bin xorriso`

Note: On Debian unstable (sid), use qemu-system-i386 instead of qemu (the meta-package may be removed).

There is also a Nix config available to use, which clones the repo and downloads all dependencies.
This can be found at: https://github.com/officerdwn/officerdownOScompile-nixconfig

Compile & Run
-------------

First you need to compile the kernel with `make`,  Now you are ready to run it with `make run`.
to run on physical hardware run `make iso` and to test the iso in QEMU run `make run iso=1`
Clear your workspace with `make clean`. 

As of 5/2 you can now build the kernel binary on Windows using the Scripts. You can get them here:
https://officerdownos.weebly.com/compile.html
or 
https://github.com/officerdwn/officerdownOS-windowsbuild/


VMware & Physical Hardware
--------------------------
Rocky DOES support physical LEGACY hardware and VMware, 
to run on physical hardware, use a program like rufus to flash 
it as MBR. To run it on VMware give it around a gigabyte of RAM
and 1 GB of storage (because VMware doesn't like 0 GB)
and run it.
I have not tested it on Virtualbox, but im sure it would run 
on it.
NOTE: Use the prebuilt ISO for booting on physical hardware and VMWare.
(or build it and make a GRUB image)
PSA: Physical Hardware booting has had issues with v0.1.4, Just use a VM.



Screenshot
----------

![ScreenShot](/screenshot.png)



