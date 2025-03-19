---
layout:  post
title: "DOC: First time Setting up Arch Linux"
date: 2025-03-18 1:23:17 -03:00
description: "Setup the Arch Linux distro for multiple purposes that includes: Cybersecurity/Ethical Hacking, Data Engineer and analysis, Productivity and Gaming(optional)"
tags: [Arch Linux, Cybersecurity, Ethical Hacking, Data Engineer, Data Analysis, Productivity, Gaming, Coding]
permalink: /posts/ArchLinuxSetup  # Custom URL path (optional)
---


### ☑️ Main goal
Setup the Arch Linux distro for multiple purposes that includes:  
Cybersecurity/Ethical Hacking:  
Data Engineer and analysis:  
Productivity:  
Gaming(optional):  


### 💢 The most painful experience that already have
Nothing works, everything is broken or in conflict, but I learned some thing.
If wasn't for the help of multiples AI(ChatGPT, DeepSeek, Claude) to help me solve my problems, I would never installed this system alone. 
- **Unsolved Problem:** Using Middle click mouse to scroll easily the pages.
#### 🪤 Basic Setup
After Booting USB Flash with UEFI, Ethernet was working, every seems okay, so I ran: `ping -c 3 google.com`, to test the network, since network was okay, then `arch install`, to start the simple method of installation, made some basic configs, used recommended partition setup to the storage with BTRFS option. English, US, Brazil Mirror, en_US, UTF-8, systemcmd-bootctl, yes, created a new user with root privileges, desktop, KDE Plasma, sddm, first PulseAudio later changed for PipeWire, linux, network as same as the usb boot, sao_paulo, true. 
![Arch Install Menu](https://diolinux.com.br/wp-content/uploads/2022/11/instalar-o-arch-linux-menu-inicial-padrao-760x569.jpg)
That was my Installation configs.

#### 👾 Pacman Basics
`pacman -Syu` - Update entire system  
`pacman -Syy` - Force refresh package databases  
`pacman -S package_name` - Install a package  
`pacman -R package_name` - Remove a package  
`pacman -Rs package_name` - Remove a package and its dependencies   
`pacman -Ss keyword` - Search for packages  
`pacman -Qi package_name` - Display information about a package  
`pacman -Qdt` - List orphaned packages  
`yay -S package_name` - Install from AUR  
`yay -Syu` - Update system including AUR packages  

#### 🕹️ Installing yay
1. Log in as a **sudo user**
2. **Update** the system packages
3. Install the **base-devel package**
4. Install **git**
5. Clone the **yay git repository**
6. Change the **ownership** of the yay directory to the **sudo user**
7. Navigate into the **yay directory**
8. Build the package from **PKGBUILD**
- Detailed steps 
    - `sudo pacman -Syy`
    - `sudo pacman -S --needed base-devel`
    - `sudo pacman -S git`
    - `sudo git clone https://aur.archlinux.org/yay.git`
    - `cd yay`
    - `makepkg -si`

> You can use yay to: 
> - Install packages from the AUR
> - Upgrade all packages on your system
> - Include development packages during the upgrade
> - Remove a package
> - Clean up unwanted dependencies
> - Print system statistics
> - Generate a development package database
> - Check for development package updates  
You can search for applications with yay by providing a search clue. Yay will search the AUR and return a list of results.

#### 📦 Installed Packages
- [X] Google Chrome
- [X] GitHub Desktop
- [X] Visual Studio Code
- [X] MySQL Workbench
- [X] Discord
- [X] Web Whatsapp(Website to App)
- [X] Steam
- [ ] Notion
- [ ] Docker
- [ ] MySQL(Client and Server)
- [ ] Postman
- [ ] Ollama
- [ ] Open-WebUI
[ ] Cloud Backup
- [ ] 
---
#### 📂 Resources
- [Arch Linux Downloads](https://archlinux.org/download/)  
- [USB Flash installation](https://wiki.archlinux.org/title/USB_flash_installation_medium#In_Windows)  
- [Arch Linux post install Guide](https://youtu.be/YPrhIfm3VJs)  
- [KDE Plasma Ricing Guide (Window scripts, latte dock, wallpaper engine)](https://youtu.be/7tWTagDykiI)  
- [Making KDE Plasma Look BEAUTIFUL!](https://youtu.be/R6C-RNhHMrE?si=V6BB8StbT7vvufqT)  
- [Searching for Official Packages](https://archlinux.org/)
