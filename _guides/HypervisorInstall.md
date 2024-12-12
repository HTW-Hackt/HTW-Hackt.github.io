---
layout: post
title: Installing a Hypervisor
author: h474rd
date: 6.Dec 2024
description: Installing a hypervisor is the first step to setting up virtual machines or even a whole lab. This guide will give you some basics on hypervisors and show you how to set one up to start your hacking journey.
---

# What's a VM and what's a hypervisor?

VM, short for Virtual Machine, is a term for an emulated Operating System (OS). Usually OSs are installed an devices such as laptops, servers or your smartphone. They provide an abstraction layer between your hardware and your applications so no application has to deal with the configuration or detailed usage of you harddrive, keyboard or other components. A Hypervisor offers a way to run an OS on software instead of hardware and a VM is software system consisting of the OS you wnat tu run and some configurations which hardware should be emulated.

There's two types of hypervisors:
- **Type 1** Runs directly on the hardware (bare-metal) and manages guest operating systems without requiring a host OS
- **Type 2** Runs on top of a host operating system, using it as an intermediary to manage guest operating systems.

So for out usecase we will only deal with Type 2 hypervisors, since we don't want to replace your running OS.

# Hypervisor Options

Depending on your system ressources and OS there are different hypervisor solutions. We usually recommend [VirtualBox](https://www.virtualbox.org), since it is freely available and most of us can assist in troubleshooting. *VirtualBox* will run on current Windows and Linux systems. For non-beginner linux users *qemu* and fronends such as *virt-manager* might be prefered. On Apple Silicon systems we recommend [UTM](https://mac.getutm.app), altough our assistance in troublshooting here is limited.

## Prerequisites

You need to activate virtualisation in your BIOS or UEFI. How this is done depends on your system.
Here are a few ressorces depending on your manufacturer:
- [Lenovo](https://support.lenovo.com/de/en/solutions/ht500006-how-to-enable-virtualization-technology-on-lenovo-computers)
- [Asus](https://www.asus.com/support/faq/1045141/)
- [Dell](https://www.dell.com/support/kbdoc/en-us/000195978/how-to-enable-or-disable-hardware-virtualization-on-dell-systems)

Note: These might be out of date of different depending on your system. Good opportunity to improve your [Google-Fu](https://tryhackme.com/r/resources/blog/google-fu), altough a simple search should be sufficient.

## VirtualBox

You can obtain *VirtualBox* from their [official Website](https://www.virtualbox.org/wiki/Downloads) or depending on your Linux distribution via your package manager.

On windows follow the [Official Install Instructions](https://www.virtualbox.org/manual/topics/installation.html#installation_windows) or any of the various [Inofficial Install Instructions](https://www.wikihow.com/Install-VirtualBox), which tend to be easier to understand.

On linux the install might be slightly different depending on your distribution, here's the one for [Arch](https://wiki.archlinux.org/title/VirtualBox#Installation_steps_for_Arch_Linux_hosts).

## UTM

*UTM is a full featured system emulator and virtual machine host for iOS and macOS. It is based off of QEMU. In short, it allows you to run Windows, Linux, and more on your Mac, iPhone, and iPad.* ~[UTM](https://docs.getutm.app/#what-is-utm)

The install process is straight forward, see: [installation instructions](https://docs.getutm.app/installation/macos/#installation)
