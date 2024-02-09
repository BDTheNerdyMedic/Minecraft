## Upgrading CurseForge Modpacks

<span style="color:red">Remember to shut the server down and create a backup before completing the upgrade.</span>

### Elevate privileges and run commands within the root user's environment
    sudo -i

### Change directory to the Minecraft folder inside the instance directory
    cd /home/amp/.ampdata/instances/[instance]/Minecraft

### Download the server file to the current directory
    wget https://mediafilez.forgecdn.net/files/4885/539/Server-Files-0.2.21.zip

### Verify the archive has a root directory
    unzip -l Server-Files-0.2.21.zip

### Extract the archive as the amp user to maintain proper ownership

#### With root directory
    su -c "unzip Server-Files-0.2.21.zip" amp

#### No root directory
    su -c "unzip -d ./Server-Files-0.2.21 Server-Files-0.2.21.zip" amp

### Purge common directories to avoid conflicts
    rm -R ./config
    rm -R ./defaultconfigs
    rm -R ./kubejs
    rm -R ./mods
    rm -R ./packmenu

### Use the rsync command to syncronize the files

#### Dry run
    rsync -aunv ./Server-Files-0.2.21/ ./

#### Complete sync
    rsync -auv ./Server-Files-0.2.21/ ./

<span style="color:red">Remember to double-check the Forge vesion and update the MOTD to reflect the modpack version.</span>

[< Back](index.md)
