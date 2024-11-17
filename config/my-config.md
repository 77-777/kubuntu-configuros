# kubuntu-configuros

> On a stock 24.04.01 LTS, fresh installation of Kubuntu.

## Common Commands

```bash
# APT replaces APT-GET.

sudo apt install <package>
sudo apt install ./<deb_file>.deb

# Refresh the repository / get updates.
sudo apt update

# Install updates
sudo apt upgrade

# Cleanup
sudo apt autoremove

# Add repository
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
    apt -y install gcc g++ gpg git make default-jdk alsa-utils ntfs-3g gdebi # find what out this one does.
    # was openjdk and coreutils-full. ntfs-3g used to be called "ntfsprogs"

  ### Preliminary
    apt -y install nano vim emacs tree wget unrar 7zip rsync secure-delete ssh curl
    # was openssh and srm

  ## Diagnostic Tools
    apt -y install htop neofetch net-tools util-linux sysstat iotop nethogs iftop, nmon, nmap, glances, radeontop # intel-gpu-tools
    # List: h/top, iostat, vmstat, iotop, lsof, ps, lshw, lspci, lsusb nethogs, iftop, nmon, lsblk, df, nmap, glances, radeontop, aptitude # intel_gpu_top

  ### Terminal
    apt -y install tmux mc irssi rtorrent lynx tty-clock slock weechat scrot

  ### Browser
    apt -y install firefox chromium

  ### Email
    apt -y install thunderbird

  ### Torrent
    apt -y install deluge transmission transmission-qt

  ### Communication
    apt -y install hexchat pidgin

  ### Security
    apt -y install pass keepass2 timeshift

  ### Multimedia
    apt -y install vlc audacity handbrake lmms openshot-qt cheese obs-studio

  ### Graphics
    apt -y install gimp blender inkscape imagemagick xpaint

  ### Office
    apt -y install libreoffice pdfsam
    # pdfsam was pdfsam-basic

  ### Accessories
    apt -y install anki cherrytree evince synapse plank

  ### Networking
    apt -y install akregator quiterss filezilla wireshark

  ### System
    apt -y install virtualbox # get a usb writer too.

  ### Development
    apt -y install codeblocks ruby texmaker

  ### Gaming
    apt -y install steam lutris

  ### Miscellaneous, Fonts, Etc
    apt -y install fonts-roboto
    # apt -y install awesome
    # apt -y install thunar
    # apt -y install moz-fcitx

    apt -y install flatpak
    apt -y install gnome-software-plugin-flatpak
    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo ## reboot after this

  ### Snap Repository
    snap install discord
    snap install nushell --classic
    snap install opera
    snap install xmind # minder may be opensource alternative to it?
    snap install sublime-text --classic
    snap install code --classic
    snap install dolphin-emulator
    snap install ppsspp-emu
    # snap install element-desktop # already comes installed.
    # snap install emby-server

  ### Flatpak Repository
    flatpak install anydesk
    flatpak install yacreader
    flatpak install lime3ds # fork of citra, continuing it. citra is dead.
    flatpak install freedownloadmanager # alternative - (xdman? [xtreme download manager])

  ### External Repositories
    add-apt-repository ppa:unit193/encryption -y
    apt update
    apt -y install veracrypt

  ## Manual Installation - Need to download .deb from official website
    # sudo apt install ./teamviewer.deb
    # sudo apt install ./staruml.deb
    # java -jar ubooquity.jar

  #########################################################
  ## Extras
  #########################################################

  ### Primary (development)
    apt -y install ghc ocaml opam nodejs

  ### Secondary (gaming)
    apt -y install wine wine64 winetricks

  ### Alternatives
    # apt -y install evolution qemu-system subversion mercurial
    # was qemu

  ### KDE Flavours
    # apt -y install kontact kleopatra korganizer kget kmail kdevelop konversation ktorrent krita kolourpaint ## okular kdenlive konqueror
    # amarok not existant.

  ### Misc
    # apt -y install nixnote2 guake yakuake scribus i3 desmume iptables # gparted gnome-system-monitor
    # fastfetch (hyfetch?) not existant.

  ### Not in Kubuntu Repository
    # apt -y install caesium clonespy

  ### anything for ntfs mounter?
    # ???

  ### what about setting scheduler and kernel vm parameters?
    # ???

```
