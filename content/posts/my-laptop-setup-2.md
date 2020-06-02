+++

date = "2020-01-12T14:00:23+05:30"
draft = true
title = "My Linux Laptop Setup II (2020) "
tags = [ "general","setup","manjaro_os"]
categories =["General","Setup","Manjaro_OS"]
bookToc = true
hideToc = true

+++

After using Elementary OS for almost half a decade...since Luna release. I wanted to explore other distros.
As I have mentioned earlier Slackware being my first Linux experience, wanted to go for something similar this time and ended up with arch based Manjaro, it turned out to be great choice. Still using the same laptop (HP EliteBook 2570P)

 The following is a documentation of the new setup.

![](/img/my-linux-laptop-setup-2/0.png)

![](/img/my-linux-laptop-setup-2/1.png)

![](/img/my-linux-laptop-setup-2/2.png)

![](/img/my-linux-laptop-setup-2/3.png)

#### 

#### Update and Upgrade system
First thing to do after Installation is full system update

#### Privacy Settings


Terminal

VMware Workstation

Virtual Box

Virtual Machine Manager

Docker

Geary

Browser

​	Chrome

​	Firefox

​	Opera

Disable tracker(Gnome)


Install browsers

Install Media players


MPVplayer
Audacious



VMware Workstation

 sudo modprobe -a vmw_vmci vmmon

Start and enable services
There are three services that can be optionally be enabled:

vmware-networks.service: Provides network access inside VMs, most people will want this enabled
vmware-usbarbitrator.service: Allows USB devices to be connected inside VMs
vmware-hostd.service: Enables sharing of VMs on the network

To start and enable these services use:

 sudo systemctl enable --now vmware-networks.service
 sudo systemctl enable --now vmware-usbarbitrator.service
 sudo systemctl enable --now vmware-hostd.service


KVM Install



Browsers
    Google Chrome
    Opera
    Firefox
    Brave

Cloud Storage

    Mega
    Dropbox

Github Desktop


Calibre ( I still use version 3.X)

sudo -v  && wget -nv -O- https://download.calibre-ebook.com/linux-installer.sh | sudo sh /dev/stdin version=3.48.0


Redshift
Caffein

Programming Languages

        Python
        Go
        Dart / Flutter
        Rust(rustup)
        lua
        D
        Node
        PWSH
        Ruby

Latte Dock

Graphic Design
    Inkscape


Code Editors

    VSCode
    Sublime Text
    Android Studio

Labs
    VMware workstation
    KVM
    GNS3/ EVENG


sudo pacman -Syu python-pip

 sudo pacman -Syu python-pip
   13  pip install pylint --user
   14  pip install black --user

sudo pacman -S nodejs npm

create .npmrc

npm -g

If you don't want to execute the npm -g with root privileges, here's how to setup npm to support this.

1. Configure npm
npm reads settings from the .npmrc file in your home directory. Create it with the following content:

prefix = ~/.npm
This will tell npm to put all packages, which you install with the -g flag, into .npm/lib/node_modules within your home directory.

2. Configure your $PATH
Some modules (like grunt) come with executable scripts. You probably want to be able to execute them without having to type the full path to .npm/lib/node_modules/.... Thankfully, npm links every executable to .npm/bin. So you just have to add this to your $PATH.

Edit your ~/.bash_profile and add this line:

export PATH=$PATH:~/.npm/bin
That's it.

######
KVM
######

sudo pacman -S qemu virt-manager virt-viewer dnsmasq vde2 bridge-utils openbsd-netcat
sudo pacman -S ebtables iptables

Step 4: Enable normal user account to use KVM
Since we want to use our standard Linux user account to manage KVM, let’s configure KVM to allow this.

Open the file /etc/libvirt/libvirtd.conf for editing.

sudo pacman -S vim
sudo vim /etc/libvirt/libvirtd.conf
Set the UNIX domain socket group ownership to libvirt, (around line 85)

unix_sock_group = "libvirt"
Set the UNIX socket permissions for the R/W socket (around line 102)

unix_sock_rw_perms = "0770"
Add your user account to libvirt group.

sudo usermod -a -G libvirt $(whoami)
newgrp libvirt
Restart libvirt daemon.

sudo systemctl restart libvirtd.service


Step 5: Enable Nested Virtualization (Optional)

Nested Virtualization feature enables you to run Virtual Machines inside a VM. Enable Nested virtualization for kvm_intel by enabling kernel module as shown.

sudo modprobe -r kvm_intel
sudo modprobe kvm_intel nested=1
To make this configuration persistent,run:

echo "options kvm-intel nested=1" | sudo tee /etc/modprobe.d/kvm-intel.conf
Confirm that Nested Virtualization is set to Yes:

$ systool -m kvm_intel -v | grep nested
    nested              = "Y"
    nested_early_check  = "N"
$ cat /sys/module/kvm_intel/parameters/nested
Y


sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service


sudo pacman -S docker
sudo systemctl start docker
sudo systemctl enable docker

sudo docker version
sudo usermod -aG docker $USER


Joplin
Cherry Tree


Install GNS3


popsicle

