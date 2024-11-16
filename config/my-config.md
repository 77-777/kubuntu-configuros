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
    apt -y install gcc g++ gpg git make default-jdk util-linux alsa-utils net-tools
    # was openjdk and coreutils-full

  ### Preliminary
    apt -y install nano vim emacs htop tree neofetch wget unrar 7zip rsync secure-delete ssh
    # was openssh and srm

  ### Terminal
    apt -y install tmux irssi rtorrent lynx tty-clock slock weechat scrot

  ### Browser
    apt -y install firefox chromium

  ### Email
    apt -y install thunderbird

  ### Torrent
    apt -y install deluge transmission transmission-qt

  ### Communication
    apt -y install hexchat

  ### Security
    apt -y install pass keepass2 timeshift

  ### Multimedia
    apt -y install vlc audacity handbrake lmms openshot-qt cheese

  ### Graphics
    apt -y install gimp blender inkscape imagemagick

  ### Office
    apt -y install libreoffice pdfsam
    # pdfsam was pdfsam-basic

  ### Accessories
    apt -y install anki cherrytree evince

  ### Networking
    apt -y install akregator quiterss filezilla wireshark

  ### System
    apt -y install virtualbox

  ### Development
    apt -y install codeblocks ruby texmaker

  ### Gaming
    apt -y install steam lutris

  ### Miscellaneous, Fonts, Etc
    apt -y install fonts-roboto
    apt -y install awesome
    apt -y install thunar
    # apt -y install moz-fcitx

    apt -y install flatpak
    apt -y install gnome-software-plugin-flatpak
    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo ## reboot after this

  ### Snap Repository
    snap install discord
    snap install nushell --classic
    snap install opera
    snap install xmind
    snap install sublime-text --classic
    snap install code --classic

  ### Flatpak Repository
    flatpak install anydesk
    flatpak install yacreader

    # staruml yacreader not found at all, nor on snap. separate repository?
    # install anydesk and teamviewer from snap

  ### External Repositories
    add-apt-repository ppa:unit193/encryption -y
    apt update
    apt -y install veracrypt

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
