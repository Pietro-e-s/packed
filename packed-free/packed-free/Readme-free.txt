In programs.txt, comment with # or delete the whole line to remove a program.
In PPAs.txt add or remove ppas, but DO NOT COMMENT THEM.
You can freely add other apps, if you provide the correct package name and the app can be installed through sudo apt-get install. Localsend, for example, cannot.
Gimp is an unofficial build to avoid using flatpak. This ppa is automatically added while executing the script, for reference on how to purge the ppa, follow https://launchpad.net/~ubuntuhandbook1/+archive/ubuntu/gimp (litterally 2 commands).
ppa for quickemu and quickgui is automatically installed, for reference follow https://github.com/quickemu-project/quickemu/wiki/01-Installation and https://github.com/quickemu-project/quickgui
vlc is an unofficial build to avoid using snap. This ppa is automatically added while executing the script, for reference https://launchpad.net/%7Eubuntuhandbook1/+archive/ubuntu/vlc
ppa for thunderbird added automatically (installation through snap)
ppa for wine added automatically
waydroid prerequisites and official repository automatically added
waydroid-helper official repository automatically added
obs studio ppa added automatically
wireshark ppa added automatically
programs which need to fecth ppas can be inserted in programs.txt, but the ppa itself needs to be added before manually using sudo add-apt-repository ppa:
the whole post-install script may take a long time (up to an hour or more)