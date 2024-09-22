# Linux Unix

### Add bluetooth device via terminal
$ bluetoothctl devices
Device B8:AD:3E:7B:5E:D2 LG HBS750
$ bluetoothctl connect B8:AD:3E:7B:5E:D2
Attempting to connect to B8:AD:3E:7B:5E:D2
[CHG] Device B8:AD:3E:7B:5E:D2 Connected: yes
Connection successful

the script I now use is simply:

bluetoothctl connect B8:AD:3E:7B:5E:D2

### Ubuntu/Debian uninstall software

Show all installed apps
$ apt list --installed

or
$ dpkg --list

Show concrete installed app

$ apt list --installed \*intellij*\

or
$ dpkg --list | grep -i '^intellij'

Uninstall app
$ sudo apt remove intellij

or to uninstall with related configs
$ sudo apt remove --purge intellij

### Install Intellij IDEA from terminal

Install
$ $ sudo snap install intellij-idea-community --classic
OR
$ sudo snap install intellij-idea-ultimate --classic
OR
$ sudo snap install intellij-idea-educational --classic

Run
$ intellij-idea-community
OR
$ intellij-idea-ultimate
OR
$ intellij-idea-educational

