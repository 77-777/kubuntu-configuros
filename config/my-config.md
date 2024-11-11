# kubuntu-configuros

> On a stock 24.04.01 LTS, fresh installation of Kubuntu.

## Preliminary

```bash
# Change scheduler

# Change Kernel parameters.
```

## Packages

```bash
#!/bin/bash
# This bash script is to be run as root/sudo.

## Packages to install.

  #########################################################
  ## Lean and Mean
  #########################################################

  ### Essentials
    apt-get install gcc g++ gpg git make openjdk coreutils-full util-linux alsa-utils net-tools

  ### Preliminary
    apt-get install nano vim emacs htop tree neofetch wget unrar 7zip rsync srm openssh

  ### Terminal
    apt-get install tmux irssi rtorrent lynx tty-clock slock weechat scrot

  ### Browser
    apt-get install firefox chromium

  ### Email
    apt-get install thunderbird

  ### Torrent
    apt-get install deluge transmission transmission-qt

  ### Communication
    apt-get install discord hexchat

  ### Security
    apt-get install pass keepass veracrypt timeshift

  ### Multimedia
    apt-get install vlc audacity handbrake lmms openshot-qt cheese

  ### Graphics
    apt-get install gimp blender inkscape imagemagick

  ### Office
    apt-get install libreoffice pdfsam-basic staruml yacreader

  ### Accessories
    apt-get install anki cherrytree xmind sublime vscode evince

  ### Networking
    apt-get install akregator quiterss anydesk teamviewer filezilla wireshark

  ### System
    apt-get install virtualbox

  ### Development
    apt-get install codeblocks ruby texmaker

  ### Gaming
    apt-get install steam lutris

  ### Miscellaneous, Fonts, Etc
    apt-get install roboto
    apt-get install awesome
    apt-get install thunar

  #########################################################
  ## Extras
  #########################################################

  ### Primary (development)
    apt-get install ghc ocaml opam nodejs

  ### Secondary (gaming)
    apt-get install wine wine64 winetricks

  ### Alternatives
    # apt-get install evolution qemu subversion mercurial

  ### KDE Flavours
    # apt-get install kontact kleopatra korganizer kget kmail kdevelop konversation ktorrent krita ## okular kdenlive konqueror amarok

  ### Misc
    # apt-get install fastfetch element-web guake yakuake scribus i3 desmume dolphin-emu ppsspp-qt iptables # gparted gnome-system-manager/monitor

  ### Not in Kubuntu Repository
    # apt-get install freedownloadmanager citra nixnode2 caesium clonespy

  ### anything for ntfs mounter?
    # ???

  ### what about setting scheduler and kernel vm parameters?
    # ???

```
