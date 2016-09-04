---
layout: post
title: A Pure WinAVR Setup
description: "A Pure WinAVR Setup"
modified: 2014-07-31
tags: [winavr, arduino, atmel, atmel2560, avrispmkii, setup]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true

share: true
---

This describes how to use WinAVR with the AVRISP mkII Programmer *without* using Atmel Studio. This has been tried on Windows 7.

1. Install WinAVR from [SourceForge](http://sourceforge.net/projects/winavr/files/)
2. Download libusb-win32 from [SourceForge](http://sourceforge.net/p/libusb-win32/wiki/Home/)
3. Unzip and open the libusb-win32-bin-1.2.6.0/bin/ folder
4. Run inf-wizard.exe with the AVRISP mkII Programmer plugged in
5. Follow the instructions and allow the wizard to do the driver installation for you.
