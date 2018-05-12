---
layout: post
title: How to Numix
categories: blog
tags: ['numix','linux','ubuntu']
excerpt: 'Remix your Ubuntu desktop with Numix!'
date: May 12, 2018
author: self

---

It's been a long time since we met and now it's time for business.In this blog post I will shed light upon how to install and apply the numix theme for Ubuntu.

**Disclaimer: I am not a subject expert on Ubuntu and I am
sharing my findings as I learn more about this myself.**

Numix is available for all major Linux distributions and desktop environments for e.g., GNOME, Cinnamon etc. Numix is the default theme of Arch based Linux distribution, Antergos.

## Prerequisites

1.Ubuntu 14.04 or Ubuntu 16.04 and nothing else.
2.Read the first requirement again.

## Cooking phase

The Numix theme is available in the official Numix PPA. Open the terminal and type the following commands

```
sudo add-apt-repository ppa:numix/ppa
```

Update the packages list!
    
```
sudo apt-get update
```
    
Install the numix theme and icons

```
sudo apt-get install numix-gtk-theme numix-icon-theme-circle
```

Slow down , the cooking is not complete yet. It's time to add the much awaited cursor themes.

Check out this link [here](https://github.com/uloco/numix-cursor) for installing the Numix themed cursor icons

## Tweak Phase

The cooking phase is complete. Now how are you going to apply the theme and icons to your Ubuntu desktop?

The tweak tool provides an opportunity to apply the GTK themes for Ubuntu desktop environments.It offers a variety of options along with this like customizing the launcher!

Install the tweak tool by typing out the following command in the terminal.

```
 sudo apt-get install unity-tweak-tool
```    
    
If you are using GNOME, then install Gnome Tweak Tool with the following command:

```
sudo apt-get install gnome-tweak-tool
```    
    
After installing the tweak tool :

1. Click and open theme in the appearances tab
2. Select Numix in the theme tab
3. Select Numix-circle in the icons tab
4. Select Numix-cursor in the cursor tab

Voila , your Numix-themed Ubuntu desktop is ready.But there is yet another catch.During the initial booting of the Ubuntu the login screen displays the default unity theme eventhough we have changed the theme to Numix.This is due the fact that this part of appearance is handled by the unity greeter.We have to install yet another application to change this screen in accordance with the Numix theme or any other GTK theme.Unfortunately , the application is available in the software centre of Ubuntu 16.04 . I haven't found the solution for 14.04

## Greeter Phase

Search for lightdm gtk+ greeter settings in the Ubuntu software centre and install it.Open the application.

1. Select theme as Numix.
2. Select icons as Numix-Circle.
3. Select image as the background image you want.
4. Click save and press reload to reload the display server! 
5. Reboot the system :D

You can find my desktop wallpaper [here](https://drive.google.com/open?id=10KcFLYjj4jT1lFZpFkYnQf9AEEtzTYvX)

That's all for today.See ya soon!