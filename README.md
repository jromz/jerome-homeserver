# Ubuntu Linux Home Server

A personal Ubuntu-based home server built from spare desktop hardware. This system is primarily operated headlessly via SSH, with XRDP set up as an emergency backup GUI.

---

## Overview

Services:

* Modded Minecraft server hosting
* Network-Attached Storage (NAS)
* Multiple Virtual Machines (VMs) for coursework and enterprise network simulations

Key goals:
* Learn more about Linux system administration
* Testing and evaluating services that may be useful in daily life or future projects
* Becoming more fluent and confident with the command line interface (CLI)
* Gaining hands-on experience with networking, storage, security, and server operations


The primary purpose of this server is to act as a hands-on learning environment.

---

## System Information

* **Operating System:** Ubuntu Linux Server
* **Hardware:** Repurposed desktop components
* **Primary Interface:** Command Line Interface (CLI)
* **Secondary Interface:** XRDP (GUI access only when required)

---

## Hardware Specifications

### CPU

* **Intel Core i5-8400T**

  * 6 cores / 6 threads
  * Integrated Intel UHD Graphics
  * Pulled from an all-in-one PC after motherboard failure
  * Original AIO display panel was later converted into a standalone monitor

### Memory

* **32 GB DDR4 (G.Skill Ripjaws)**

  * Rated at 3600 MHz
  * Operating at **2666 MHz** due to motherboard chipset limitations

### Motherboard

* **ASRock H370M-HDV**

  * LGA1151 socket
  * Consumer-grade board repurposed for 24/7 homelab use

### Storage

* **2 × 256 GB SSDs**

  * One dedicated to the Ubuntu Linux OS
  * Second SSD used for applications, scratch space, or future expansion

* **2 × 1 TB HDDs**

  * NAS data
  * Media libraries
  * Game server assets

---

## Network Configuration

* **DHCP Reservation & Static IP Mapping**

  * Configured on the router to ensure a consistent internal IP address
* **Persistent Storage Mounting**

---

## Remote Access & Security

### Local Network Access

* **OpenSSH**

  * Primary management method
  * Key-based authentication

### Remote / Internet Access

* **Tailscale**

  * Encrypted mesh VPN
  * Secure SSH access without exposing ports to the public internet

### GUI Access (Backup use)

* **XRDP**

---

## Services & Workloads

### Minecraft Server

* Modded Minecraft server
* Publicly accessible via tunneling/proxy software
* Avoids exposing the home network's public IP address

### NAS (File Storage)

* **Samba (SMB)** for network file sharing
* Credential-based authentication
* Accessible from Windows and Linux clients

### Virtualization

* **VMware**
* Used for:

  * College coursework
  * Enterprise network simulations
  * Testing isolated environments

---

## Server Management & Tooling

* **Tmux (Terminal Multiplexer)**

  * Manages long-running processes and persistent sessions
* **htop**

  * Real-time system and resource monitoring
* **SFTP / PSCP**

  * Secure file transfers to and from Windows systems

---

## Operational Philosophy

* CLI-first, minimal GUI dependency
* Security-conscious remote access
* Designed for learning, experimentation, and real-world IT practice

---

## Notes

* XRDP is intentionally kept disabled unless needed
* Most services are designed to recover cleanly after reboots
* The system doubles as both a production-style server and a learning platform

---

## Development Progress

For those interested in the detailed task tracking and ongoing experiments, a **Kanban project board** is available:  

[Project Board](https://github.com/users/jromz/projects/4)
