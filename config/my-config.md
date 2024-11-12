# kubuntu-configuros

> On a stock 24.04.01 LTS, fresh installation of Kubuntu.

## Common Commands

```bash
# APT replaces APT-GET.
```

## Preliminary

```bash
# Change scheduler

# Change Kernel parameters.
```

## Packages

```bash
#!/bin/bash
# This bash script is to be run as root/sudo.

## Some package asked me for email configuration and toggled a prompt, cutting automation. Need to find out which. It was before installing irssi set of pkgs.
## Wireshark also prompts to ask if non-superusers should be able to capture packets.

## Packages to install.

  #########################################################
  ## Lean and Mean
  #########################################################

  ### Essentials
    apt -y install gcc g++ gpg git make default-jdk util-linux alsa-utils net-tools # was openjdk and coreutils-full

  ### Preliminary
    apt -y install nano vim emacs htop tree neofetch wget unrar 7zip rsync secure-delete ssh # was openssh and srm

  ### Terminal
    apt -y install tmux irssi rtorrent lynx tty-clock slock weechat scrot

  ### Browser
    apt -y install firefox chromium

  ### Email
    apt -y install thunderbird

  ### Torrent
    apt -y install deluge transmission transmission-qt

  ### Communication
    apt -y install hexchat # install discord from snap

  ### Security
    apt -y install pass keepass2 timeshift # install veracrypt from separate repository. keepass became keepass2.

  ### Multimedia
    apt -y install vlc audacity handbrake lmms openshot-qt cheese

  ### Graphics
    apt -y install gimp blender inkscape imagemagick

  ### Office
    apt -y install libreoffice pdfsam # pdfsam waas pdfsam-basic. staruml yacreader not found at all. separate repository?

  ### Accessories
    apt -y install anki cherrytree evince # xmind sublime vscode

  ### Networking
    apt -y install akregator quiterss filezilla wireshark # install anydesk and teamviewer from snap

  ### System
    apt -y install virtualbox

  ### Development
    apt -y install codeblocks ruby texmaker

  ### Gaming
    apt -y install steam lutris

  ### Miscellaneous, Fonts, Etc
    apt -y install fonts-roboto # was roboto
    apt -y install awesome
    apt -y install thunar
    # apt -y install nushell # installed by snap.

  #########################################################
  ## Extras
  #########################################################

  ### Primary (development)
    apt -y install ghc ocaml opam nodejs

  ### Secondary (gaming)
    apt -y install wine wine64 winetricks

  ### Alternatives
    # apt -y install evolution qemu subversion mercurial

  ### KDE Flavours
    # apt -y install kontact kleopatra korganizer kget kmail kdevelop konversation ktorrent krita ## okular kdenlive konqueror amarok

  ### Misc
    # apt -y install fastfetch element-web guake yakuake scribus i3 desmume dolphin-emu ppsspp-qt iptables # gparted gnome-system-manager/monitor

  ### Not in Kubuntu Repository
    # apt -y install freedownloadmanager citra nixnode2 caesium clonespy

  ### anything for ntfs mounter?
    # ???

  ### what about setting scheduler and kernel vm parameters?
    # ???

```
