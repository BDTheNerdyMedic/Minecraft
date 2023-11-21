## Upgrading FTB Modpacks

<span style="color:red">**Remember to shut the server down and create a backup before completing the upgrade.**</span>

<span style="color:yellow">Note the you can use an existing FTB installer file with the --latest parameter to avoid several steps.</span>

### Change directory to the Minecraft folder inside the instance directory
    cd /home/amp/.ampdata/instances/[instance]/Minecraft

### Download the server file to the current directory
    wget https://api.modpacks.ch/public/modpack/119/11338/server/linux/serverinstall_119_11338

### Add permission to allow the file to be executed
    chmod +x serverinstall_119_11338

### Execute the installer
#### Fresh download
    ./serverinstall_119_11338
#### Recycled installer
    ./serverinstall_119_11330 --latest

[< Back](index.md)