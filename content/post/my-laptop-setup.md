+++

date = "2017-06-21T14:00:23+05:30"
draft = false
title = "Chronicles of my Linux Laptop Setup I ( Hp-Elitebook + Elementary OS Loki ) "
tags = [ "general","setup","elementary_os"]
categories =["General","Setup","Elementary_OS"]

+++

![](/img/my-linux-laptop-setup/0.png)

![](/img/my-linux-laptop-setup/1.png)

After being in draft for years I am finally publishing this post updated to my current setup(Loki).

I started writing this as a documentation of my setup for self, then i thought its good to share once experience.

Linux has always been my choice of OS at home from early days of my computer usage.

Mandrake Linux was the only distro at that time known to me until I was introduce to Slackware, which has been my distro of Linux for many years. Until 2010 my pc setup was mostly windows/slackware dual-boot and windows at work place for obvious reasons.

This changed when my friends started using MacBook Pro in year 2010, I couldn't resist myself and went on to install hackintosh on my PC. It took a lot of effort ... I mean I had to struggle with lot of iterations for drivers to make things work. Even though I was using iPhone already, this is my first Mac OS experience. The best thing was how my workflow improved with Mac OS. Though now and then stability was an issue with my Hackintosh.

By the end of 2012, I got my new laptop HP EliteBook 2570p, suddenly I have a laptop with 16GB RAM, Intel Core i7 , dual SSD disk etc. I was determined to have best possible setup.

First thing I did was to remove windows 7 on it completely. Initially I considered to go with Hackintosh, after some effort I opted out due to stability issues(Now a days I triple boot into WIN10/Linux on first SSD and Hackinstosh from second ssd on this laptop for my iPad sync). My primary OS is Linux (Elementary OS) unless I specifically need WIN or MacOS.

![](/img/my-linux-laptop-setup/about.png)

At this time I started looking out for linux distros other than Ubuntu with good desktop environment and I stumbled upon [Elelementary OS](https://elementary.io/), I never looked back since them. If you look at what elementary team have achieved so far, its amazing . There is a saying that "Simplicity Is The Real Beauty" and Elementary OS exactly fits into that saying.

[Elementary OS design](https://elementary.io/docs/human-interface-guidelines) philosophy is simple and elegant. Only thing I miss coming from Hackintosh is few apps (Sparrow,SourceTree,Evernote,Reeder etc) that i got used to over the period of using hackintosh. Eventually I have found decent/good alternatives, some in default apps of Elementary OS and some in electron based apps.

Due to its simplicity I have been more productive too. I started with Luna --> Freya --> Loki and it just gets better with every release. The current Loki release of 0.4.1 is a massive one.

I have done fresh install for every new release. Also I have tried to use apps(gimp,darktable etc) from appcenter for most of them unlike earlier setups where I tried to use external ppa to get most latest releases of apps.

Over the period of decade I have come to like and use many tools, I do not use everything on daily basis I just love to have them installed and configured to be used when needed.

The following is the effort to document my setup.

![](/img/my-linux-laptop-setup/1.1.png)

#### Update and Upgrade system

After default installation update and upgrade your system

        sudo apt update
        sudo apt upgrade
        sudo apt dist-upgrade

#### Privacy Settings

This is first thing to do for me, enable "Privacy Mode"

![](/img/my-linux-laptop-setup/1.gif)

#### Enable PPA support

PPA support is not available by default in Loki, for some good reasons . Though
it is impossible to completely stay away from it for someone like me.

        sudo apt install software-properties-common --no-install-recommends


#### Basic compression tools

         sudo apt install rar unrar cabextract lzip lunzip arj unace p7zip-rar p7zip

#### Media Codecs

As far as my understanding goes Elementary OS default installation comes with required codecs unlike Ubuntu .

#### Install Elementary Tweak

It is a must for every elementary os user who would like to tweak, I wonder why its not inbuilt.

        sudo add-apt-repository ppa:philip.scott/elementary-tweaks
        sudo apt update && sudo apt install elementary-tweaks

![](/img/my-linux-laptop-setup/eos-tweaks.png)

I love dark theme....I wish it was officially supported. Elementary OS Dev team suggest
against tweaks app ....but then I wanted dark theme.

Also I have added couple of icon themes as follows apart from default. These themes
just extend default theme. They make wingpanel icons look better .

#### Install Icon theme

        sudo add-apt-repository ppa:cybre/elementaryplus
        sudo apt update
        sudo apt upgrade && sudo apt install elementaryplus


        sudo add-apt-repository ppa:elementary-add-team/icons
        sudo apt update
        sudo apt upgrade && sudo apt install elementary-add-icon-theme

Also few other icon themes that I have installed .....

        sudo add-apt-repository ppa:papirus/papirus
        sudo apt-get update
        sudo apt-get install papirus-icon-theme

I prefer not to install any GTK themes as I love default Elementary GTK Theme

Sometimes tray icons doesnt fit right into existing theme, in such case [hardcode-tray](https://github.com/bil-elmoussaoui/Hardcode-Tray) can be handy

        sudo add-apt-repository ppa:andreas-angerer89/sni-qt-patched
        sudo apt update
        sudo apt install sni-qt sni-qt:i386 hardcode-tray

#### Fontmanager

Font Viewer is available with default installation. For who want to use font manager install Font-Manager

        sudo apt install font-manager

#### Dual Monitor Setup ( Not using this in Loki)

I use external monitor at home, after trying out various hacks, found this gem.

[MultiPlank](https://heathpaddock.com/?p=854)

        sudo apt-add-repository ppa:heathbar/multiplank
        sudo apt update
        sudo apt install multiplank

Once installed, enable multiplank by issuing the following command:

         multiplank -e

And to disable:

        multiplank -d

Also I use this for controlling my dual monitors

        sudo add-apt-repository ppa:apandada1/brightness-controller
        sudo apt update
        sudo apt install brightness-controller

## Browsers

Chrome is default browser and Opera, Firefox, Vivaldi when normal is boring.

#### Google Chrome

Chrome is my default one with lots of chrome apps(feedly,tweedeck etc)

        wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
        sudo dpkg -i ./google-chrome*.deb
        sudo apt-get install -f

#### Opera

I use it for its inbuilt vpn feature plus when ever I dont need chrome . I before Chrome came into existance Opera was my default browser.

#### Firefox

Install from Appcenter

#### FeedReader

Lately using Feedly webapp

### Dev Setup

#### Text Editors

##### Scratch (Default)

Scratch Text editor is the default one in Elementary OS, its a fork of Gedit.
Most of the text editing done on Scratch including this blog post. I have added few
color schemes other than default ones.

![](/img/my-linux-laptop-setup/scratch.png)

##### Sublime Text 3

Sublime Text has been my default since its launch and now theres official repo
for apt.

        echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

        sudo apt update && sudo apt install sublime-text

![](/img/my-linux-laptop-setup/sublime-text-3.png)

##### VS Code

Now a days exploring VS Code and i started loving it sooner than expected as I used to descpice anything M$

### Tools


#### Slack Client

Slack provides official client for linux

#### Install torrent client

Transmission from AppCenter

#### Install JAVA

Java is needed for some of the java based apps that are installed like Enpass or Xmind.

        sudo add-apt-repository -y ppa:webupd8team/java
        sudo apt-get update
        sudo apt-get install oracle-java8-installer

#### Install Node via NVM

Node is required for Firebase-tools that I use to deploy my websites.

        curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash

        nvm ls-remote

        nvm install 6.11.0

#### Install LibreOffice Suites

             sudo add-apt-repository ppa:libreoffice/ppa
             sudo apt updatew
             sudo apt install libreoffice-gtk2 libreoffice-gnome libreoffice-writer

#### Misc Tools

            sudo apt install gnome-disk-utility gnome-system-monitor gparted

### Graphic Designing

#### Pencil

[Pencil V3](http://pencil.evolus.vn) is a complete re-write using Githubs Electron .

#### Scribus

Install from appcenter

#### Inkscape

All of my designs are done using Inkscape as of this writing.

    sudo add-apt-repository ppa:inkscape.dev/stable
    sudo apt-get update
    sudo apt-get install inkscape

#### Gravit Designer

This is the latest addition

#### GIMP

Installed the default package available from appcenter

#### Blender3D

Want to learn this some day just for fun. More interested in Motion Graphics. Installed the default package available from appcenter.

### Cloud storage

#### Dropbox

for some reasons official package doenst work as expected on elementary os. There is a workaround for that in the following link

         git clone https://github.com/zant95/elementary-dropbox /tmp/elementary-dropbox
         bash /tmp/elementary-dropbox/install.sh


          sudo apt purge epiphany-browser epiphany-browser-data

#### Fonts

I go with default faunts that come with elementary os. For text editors I use
[Hermit Font](https://pcaro.es/p/hermit/) which has been my go to font for years now.

Also I use [Source Code Pro](https://github.com/adobe-fonts/source-code-pro) , which is another great font for texteditor/ide.

[ProgrammingFonts](http://app.programmingfonts.org/) is a good place to check
for font you would want to use.

[Mono Spaced Fonts for Programmers](https://www.hanselman.com/blog/MonospacedProgrammingFontsWithLigatures.aspx)

#### Install calibre

Defacto , nothing comes close, though there is a elementary os native app BOOKWORM in developemnt
and it is slick and promising from what ever I have seen so far.

        sudo -v && wget -nv -O- https://raw.githubusercontent.com/kovidgoyal/calibre/master/setup/linux-installer.py | sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"

#### Install Zeal

Was looking for Dash alternative unitl i found this. Theres a nice integration into most of the code editors. The doc set is from DASH itsel. I have nicely integrated into Sublime and Brackets.

        sudo add-apt-repository ppa:zeal-developers/ppa
        sudo apt-get update
        sudo apt-get install zeal

![](/img/my-linux-laptop-setup/brackets-zeal.gif)

### Install redshift

This is a must. Install it from appcenter

### Enpass

[Enpass](https://enpass.io/) is my password manager. I use this because of cloud sync and mobile app. No matter whether I am using my mobile or pc or laptop I always have access to enpass.

Its free for desktop, though mobile edition costs you, check the [pricing](https://enpass.io/pricing/)

### Install Git Client

[GitKraken](http://www.gitkraken.com/) I was missing Sourcetree untill I started using this. Its simple and clean UI is impressive. Its usefull for my basic needs of version control(mostly scripts and texts)

### WebUpd8 Java PPA

Due to Oracle’s licensing restrictions, Java is no longer included within Ubuntu’s default packages list.

WebUpd8 team has provided a PPA that downloads and packages Java for you.

        sudo add-apt-repository ppa:webupd8team/java
        sudo apt-get update
        sudo apt-get install oracle-java8-installer

## Startup Disk Creator

### UNetbootin

    sudo apt-get install unetbootin

### StartUP Disk Creator

    sudo apt-get install usb-creator-gtk

### WoeUSB (fork of WinUSB)

To create windows usb bootable installation media.

        sudo add-apt-repository ppa:nilarimogard/webupd8
        sudo apt update
        sudo apt install woeusb

Or install from deb file

        http://ppa.launchpad.net/nilarimogard/webupd8/ubuntu/pool/main/w/woeusb/woeusb_2.1.2-1~webupd8~xenial_amd64.deb
        sudo dpkg -i woeusb_2.1.2-1~webupd8~xenial_amd64.deb
        http://ppa.launchpad.net/nilarimogard/webupd8/ubuntu/pool/main/w/woeusb

gnome-disk-utility

### FTP Client

Its obvious , its Filezilla client. Hope to see Trasmit like client on Linux.

    sudo apt-get install filezilla

#### Safe Eyes

A simple utitly that forces you to take breaks

### PPA Purge

Some times when PPA installs go bad..this tool helps to restore

        sudo apt-get install ppa-purge

## Network Tools

### Wireshark

        sudo add-apt-repository ppa:wireshark-dev/stable
        sudo apt-get update
        sudo apt-get install wireshark

### Nmap 7

Download source code nmap 7 :

         wget https://nmap.org/dist/nmap-7.50.tar.bz2

Unzip file and move to folder :

         bzip2 -cd nmap-7.50.tar.bz2 | tar xvf -
        cd nmap-7.50

Configuration and Install from source code :

         ./configure
         make
         sudo make install

### Iperf

          sudo apt-get install iperf

## Documentations && Blogging

### Sphinx

Recently I have started consolidating the technical docs I have dumped into my backups for years. I am trying to centralize all the guides and tutorials that I have saved as text files from over the time in my career. I found [Sphinx](http://www.sphinx-doc.org/en/stable/)to be suitable, also I am exploring [MKDOCS](http://www.mkdocs.org/) too. I would like to publish this at some point as **SysNetLabs** . Mainly for myself though might be usefull for others too. Thats the idea.

            sudo apt-get install python3-setuptools
            sudo easy_install3 pip


            sudo pip3 install Sphinx
            sudo pip3 install recommonmark

### Hugo

I use [Hugo](https://gohugo.io/) for my personal blog at **[kanthi.in](http://kanthi.in)** . I have added hugo command to my system startup. Now every time I edit and save my post I have hugo autogenerate for me in the background. With dual monitor setup , this is a good workflow.

        "hugo server  --buildDrafts  --watch  --source=/home/king/Workspace/Repos/kanthi.in"

#### Baobab Disk Uage Analyzer

Its always good to have this tool.

         sudo apt-get install baobab

![](/img/my-linux-laptop-setup/Disk_Usage_Analyzer.png)

I miss Evernote native client though i manage with chrome app

#### Variety Wallpaper Changer

Wallpaper plays a very important role for me ;-) . [Variety](http://peterlevi.com/variety/) is a wallpaper changer for linux os.

            sudo add-apt-repository ppa:peterlevi/ppa
            sudo apt-get update
            sudo apt-get install variety

#### National Geo Wallpaper

        wget https://launchpad.net/~atareao/+archive/ubuntu/atareao/+files/national-geographic-wallpaper_0.4.3-0extras16.04.0_all.deb
        sudo dpkg -i national-geographic-wallpaper_0.4.3-0extras16.04.0_all.deb

#### Screencast

After trying out various tools I have decided on KAZAM . Its simple and usefull


#### Peek

Its a simple tool to record your screen and export into multiple formats including gif
Some of the gifs on this blogs are creating using the same.

        sudo add-apt-repository ppa:peek-developers/stable
        sudo apt update
        sudo apt install peek

![](/img/my-linux-laptop-setup/diskspace.png)

#### Mogrify

mogrify -path ../PathToFolder/ -format ico -density 600 -define icon:auto-resize=128,64,48,32,16 \*.svg

#### Caffeine

When you do not want be disturbed by screen saver etc

sudo add-apt-repository ppa:caffeine-developers/ppa
sudo apt-get update
sudo apt-get install caffeine

### Screenkey

            sudo add-apt-repository ppa:nilarimogard/webupd8
            sudo apt-get update
            sudo apt-get install screenkey

#### Audacious

             sudo apt-get install audacious

#### Minitube

         sudo apt-get install minitube

### Video Editing:

#### HandBrake

In the initial days of my iphone usage , handbrake was my saviour.

        sudo add-apt-repository ppa:stebbins/handbrake-releases
        sudo apt update
        sudo apt install handbrake-gtk
        sudo apt install handbrake-cli

- Cinelerra
- Avidemux
- Pitivi
- Shotcut App
- http://ardour.org/
- http://www.cinepaint.org/

### E-Mail Client

I used thunderbird in early days and Sparrow on MacOS which google acquired and killed it. I still have Sparrow on my Hackintosh ;-)

On Elementary OS theres default MAIL app which is nothing but fork of Geary , it comes as a native app as part of default installation. I still have issues with auto scaling of the app and a few crashes . Theres nothing else that comes close at the moment :(

## Photography

Mobile Photography is one of my hobby. I find it challenging to take good pics using mobile. This started when I got my first **iPhone**  and these days with **OnePlus One**

### Digikam

At the moment I do cloud sync of mobile pics with dropbox and google photos. So digikam is yet to be part of my workflow.

### Darktable

Most of work is done on my mobile with Snapseed. I intend
to learn how to use darktable

## Music Creation (New to these tools)

So far considering these tools...still exploring

#### Audacity

- http://www.hydrogen-music.org/hcms/
- http://www.rncbc.org/drupal/
- Rosegarden

### LMMS

        sudo apt install lmms

### Mixx

This is just for kicks. Ocassionally i have used auto mixx feature

          sudo add-apt-repository ppa:mixxx/mixxx
          sudo apt update
          sudo apt install mixxx

## Games

The games that I have installed

![](/img/my-linux-laptop-setup/games.png)



### DevOps Labs Virtualization

![](/img/my-linux-laptop-setup/virt.png)

#### KVM

        king@konquer:~$ kvm-ok
        INFO: /dev/kvm exists
        KVM acceleration can be used


        sudo apt install qemu-kvm libvirt-bin bridge-utils virt-manager virtinst virt-viewer

#### VMware Workstation

Download the binary.

#### VirtualBox

        sudo vim /etc/apt/sources.list.d/virtualbox.list

Add following line

    #For Ubuntu 16.04 ("Xenial")
        deb http://download.virtualbox.org/virtualbox/debian xenial contrib

Add the keys

         wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
         wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -


        sudo apt update

        king@konquer:~$ apt-cache policy virtualbox-5.1
        virtualbox-5.1:
          Installed: (none)
          Candidate: 5.1.22-115126~Ubuntu~xenial
          Version table:
             5.1.22-115126~Ubuntu~xenial 500
                500 http://download.virtualbox.org/virtualbox/debian xenial/contrib amd64 Packages


         sudo apt install virtualbox-5.1

#### Vagrant

Download the latest vagrant deb file https://www.vagrantup.com/

        wget https://releases.hashicorp.com/vagrant/1.9.5/vagrant_1.9.5_x86_64.deb
        sudo dpkg -i vagrant_1.9.5_x86_64.deb

#### Docker

Follow the official documentation

#### Ansible

        sudo apt-get install software-properties-common
        sudo apt-add-repository ppa:ansible/ansible
        sudo apt-get update
        sudo apt-get install ansible

#### GNS3

GNS3 V2 is no longer just for networking guys, with its new architecture gns3
use cases are beyond Cisco and GNS3 VM makes it more flexible, theres also

        sudo add-apt-repository ppa:gns3/ppa
        sudo apt-get update
        sudo apt-get install gns3-gui

If you want IOU support:

        sudo dpkg --add-architecture i386
        sudo apt-get update
        sudo apt-get install gns3-iou

#####

#### Network Interface Names

Current Ubuntu versions have new naming convention of network interfaces, to get to old ways follow these steps

        $ sudo nano /etc/default/grub
        Look for “GRUB_CMDLINE_LINUX”  and add the following”net.ifnames=0 biosdevname=0“.

        From:

        GRUB_CMDLINE_LINUX=""
        To:

        GRUB_CMDLINE_LINUX="net.ifnames=0 biosdevname=0"
        Generate a new grub file using the following command.

        sudo grub-mkconfig -o /boot/grub/grub.cfg

#### Appcenter

A sepcial mention about the efforts of the dev with Appcenter. Its still young with great
future. There are already elementary specific tools

![](/img/my-linux-laptop-setup/appcenter.png)

#### Disk Image

Finally I have taken complete disk image of the entire ssd using gnome-disk-utilty. Yet to test its restore
capabilities.


#### My Wishlist

Eelementary : Wingpanel (More options to customize like auto-hide, slim etc whould be great for small screens)
Better Tray icons
Officcial dark mode

Computer Hardware : I wish to see real bezel less displays on laptop too. At the moment my fav is XPS Developer Edition. Unless something better comes

Mobile Hardware : Been using classic OnePlus One since it lanuched with multiboot. Exploring new roms when ever bored with out disturbing primary rom. Also I have Netrunner as one of the secondary roms...still yet to explore it completely. Having high hopes for next iPhone(8) release.

My Laptop has a 3G sim slot.....not sure how to use it in elementary Linux

## Clean up!

As a final step, let’s get rid of packages and software that are not necessary and taking up our precious disk space.

    sudo apt-get autoclean
    sudo apt-get clean

#### Further Elementary OS resources

Google plus group
Stack Exchange
https://www.reddit.com/r/elementaryos/



