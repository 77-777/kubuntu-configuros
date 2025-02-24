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
add-apt-repository ppa:<repo_name>/encryption -y
```

## Preliminary

```bash
# Change su password, as you cannot login directly. Root is locked by default.
sudo passwd root

# Change scheduler (as su) - More info here - https://unix.stackexchange.com/questions/375600/how-to-enable-and-use-the-bfq-scheduler
sudo modprobe bfq

echo bfq > /sys/block/nvme0n1/queue/scheduler
cat /sys/block/nvme0n1/queue/scheduler

# Change Kernel parameters. (as su)
sysctl vm.dirty_background_bytes=2500000 #4194304
sysctl vm.dirty_bytes=2500000 #4194304

sysctl vm.dirty_ratio=3
sysctl vm.dirty_background_ratio=2

sysctl vm.vfs_cache_pressure=10
sysctl vm.swappiness=10
```

## Packages

```bash
#!/bin/bash
# This bash script is to be run as root/sudo.

## Packages to install.

  #########################################################
  ## Prepare Repositories
  #########################################################

  add-apt-repository ppa:unit193/encryption -y
  apt update

  apt -y install flatpak
  apt -y install gnome-software-plugin-flatpak
  flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo ## reboot after this

  #########################################################
  ## Lean and Mean
  #########################################################

  ### Essentials
    apt -y install gcc g++ gpg git make default-jdk alsa-utils ntfs-3g gdebi # find what out this one does.
    # was openjdk and coreutils-full. ntfs-3g used to be called "ntfsprogs"

  ### Preliminary
    apt -y install nano vim tree wget unrar 7zip rsync secure-delete ssh curl
    # was openssh and srm

  ## Diagnostic Tools
    apt -y install htop neofetch net-tools util-linux sysstat iotop nethogs iftop nmon nmap glances radeontop # intel-gpu-tools
    # List: h/top, iostat, vmstat, iotop, lsof, ps, lshw, lspci, lsusb, modprobe, systemctl, nethogs, iftop, nmon, lsblk, df, nmap, glances, radeontop, aptitude intel_gpu_top

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
    apt -y install gimp blender inkscape imagemagick converseen xpaint

  ### Office
    apt -y install libreoffice pdfsam
    # pdfsam was pdfsam-basic

  ### Accessories
    apt -y install anki cherrytree evince synapse plank meld dupeguru fdupes

  ### Networking
    apt -y install akregator quiterss filezilla

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

  ### Snap Repository
    snap install discord
    snap install nushell --classic
    snap install opera
    snap install xmind # minder may be opensource alternative to it? no. freemind is better.
    snap install freemind
    snap install sublime-text --classic
    snap install code --classic
    snap install dolphin-emulator
    snap install ppsspp-emu
    snap install element-desktop
    # snap install emby-server

  ### Flatpak Repository
    flatpak --assumeyes install anydesk
    flatpak --assumeyes install yacreader
    flatpak --assumeyes install lime3ds # fork of citra, continuing it. citra is dead.
    flatpak --assumeyes install freedownloadmanager # alternative - (xdman? [xtreme download manager])

  ### From External Repositories
    apt -y install veracrypt

  #########################################################
  ## Requires Manual Intervention
  #########################################################

  ### Broken automation packages - install manually - ncurses gets in the way even with -y
    # apt -y install emacs
    # apt -y install wireshark

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

```
