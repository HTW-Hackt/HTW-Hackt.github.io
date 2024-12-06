---
layout: default
title: Installing Kali Linux
author: h474rd
date: 6.Dec 2024
description: After successfully installing a hypervisor the next step is to install kali linux, a Linux distribution specifically built for security hobbiests and professionals. Kali bundles lots of commonly used tools, this guide will show you how to set it up locally.
---

![Kali Linux Logo](./img/kali-logo.svg "Kali Linux Logo")

# Requierements

You need to have a hypervisor installed. We usually recomend [VirtualBox](https://www.virtualbox.org), on apple silicon you can use [utm](https://mac.getutm.app).

There are different approaches to installing kali. Each comes with their respective pros and cons, also detaile on [kali.org](https://www.kali.org/get-kali), TL;DR:

| Install method | Pros | Cons |
|:---|:---|:---|
| Manual live install | No network connection requiered. | Larger install file and initial download. |
| Manual network install | Smaller install file and initial download. | Requieres network connection for the install. |
| Premade VM | Easier setup and usually better out of the box. | You'll miss the basics. |

# Installation

Depending on your system you will either need the 64-bit or ARM64 version, each refering to you systems CPU instruction set.
64-bit is intended for the [x86-64](https://en.wikipedia.org/wiki/X86) instruction set, common in most windows or *nix systems.
Apple silicon, as well as RaspberryPis and some mobile CPUs use the [ARM64](https://en.wikipedia.org/wiki/ARM_architecture_family) instruction set.

Some hypervisors or hypervisor configurations allow to emulate instructions sets, altough this is out of scope for this guide.

## Manual Install

The **live install** image can be downloaded from [kali.org](https://www.kali.org/get-kali) and is intended for offline installations. It can also be used for live boots, for this usecase you want to consider the **everything** option which is quiete big but ships with all available tooling, this will requiere a torrent download.
Once the torrent is downloaded the `.iso` can be used to install kali in a VM.

The **network install** image con also be donwloaded from [kali.org](https://www.kali.org/get-kali) and is intended for online installations, meaning you system will requiere an internet connection. Thi initially donloaded `.iso` file is smaller but during installation the choosen packages will be donwloaded.

To install kali you can follow the official documentation to:

- [setup kali in virtualbox](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/)
- [install kali](https://www.kali.org/docs/installation/hard-disk-install/)
- [install guest tools](https://www.kali.org/docs/virtualization/install-virtualbox-guest-additions/)

- [setup kali in utm](https://www.kali.org/docs/virtualization/install-utm-guest-vm/)
- [install kali](https://www.kali.org/docs/installation/hard-disk-install/)
- you can install the guest tools with `$ sudo apt install qemu-guest-agent spice-vdagent` in your kali VM

Things to consider:

- using english will be more practical for troubleshooting
- your keyboard layout should match your actual keyboard
- if you're running kali you will most likely not use your host or other VMs, therefor no need to be greedy with system ressources

## Premade VM

Kali also comes in a preconfigured VM, ready to downlaod and import in your hypervisor of choice.
For VirtualBox follow the this guide: [Import Pre-Made Kali VirtualBox VM](https://www.kali.org/docs/virtualization/import-premade-virtualbox/)
