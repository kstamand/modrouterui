# ModrouterUI - Customize Asuswrt-Merlin router Web UI to hide unused / unwanted tabs

This script has been developed and tested on a GT-AX6000, running Asuswrt-Merlin 3006.102.5

## Overview:
- Installs script onto router and adds call to "services-start" to automatically customize router WebUI menus on router bootup
- Provides and interactive manu of options to maintain the script and customize list of menus to hide from router WebUI
** You must edit the hide_menus_list file before first use, right after install

## Install:
*Requires Asuswrt-Merlin, JFFS enabled, and entware installed via AMTM*

SSH to the router and enter:

```Shell
/usr/sbin/curl --retry 3 "https://raw.githubusercontent.com/kstamand/modrouterui/master/hideuimenus" -o "/jffs/addons/modrouterui/hideuimenus" --create-dirs && chmod +x /jffs/addons/modrouterui/hideuimenus && sh /jffs/addons/modrouterui/hideuimenus install
```

## Configuration:
1. Edit the file /jffs/addons/modrouterui/hide_menus_list file, using the option #5 (Edit), from the scripts menu:
  - The hide_menus_list file contains a commented list of menus to select
  - Uncomment the menus you wish to hide, generally those you may never use
  - After you save and exit the editor, choose menu option #6 to apply the changes (hide selected menus) from router's UI
   
## Usage:
Once installed, from a terminal ssh session into the router, enter the command hideuimenus and choose from one of the menu options:

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
