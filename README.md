This is a small Script for Updating the Discord Version on Arch Linux.
It accesses the build_info.json File and edits the Version Number.

In the GUI, you have two Buttons.
One for the Next Version and one to Enter the Version Number manually.
The Script checks for Formatting when entering the Version Number manually.
The Script asks for root Password before saving.

![Image](https://github.com/user-attachments/assets/26ae343f-c77c-4de6-8cf7-97db4eaa81fe)
![Image](https://github.com/user-attachments/assets/7b9a9a35-d61e-4b2f-8e40-daadadaf3a04)

### Installation

Create a Folder for local Programs:

    mkdir -p ~/.local/bin

Copy the Script into that Folder:

    cp update_discord.sh ~/.local/bin/discord-updater
    chmod +x ~/.local/bin/discord-updater

**Create Desktop-Starter**

Create a Folder for Desktop-Starters:

    mkdir -p ~/.local/share/applications

Create a .desktop File:

    nano ~/.local/share/applications/discord-updater.desktop

Paste the following into the .desktop File:

    [Desktop Entry]
    Name=Discord Version Updater
    Comment=Update Discord Version
    Exec=/home/IHRUSERNAME/.local/bin/discord-updater
    Icon=discord
    Terminal=false
    Type=Application
    Categories=Utility;

Set Permissions:

    chmod +x ~/.local/share/applications/discord-updater.desktop

IMPORTANT

Replace "IHRUSERNAME" with your Username.
After Installation, you should find the Script in your Startmenu.
You can also create a Desktop Shortcut:

    ln -s ~/.local/share/applications/discord-updater.desktop ~/Desktop/

