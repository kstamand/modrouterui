# ModrouterUI - Customize Asuswrt-Merlin router Web UI to hide unused / unwanted tabs

This script has been tested on a GT-AX6000, running Asuswrt-Merlin 3006.102.5

## Overview:
- Installs script onto router and adds call to "services-start" to automatically customize router WebUI on router bootup
- Provides and interactive manu of options to maintain the script and customize list of tabs to hide
** You must edit the hidetabs file before first use, right after install

## Install:
*Requires Asuswrt-Merlin, JFFS enabled, and entware installed via AMTM*

SSH to the router and enter:

```Shell
/usr/sbin/curl /usr/sbin/curl --retry 3 "https://raw.githubusercontent.com/kstamand/modrouterui/master/modrouterui" -o "/jffs/addons/modrouterui/modrouterui" --create-dirs && chmod +x /jffs/addons/modrouterui/modrouterui && sh /jffs/addons/smodrouterui/modrouteryi -install
```

## Configuration:
1. Edit the file /jffs/addons/modrouterui/hidtabs file to contain the menu tab names you wish to hide / not show in routers WebUI
  - To see a list of avaialable tab names, choose option 2 (about) from the script's menu
  - add one line for each tab name 
   
## Usage:
Once installed, from a terminal session into the router, enter the command modrouterui and choose from one of the menu options:

    (1) About        explain functionality
    (2) Help         information on how to use this script
    (3) Install      install modrouterui files
    (4) Update       check for script updates
    (5) Edit         edit the hidetabs file to only contain the tab names (menu_xxxx) you want to hide
    (6) Hide         run this if you changed the contents of "hidetabs" file and dont want to reboot
    (7) Unhide       restore router UI to default tabs
    (8) Debug        enable verbose logging for troubleshooting
    (9) Uninstall    completely remove modrouterui from the router
    (e) Exit         exit without doing anything
