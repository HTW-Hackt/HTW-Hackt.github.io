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

## VirtualBox

- on windows

- on linux

## UTM
