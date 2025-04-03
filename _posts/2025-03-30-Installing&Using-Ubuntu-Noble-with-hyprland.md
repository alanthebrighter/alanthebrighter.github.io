---
layout:  post
title: "DOC: Installing and Using Hyprland on Ubuntu"
date: 2025-03-30 09:56:30 -03:00
description: "Installing Hyprland on Ubuntu 24.04 LTS Noble 24.04 LTS"
tags: [Linux, Ubuntu, Hyprland, wayland, Hyprdots, Tyling compositor]
permalink: /posts/UbuntuHyprland  # Custom URL path (optional)
---  
Setting Up Ubuntu Noble 24.04 LTS with Hyprland Using JaKooLit's Script.  
Ubuntu Noble 24.04 LTS is the latest long-term support release, offering stability and performance. If you're looking for a sleek, highly customizable window manager, Hyprland is a fantastic choice.  
I'll walk you through my experience setting up Ubuntu 24.04 with Hyprland using JaKooLit's automated script in this guide. 

---
This script simplifies the installation process, configuring everything from essential dependencies to a well-optimized Hyprland environment. Whether you're a beginner or an experienced Linux user, this setup will help you achieve a modern, stylish, and efficient desktop experience.   
[JaKooLit's Script](https://github.com/JaKooLit/Ubuntu-Hyprland)


![Desktop day 01](https://github.com/user-attachments/assets/a53b8e51-6bd4-465c-85ec-5a196c059e50)

## 💬 Some useful shortcuts

<style>
  .custom-table {
    width: 100%;
    border-collapse: collapse;
  }
  .custom-table th, .custom-table td {
    border: 1px solid #ddd;
    padding: 8px;
  }
  .custom-table th {
    background-color: #f2f2f2;
    color: #333;
    text-align: left;
  }
  .custom-table tr:nth-child(even) {
    background-color: #f9f9f9;
  }
  .custom-table tr:hover {
    background-color: #f1f1f1;
  }
</style>

<table class="custom-table">
  <thead>
    <tr>
      <th>Key Combination</th>
      <th>Action</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Super + Enter</td>
      <td>Launch terminal emulator (Kitty)</td>
    </tr>
    <tr>
      <td>Super + D</td>
      <td>Launch application launcher (Rofi)</td>
    </tr>
    <tr>
      <td>Super + Q</td>
      <td>Close active/focused window</td>
    </tr>
    <tr>
      <td>Super + Shift + E</td>
      <td>Open KooL Hyprland Settings</td>
    </tr>
    <tr>
      <td>Super + E</td>
      <td>Launch file manager (Thunar)</td>
    </tr>
    <tr>
      <td>Super + Shift + F</td>
      <td>Toggle fullscreen for the active window</td>
    </tr>
    <tr>
      <td>Super + Spacebar</td>
      <td>Toggle floating mode for the active window</td>
    </tr>
    <tr>
      <td>Super + Alt + Spacebar</td>
      <td>Toggle floating mode for all windows</td>
    </tr>
    <tr>
      <td>Super + H</td>
      <td>Launch help file with keybinding hints</td>
    </tr>
    <tr>
      <td>Super + Shift + K</td>
      <td>Search configured keybindings via Rofi</td>
    </tr>
  </tbody>
</table>

For a complete list of shortcuts and further information: [Keybinds section of JaKooLit's Hyprland-Dots Wiki](https://github.com/JaKooLit/Hyprland-Dots/wiki/Keybinds).

## 💬 Some useful tips
### Recovering Ubuntu and Windows Boot Issues + Hyprland Login Tip  

Recently, I encountered some issues while trying to restore GRUB to recognize both Ubuntu and Windows. The problem started when Windows failed to create the EFI partition correctly. In an attempt to fix it, I booted from a Windows USB recovery drive. However, after that, when I tried to return to Ubuntu, it would start booting, but the screen would go black, and my monitor would display a "no signal" message.  

Not knowing what to do, I decided to format Ubuntu and reinstall everything from scratch using the [JaKooLit Hyprland setup script](https://github.com/JaKooLit/Ubuntu-Hyprland).  

However, this morning, I encountered another issue: after suspending my system, it prompted me for a password upon waking up. No matter what I pressed, I couldn't type my password or exit the lock screen.  

To resolve this, I used the following key combinations:  

- **CTRL + ALT + F3** (switch to a TTY terminal)  
- **CTRL + ALT + F2** (to access another terminal if needed)
From there, I logged in with my username and password and manually started Hyprland by running:  

```sh
Hyprland 
```

- Nevermind, i just needed to press **ALT + TAB**, to start typing my password. (I'm learning, calm down.)

### Changing mouse/mice sensitivity
SUPER + SHIFT + E (KooL Hyprland settings menu) -> View/Edit user settings  
**Change**  
```text
general {
  sensitivity=.285 # This one
  apply_sens_to_raw=0 # This one is for acceleration, I think.
  resize_on_border = true
  layout = dwindle
} 
```
## Waybar, Kitty, Oh-My-Zsh, Fastfetch  

I spent some time customizing Hyprland, Waybar, terminal (Kitty/Zsh), and I learned some pretty interesting things along the way.  

### Fastfetch  
I wanted to modify the Fastfetch configuration to display a custom image, inspired by **@DIMFLIX** and his **hyperdots meowrch**. It seemed simple, but I got lost for almost two hours before figuring out what was happening. In the end, I made it work!  

### Zsh & Kitty  
Besides Fastfetch, I also wanted to change the terminal theme. While exploring **hyperdots**, I remembered that `SUPER + SHIFT + E` brings up a lot of configurations, including themes for Kitty. Kitty already has a wide variety of themes, but I wanted to create my own.  
I navigated to the Kitty themes folder, copied a **template**, and started modifying the colors. The result? **It broke everything!** 😂 Nothing new, haha. But then I used another theme from the folder as a base, and this time it worked without issues.  

However, my Zsh still looked a bit dull for my taste. I searched for some themes and remembered that many I used in the past were for **Oh-My-Posh** and **Fish**. In the end, I picked a simple theme called **"Ultima"**—basic but clean.  

### Waybar  
Customizing Waybar was relatively simple, but there are still some things I want to tweak. Right now, I'm switching between random dark and light themes every time I click the theme switch button. In the future, I plan to modify the color scheme and decide whether the entire bar should be solid or just the icon areas, keeping the rest transparent. I haven't experimented with this yet, but it's something I want to try.  

I also found out how to display the calendar by hovering over the Waybar! I just added it to the same section where the clock is displayed.  


### Steam & Hyprland Bugs  
I'm also curious about why Steam always opens on workspace 5 and Chrome on workspace 2. If I try to move it from there, it starts bugging out and constantly switching workspaces whenever I hover over the menus. I'm not sure if this is a bug with the application or with Hyprland. Additionally, several other visual glitches occur frequently. They are not annoying enough to stop me from using Hyprland, but I still want to see if it's possible to fix them. 

### Workspace Memory Feature  
I think it would be interesting if every time an application is opened, it remembers the workspace where I placed it and continues to open in that workspace, even if I switch to another one in the meantime. This way, the application would not pop up in my current workspace, disrupting my workflow. Instead, it would open in the background in the designated workspace, allowing me to continue working smoothly and check on it later when needed.  

### Floating Pop-ups & Chrome Behavior  
I still haven't figured out why some applications open in floating pop-up mode on the screen. For example, the calculator doesn't always need to be centered as a pop-up, since it can sometimes block information from another application that I'm trying to sum up. Additionally, Chrome always opens on **workspace 2**, and even when it's moved to **workspace 1**, its pop-ups still appear on **workspace 2**. I don't know if this is a Hyprland issue or just how these applications behave by default, but I'd like to understand if there's a way to fix this.  

### Startup Configuration Goals  
I want to set specific applications to open in predefined workspaces on startup without breaking any other configurations:  
- **Chrome** should open where I last left it, preferably in **workspace 1**.  
- **Station** (my web app manager for WhatsApp Web and Instagram) should always start in **workspace 3**.  
- **Zen Browser** (which I'm currently using to access Notion) should always launch in **workspace 2**.  
This way, I can ensure my workflow remains smooth, and applications don’t randomly open in unexpected places.


![image](https://github.com/user-attachments/assets/a8a26566-8db5-4ced-8260-c72c0686fa90)  

For now, that's all! I still want to tweak/create many configurations for Hyprland. I'm learning more about how it works, how **Linux** works, and exploring **@JaKooLit**'s Hyprland setup.

![Desktop day 4](https://github.com/user-attachments/assets/03590393-17ee-4d56-ab14-20ddf8ee5ac2)

