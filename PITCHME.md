---?image=assets/images/gitpitch-audience.jpg
@title[Platform Build Lab]
<br><br><br><br><br>
## <span class="gold"   >UEFI & EDK II Training</span>

#### UEFI Aware Operating System 

<br>
<span style="font-size:0.75em" ><a href='http://www.tianocore.org'>tianocore.org</a></span>
Note:
  PITCHME.md for UEFI / EDK II Training  UEFI Shell Application

  Copyright (c) 2018, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



---  
@title[Lesson Objective]
<BR>
### <p align="center"<span class="gold"   >Lesson Objective </span></p><br>

<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
<br>
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How the OS and UEFI Work together </span><br>
 @fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the UEFI Requirements for UEFI aware OS</span><br>
 @fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How Secure Boot Fits with UEFI</span> <br>
 @fa[certificate gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;What about MM (Formerly Known as SMM)</span> <br>
 @fa[certificate gp-bullet-ltgreen]<span style="font-size:0.9em">&nbsp;&nbsp;What about coreboot?</span> 


---?image=assets/images/binary-strings-black2.jpg
@title[UEFI Shell Overview Section]
<br><br><br><br><br>
### <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UEFI Aware OS Requirements</span>
<span style="font-size:0.9em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Common Requirements</span>
 
---?image=/assets/images/slides/Slide4.JPG
@title[UEFI Operating Systems]
### <p align="right"><span class="gold" >UEFI Operating Systems</span></p>

Note:
Many OS already use UEFI to boot from and use UEFI Services


---?image=/assets/images/slides/Slide6.JPG
<!-- .slide: data-transition="none" -->		 
@title[UEFI Boot Flow review]
<p align="right"><span class="gold" > UEFI - PI & EDK II Boot Flow </span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>

Note:
SEC Function <Br>

Review -Boot Execution Flow

+++?image=/assets/images/slides/Slide7.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 02]
<p align="right"><span class="gold" > UEFI - PI & EDK II Boot Flow </span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow
 

+++?image=/assets/images/slides/Slide8.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 03]
<p align="right"><span class="gold" > UEFI - PI & EDK II Boot Flow </span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow
 

+++?image=/assets/images/slides/Slide9.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 09]
<p align="right"><span class="gold" > UEFI - PI & EDK II Boot Flow </span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow

Boot to OS with UEFI Services available


---?image=/assets/images/slides/Slide11.JPG
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
 
Note:
- What is the list of things you need to have in the BIOS/ FW?
- UEFI drivers for boot devices and console – storage devices / 
- UEFI loader need / Elilo for Linux - / RH published need to be there
  - For windows 
  - Transfers con
- UEFI installer –  - Requirements WIN has this so far
- Disk partition and Disk formats - need GPT  / FAT32 disk format
- Firmware requirements
- Boot manager
- BIOS Setup
- Nvram Large enough to store device path

- After installation, set boot path to boot to OS as default system behavior

 
+++?image=/assets/images/slides/Slide12.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements 02]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
  
Note:
 

+++?image=/assets/images/slides/Slide13.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements 03]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
  
Note:
 
+++?image=/assets/images/slides/Slide14.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements 04]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
  
Note:
 
+++?image=/assets/images/slides/Slide15.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements 05]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
  
Note:
 
+++?image=/assets/images/slides/Slide16.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI OS Requirements 06]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
  
Note:

- What is the list of things you need to have in the BIOS/ FW?
- UEFI drivers for boot devices and console – storage devices / 
- UEFI loader need / Elilo for Linux - / RH published need to be there
  - For windows 
  - Transfers con
- UEFI installer –  - Requirements WIN has this so far
- Disk partition and Disk formats - need GPT  / FAT32 disk format
- Firmware requirements
- Boot manager
- BIOS Setup
- Nvram Large enough to store device path

- After installation, set boot path to boot to OS as default system behavior
 
---?image=/assets/images/slides/Slide18.JPG
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes ]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>

Note:
Make sure the “class” terminology is understood here before moving on

### Classes 0-2:
- Limited Benefits
- OEMs/ODMs Internal
- Development Optimization
  -  & Code Organization

### Class 3+
- Full Benefits
- UEFI Innovation
- Performance
- Extensibility




+++?image=/assets/images/slides/Slide19.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 02]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:


+++?image=/assets/images/slides/Slide20.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 03]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:

+++?image=/assets/images/slides/Slide21.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 04]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:


+++?image=/assets/images/slides/Slide23.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 05]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:


+++?image=/assets/images/slides/Slide24.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 06]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:

+++?image=/assets/images/slides/Slide25.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 07]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">UEFI System Classes&nbsp;&nbsp;</span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


Note:
Make sure the “class” terminology is understood here before moving on

### Classes 0-2:
- Limited Benefits
- OEMs/ODMs Internal
- Development Optimization
  -  & Code Organization

### Class 3+
- Full Benefits
- UEFI Innovation
- Performance
- Extensibility

---?image=/assets/images/slides/Slide27.JPG
<!-- .slide: data-transition="none" -->
@title[Required UEFI Drivers: OS Install & Boot]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">Required UEFI Drivers:&nbsp;&nbsp;</span><span style="font-size:0.8em" ><font color="#FFC000">OS Install & Boot<font></span></p>

Note:
- Boot Device: hard drive controller, USB, RAID, Fiber Channel, network, etc. 
- Console Output: Graphics Output Protocol (GOP) or Serial Console (COM port)
- Console Input: Keyboard, Mouse, Touch Screen or Serial Console (COM)
- NVRAM Driver – store boot entry for OS in flash or other NVRAM (not part of boot disk partition)



+++?image=/assets/images/slides/Slide28.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Required UEFI Drivers: OS Install & Boot 02]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">Required UEFI Drivers:&nbsp;&nbsp;</span><span style="font-size:0.8em" ><font color="#FFC000">OS Install & Boot<font></span></p>

Note:


+++?image=/assets/images/slides/Slide29.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Required UEFI Drivers: OS Install & Boot 03]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">Required UEFI Drivers:&nbsp;&nbsp;</span><span style="font-size:0.8em" ><font color="#FFC000">OS Install & Boot<font></span></p>

Note:


+++?image=/assets/images/slides/Slide30.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Required UEFI Drivers: OS Install & Boot 04]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436">Required UEFI Drivers:&nbsp;&nbsp;</span><span style="font-size:0.8em" ><font color="#FFC000">OS Install & Boot<font></span></p>

Note:
- Boot Device: hard drive controller, USB, RAID, Fiber Channel, network, etc. 
- Console Output: Graphics Output Protocol (GOP) or Serial Console (COM port)
- Console Input: Keyboard, Mouse, Touch Screen or Serial Console (COM)
- NVRAM Driver – store boot entry for OS in flash or other NVRAM (not part of boot disk partition)


---
@title[UEFI OS Loader/Installer]
#### <p align="right"><span class="gold" >UEFI OS Loader</span></p>
@fa[circle gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;OS install process includes UEFI loader<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span style="font-size:0.7em"><font face="Courier New" color="#FFFF00">/efi/boot/bootx64.efi    /efi/redhat/grub.efi</font></span><br>
@fa[circle gp-bullet-gold]<span style="font-size:0.9em">&nbsp;&nbsp;Call UEFI boot & runtime services to start OS</span> <br>
@fa[circle gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Exit UEFI Boot Services</span><br>
@fa[circle gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Transfer control to native OS</span><br>
#### <p align="right"><span class="gold" >UEFI OS Installer</span></p>
@fa[circle gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;Discover UEFI storage devices</span> <br>
@fa[circle gp-bullet-gold]<span style="font-size:0.9em">&nbsp;&nbsp;Setup storage device: GPT w/ FAT32 boot partition</span> <br>
@fa[circle gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Create boot variable &nbsp;&nbsp;<font face="Courier New" color="#FFFF00">BootXXXX</fon></span><br>

Note:

#### WHICH DRIVERS?

All UEFI OS’s require that firmware contain UEFI drivers for Boot devices and console 
– mass storage device – or LAN Stack for PXE
–    Boot devices: hard drive controller, usb, raid, fiber channel etc. 
–     Console : GOP or UGA, keyboard (ps2 or usb), mouse (usb) or serial port (some way to control the system on install) 
–   alter the boot opt for the loader
– 	Some way of interacting with user during OS installation and a boot device to store the OS
    – NVRAM driver – boot entry for OS must be stored in flash or some other nonvolatile device that is not part of the OS disk storage – Device path where the boot device is located is stored in NVRAM.
  
– Firmware must contain UEFI drivers for boot devices (OS storage) and console (user interaction)



#### As seen on the SLIDES:
– OS install process will install a UEFI loader (.efi)
– Example: /efi/boot/bootx64.efi, /efi/redhat/grub.efi
– UEFI loader will …
– Call UEFI boot & runtime services to start the OS
– Exit UEFI boot services (OS uses runtime services)
– Transfer control to native OS
– UEFI OS installer must …
– Discover UEFI storage devices
– Setup storage device (GPT w/ FAT32 boot partition)
– Install UEFI loader & create boot variable (BootXXXX)

---?image=/assets/images/slides/Slide33.JPG
@title[Disk Partition and Format]
<p align="right"><span class="gold" >Disk Partition and Format</span></p>


Note:

- UEFI OS requires GPT partitioned disks
- One partition must be formatted FAT32
- “Service partition” for the OS boot loader
- Under /EFI/BOOT or /EFI/osname directory
- Boot0000 entry points to OS loader (.efi)


- Disk partition and Format
- UEFI requires disks be partitioned GPT – May need to wipe the drive to re-partition for GPT
On one of the partitions there must be one formatted FAT.
On the Fat partition under /EFI/boot/* the UEFI os loader must be installed.
Os loader needs to be here

- Question – boot to EFI shell with default – x64 – EFI Shell is not part of the UEFI spec but can be loaded separately. The UEFI Spec section 3 has Boot manager section. A UEFI OS will have a EFI appl that will be the OS loader.

- Can have mult partition for multi-boots on the disk – example – one for windows – one for Linux

-    Windows may have issues with EXT partitions – so there maybe some order of install – 
- Boot manager required in UEFI spec – 1st boot option could be boot to Windows Boot Manager on Windows hard disk 

- There can be mult boot option


---?image=assets/images/binary-strings-black2.jpg
@title[Security with UEFI Section]
<br><br><br><br><br>
## <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Security with UEFI</span>
<span style="font-size:0.9em" > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;How does UEFI  ensure the Operating System is trusted?</span>


---  
@title[Summary]
<BR>
### <p align="center"><span class="gold"   >Summary </span></p><br>
<br>
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How the OS and UEFI Work together </span><br>
 @fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the UEFI Requirements for UEFI aware OS</span><br>
 @fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How Secure Boot Fits with UEFI</span> <br>
 @fa[certificate gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;What about MM (Formerly Known as SMM)</span> <br>
 @fa[certificate gp-bullet-ltgreen]<span style="font-size:0.9em">&nbsp;&nbsp;What about coreboot?</span> 

 

---?image=assets/images/gitpitch-audience.jpg
@title[Questions]
<br>
![Questions](/assets/images/Questions.png =10x) 


---?image=assets/images/gitpitch-audience.jpg
@title[Logo Slide]
<br><br><br>
![Logo Slide](/assets/images/TianocoreLogo.png =10x)


---
@title[Acknowledgements]
#### <p align="center"><span class="gold"   >Acknowledgements</span></p>

```c++
/**
Redistribution and use in source (original document form) and 'compiled' forms (converted
to PDF, epub, HTML and other formats) with or without modification, are permitted provided
that the following conditions are met:

Redistributions of source code (original document form) must retain the above copyright 
notice, this list of conditions and the following disclaimer as the first lines of this 
file unmodified.

Redistributions in compiled form (transformed to other DTDs, converted to PDF, epub, HTML
and other formats) must reproduce the above copyright notice, this list of conditions and 
the following disclaimer in the documentation and/or other materials provided with the 
distribution.

THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR IMPLIED 
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL TIANOCORE PROJECT BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, 
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF ADVISED OF THE POSSIBILITY 
OF SUCH DAMAGE.

Copyright (c) 2018, Intel Corporation. All rights reserved.
**/

```
