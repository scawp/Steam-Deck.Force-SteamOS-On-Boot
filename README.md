# Steam-Deck.Force-SteamOS-On-Boot
When Dual Booting, This Script will Force SteamOS to Boot when Powering on rather than Windows


# How Does this work?

A systemd service is installed that tells the system to launch SteamOS on the next boot (as seen in `efibootmgr`).

This script assumes the SteamOS is `Boot0001` to check this in `konsole` type `efibootmgr` :

```
BootNext: 0001
BootCurrent: 0001
Timeout: 0 seconds
BootOrder: 2001,0005,0006,0001,0000,2002,2003
Boot0000* Fedora
Boot0001* SteamOS
Boot0005* Windows Boot Manager
Boot0006* sTeam Chinballs
Boot2001* EFI USB Device
Boot2002* EFI DVD/CDROM
Boot2003* EFI Network
``` 
(example result of `efibootmgr`)


# Install (via Curl)

In Konsole type `curl -sSL https://raw.githubusercontent.com/scawp/Steam-Deck.Force-SteamOS-On-Boot/main/curl_install.sh | bash`


# Uninstall

Simply Delete the service

`sudo rm /etc/systemd/system/force-steamos-on-next-boot.service`


# Found a Bug?

Please add to the `issues` tab! https://github.com/scawp/Steam-Deck.Force-SteamOS-On-Boot/issues

# "This is cool! How can I thank you?"
### Why not drop me a sub over on my youtube channel ;) [Chinballs Gaming](https://www.youtube.com/chinballsTV?sub_confirmation=1)

### Also [Check out all these other things I'm making](https://github.com/scawp/Steam-Deck.Tools-List)
