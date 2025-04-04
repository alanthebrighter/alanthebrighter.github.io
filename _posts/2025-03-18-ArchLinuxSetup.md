---

layout: post

title: "DOC: First time Setting up Arch Linux"

date: 2025-03-18 1:23:17 -03:00

description: "Setup the Arch Linux distro for multiple purposes that include: Cybersecurity/Ethical Hacking, Data Engineer and analysis, Productivity and Gaming(optional)"

tags: [Arch Linux, Cybersecurity, Ethical Hacking, Data Engineer, Data Analysis, Productivity, Gaming, Coding]

permalink: /posts/ArchLinuxSetup # Custom URL path (optional)

---

Setup the Arch Linux distro for multiple purposes including:  
Cyber-security/Ethical Hacking:  
Data Engineer and Analysis:  
Productivity:  
Gaming(optional):  

---

### 🫠 I gave up -- It's over

I gave up on the idea and migrated to Ubuntu Budgie, as it is simpler in terms of usability, whose objective is to have a system that works quickly as a tool, as a case for study and application in other areas. I found the experience interesting and in the future I plan to go back and try once again to configure an Arch Linux that works stably as I want, but for now, I will stick with Ubuntu and more user-friendly distros.

### 💢 The most painful experience that I already have

Nothing works, everything is broken or in conflict, but I learned something.

If wasn't for the help of multiple AI(ChatGPT, DeepSeek, Claude) to help me solve my problems, I would never have installed this system alone.

- **Unsolved Problem:** Using the mouse Middle click to scroll easily the pages.

#### 🪤 Basic Setup

After Booting USB Flash with UEFI, Ethernet was working, every seemed okay, so I ran: `ping -c 3 google.com`, to test the network, since the network was okay, then `arch install`, to start the simple method of installation, made some basic configs, used recommended partition setup to the storage with BTRFS option. English, US, Brazil Mirror, en_US, UTF-8, systemcmd-bootctl, yes, created a new user with root privileges, desktop, KDE Plasma, sddm, first PulseAudio later changed for PipeWire, Linux, network as same as the USB boot, sao_paulo, true.

![Arch Install Menu](https://blog.desdelinux.net/wp-content/uploads/2022/04/Arch-Install.png)  

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

  

---

  

#### 📦 Installed Packages

- [X] > Google Chrome

- [X] > GitHub Desktop

- [X] > Visual Studio Code

- [X] > MySQL Workbench

- [X] > Discord

- [X] > Web Whatsapp(Website to App)

- [X] > Steam

- [ ] > Notion

- [ ] > Docker

- [ ] > MySQL(Client and Server)

- [ ] > Postman

- [ ] > Ollama

- [ ] > Open-WebUI

- [ ] > Cloud Backup

- [ ] >  Kvantum(For translucent effect)

  

---

  

#### 🔧 Fixed Problems

- [X] > PipeWire-Pulse (Lower volume than normal)

- [X] > PipeWire-Pulse x PulseAudio (Echo cancellation in discord)

- [ ] > Discord (Withe blank screen [Enhanced and Normal])

- [x] > Numlock on Bootup

---

#### 📂 Resources

- [Arch Linux Downloads](https://archlinux.org/download/)

- [USB Flash installation](https://wiki.archlinux.org/title/USB_flash_installation_medium#In_Windows)

- [Arch Linux post install Guide](https://youtu.be/YPrhIfm3VJs)

- [KDE Plasma Ricing Guide (Window scripts, latte dock, wallpaper engine)](https://youtu.be/7tWTagDykiI){:target="_blank"}  

- [Making KDE Plasma Look BEAUTIFUL!](https://youtu.be/R6C-RNhHMrE?si=V6BB8StbT7vvufqT){:target="_blank"}  

- [Searching for Official Packages](https://archlinux.org/){:target="_blank"}  
- [Arch Linux - xinitrc](https://wiki.archlinux.org/title/Xinit#xinitrc){:target="_blank"}  

- [How to Setup Audio on Arch Linux (Pipewire)](https://youtu.be/zmNCi9wqiuU){:target="_blank"}  

- [Upgrade your Terminal](https://youtu.be/80PHRWH84Tc){:target="_blank"}  

- [Fish Shell](https://fishshell.com/){:target="_blank"}  

- [Oh My Zsh](https://ohmyz.sh/){:target="_blank"}  

- [🛠️ Fix "code" fonts and symbols (not only in Discord!) - Arch Linux](https://youtu.be/hTklkv0_s-U){:target="_blank"} 

- [Activating Numlock on Bootup](https://wiki.archlinux.org/title/Activating_numlock_on_bootup){:target="_blank"}  

