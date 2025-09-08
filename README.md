# Packed
<a href="https://www.buymeacoffee.com/pietroes" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

Ok, so you are a technician and the company you've been working for a couple of months asks you to setup an evironment of five _Ubuntu_ virtual machines for _Debian_ apps. You have to use your own personal PC and your internet connection. Every machine has a slight change in the packages required and has to be as purged as possible for maximum performance - _So no, copying the same qcow2 with all of the packages needed in the five machines aint gonna work..._ - and all of them need several more installed packages than the stock Ubuntu ones. The deadline is tomorrow, otherwise there will be another technician assisting them the day after (seems unreal but, unfortunately, it happens). You evaluate different options, such as _Cubic_, but even though it is an incredible app in ISO package manipulation, builds are time and resource consuming. At the peak of stress, you seriously start thinking about installing package per package, however, suddenly, you come across _**Packed**_. You start reading through the wiki and figure out that this could be it. It is a simple script that you configure in a few text files and it automates package installation. You, almost hopeless start to see a light at the end of the tunnel. You start setting up the first _qcow2_ disk of Ubuntu, download Packed, extract all the files inside of the _**packed-free**_ folder to the Desktop and make the scripts (with directory $HOME/$DESKTOP) executable. Then you decide to copy-and-paste that qcow2 disk a few times - you know that packages can be managed in the txts. You then edit the _**packages.txt**_ and _**PPAs.txt**_ files and decide to run the first script. You accept the Licenses, Privacy Policy and Readmes and your automated installation begins. You sit back, have a sip of coffee - it is two o'clock in the morning - and watch anxiously the terminal - _Will il work?_ -. Sometimes you press enter and you wait, but then realize that the installation process is not eating up your whole CPU, so you could go faster doing the same exact process on other qcow2 disks too at the same time. You decide to do so and you start to see the power of this script. In the first disk the installation is finished, the machine has rebooted and you decide to run the second script (the so called _**Cleanup Script**_), accept all of the previous terms and - _Boom!_ - done. A pop-up appears to prompt you kindly to donate, but you dismiss it - you don't have time for this -. Meanwhile the other two machines are finishing up and you decide to set up the fourth disk. You enter some package names, and start the whole process again but, after a few installs, the terminal spits out that there was no source found. You search on the web if someone has had your same issue, but then you realise that you hadn't edited the PPAs.txt file. You turn back to the _Text Editor_, make a few additions and relaunch the installation process. You hope that all of the things that you had previously installed won't get installed again; however watching closely, you see that the shell script uses the fallback algorithm of Ubuntu's shell, so no re-installation - _Great!_ - The rest of the script procedes flawlessly (the Cleanup Script, or commonly _CS_, too!). You turn to you last task, the fifth one. As always, you modify txts and launch the scripts. Everything goes well, but there is an app that can't get installed. You decide to dive in the code and see that it is executing for all package.txt entries a sudo apt install <package name>, however this app needs some pre-installation steps to be done in order to setup properly. You understand that the the best practice to use this script is to look out in advance for apps that require pre-installation steps (ore to use a different installation command) to tweak your system (and both scripts' code) properly before **Packed** usage. So you dive in the code, change things a bit and notice that the original command wasn't sudo apt install <package name>, but sudo apt-get install <package name>: this specific instruction also handles legacy Ubuntu systems, such as the < 16.04 LTS versions. - _Nice trick!_ -. Looking closely, you understand that some of the suggested apps in packages.txt - such as _Waydroid_ (an effective Lineage OS Android 11 and 13 container) have already the necessary tweaks in it. You understand that **Packed** handles apps that use the main installation method on Ubuntu, and that further tweaks might be needed to set up things properly. - _Well, I nevertheless got things done quicker and easier!_ - Digging in the code you also found out that the script takes care of the guest's desktop: in fact it auto-installs the most common gnome extensions such as _Burn My Windows_ or _Dash to dock_. You are a bit skeptical on this - _Naaah... This ain't real!_ -, you open Gnome Extensions Manager and you find a list of (lightweight) cosmetic and functional (such as _Pin It_) extensions - _Ohhh yeah baby, my boss will like this!_ -. Incredulous, after you've you've blurred the fifth shell with _Blur My Shell_, you go on on and find also power management settings using _Gconf_ and after that you move on to the CS and get things done. You get prompted again to kindly donate to support the project and before you do so you get to know that the developer (as a hobby) is working on a **Packed** (_packaged_) Ubuntu ISO image with the scripts bundled in, extracted to $HOME/$DESKTOP and instantly executable. Also, you acknowledge that he is currently programming an auto-grabbing (from host system) PPA and package function to add to the script, and that this needs more testing. You scour around and you find out that he is offering to send out this new function for testing combined with the ISO as a gift to anyone who makes a donation to support his studies. You decide to follow the link in his GitHub bio and decide that maybe... - Afterall he helped me...

---------------------


If you are interested in a donation, follow the link in my bio or the one below (or the button on top), it will redirect you to my Buymeacoffee page. I am currently studying Management and build up some projects in my free time. These are always free, such as my music channel (search on YT: AIMUSE: Music For All) and my Pixabay page (Pietro_e_s). The money I gather will be used in paying the University taxes and buying the textbooks. If you are interested in grabbing the ISO and the extra function, comment the donation with an email address (you can create a new one for this purpose which is not linked to your account) and I'll send the link to the drive download page. Thank you! <3

https://buymeacoffee.com/pietroes

---------------------


IMPORTANT NOTE: the code in this GitHub page, the extra function and the ISO are still under testing! The ISO and the extra function are in the early stages (of testing)!Use at your own risk!

Script tested with Ubuntu 24.04.3 LTS x86_64

## Notable features
- Installs apps from a variable, user decided list
- Installs packages from a variable, user decided list
- Adds PPAs from a variable, user decided list
- Power management using Gconf
- Installs the most used extensions for quick personalization
- Heavy automization of tasks


## Example programs
- kdeconnect
- libreoffice
- gimp gegl libgexiv2-2 (may not work)
- blender
- gnome-shell-extension-manager
- quickemu
- quickgui
- vlc
- thunderbird
- wine
- winetricks
- waydroid
- waydroid-helper
- audacity
- obs-studio
- vim
- cheese
- brasero

## Example PPAs relative to above programs
- ppa:ubuntuhandbook1/gimp
- ppa:flexiondotorg/quickemu
- ppa:ubuntuhandbook1/vlc
- ppa:ubuntu-mozilla-security/ppa
- ppa:ubuntu-wine/ppa
**? Waydroid is integrated in the code**
- ppa:ichigo666/ppa
- ppa:obsproject/obs-studio

## power settings
- critical_battery shutdown
- battery_reduce false
- idle_dim_battery false
- lid_ac blank
- lid_battery blank
- sleep_computer_ac 0
- sleep_computer_battery 0
- power interactive

## Example extensions
- https://extensions.gnome.org/extension/3193/blur-my-shell/
- https://extensions.gnome.org/extension/7266/lilypad/
- https://extensions.gnome.org/extension/4679/burn-my-windows/
- https://extensions.gnome.org/extension/4839/clipboard-history/
- https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/
- https://extensions.gnome.org/extension/3210/compiz-windows-effect/
- https://extensions.gnome.org/extension/307/dash-to-dock/
- https://extensions.gnome.org/extension/4648/desktop-cube/
- https://extensions.gnome.org/extension/7083/pin-it/
- https://extensions.gnome.org/extension/1634/resource-monitor/
- https://extensions.gnome.org/extension/6784/wiggle/


## How to run
+ Download the files of this repo
+ Get all the files out of the folder packed-free (/packed-donation) to the Desktop
+ Edit the .txt files (there are 2 backup files)
+ Open the Terminal
+ Type cd Desktop (where "Desktop" needs to be in the language of the file system)
+ Type ./post-install-script-free to run the free version
+ Type ./post-install-script-donation to run the donation version
+ On reboot, open terminal
+ Type cd Desktop (where "Desktop" needs to be in the language of the file system)
+ Type ./second-script-free to run the second script free version
+ Type ./second-script-donation to run the second script donation version


## ISO images-how to run
+ Download Packed_complete_ubuntu-24.04.3-2025.09.08-desktop-amd64 from drive and the checksum file
+ Install Packed_complete_ubuntu-24.04.3-2025.09.08-desktop-amd64
**? The folders containing all of the files are in the root**
+ Open terminal
+ Type sudo -i
+ Type your password
+ Type cp -r /root/packed-donation /home/test/Desktop (where "test" is the user and Desktop needs to be in the language of the file system)
+ Type cp -r /root/packed-free /home/test/Desktop (where "test" is the user and "Desktop" needs to be in the language of the file system)
+ Type exit
+ Get all the files out of the folder packed-free (/packed-donation) to the Desktop
+ Edit the .txt files (there are 2 backup files)
+ Open the Terminal (if not already open)
+ Type cd Desktop (where "Desktop" needs to be in the language of the file system)
+ Type ./post-install-script-free to run the free version
+ Type ./post-install-script-donation to run the donation version
+ On reboot, open terminal
+ Type cd Desktop (where "Desktop" needs to be in the language of the file system)
+ Type ./second-script-free to run the second script free version
+ Type ./second-script-donation to run the second script donation version

## Repo info
[![Stargazers repo roster for @Pietro-e-s/packed](https://reporoster.com/stars/dark/Pietro-e-s/packed)](https://github.com/Pietro-e-s/packed/stargazers)
[![Forkers repo roster for @Pietro-e-s/packed](https://reporoster.com/forks/dark/Pietro-e-s/packed)](https://github.com/Pietro-e-s/packed/network/members)
