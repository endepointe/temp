#!/bin/bash

sudo apt update
sudo apt upgrade

#install necessary tools
sudo apt install zsh tmux emacs cinnamon kali-defaults kali-root-login desktop-base gdb python3-pip cmake gdb-peda gnome-terminal cowsay figlet filters fortunes bsdgames bsdgames-nonfree dos2unix asciinema python3-pyx squashfs-tools squashfs-tools-ng zlib1g-dev liblzma-dev liblzo2-dev docker.io containerd xfsprogs 

#optional, uncomment if you want a "full" kali install
#sudo apt install kali-tools-gpu kali-tools-hardware kali-tools-fuzzing kali-tools-sdr kali-tools-rfid kali-tools-information-gathering kali-tools-vulnerability kali-tools-passwords kali-tools-wireless kali-tools-reverse-engineering kali-tools-exploitation kali-tools-forensics cmake libboost-all-dev texlive-full emacs auctex fontforge doxygen python3-scipy python3-numpy graphviz radare2-cutter

#install gef
wget -q -O- https://github.com/hugsy/gef/raw/master/scripts/gef.sh | sh
sudo -H pip3 install keystone-engine ropper capstone unicorn requests

#environment setup
wget -q -O setup-373.tar.bz2 https://web.engr.oregonstate.edu/~dmcgrath/setup-373.tar.bz2
tar xjvf setup-373.tar.bz2 -C ~/
chsh --shell /bin/zsh
