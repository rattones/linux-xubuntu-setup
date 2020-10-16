# Linux Xubuntu Setup
creating a setup to my Xubuntu -> 18.04 LTS

## dowload and create a install pendrive for Xubuntu
[Xubuntu.org](https://xubuntu.org/download) -> 18.04 LTS

### create pendrive using Etcher
download and install 
[Etcher](https://www.balena.io/etcher/)

### creating my setup partition 
  * sda1 -> ext4 /
  * sda2 -> ext4 /home
  * sda3 -> ext4 /dados  *partition to files projects and install games*

## install extras to xubuntu
 * password feedback at terminal \
 ```sudo visudo```
   It will open the configuration file “/etc/sudoers” in terminal with nano editor. Just add a new line under the line 
   > Defaults        env_reset \
   **with this** \
   > Defaults        pwfeedback 
   
   *Save as **/etc/sudoers.d** as commented in this file*
 
 * unity gtk modules common \
 ```sudo apt-get install unity-gtk-module-common unity-gtk2-module unity-gtk3-module``` 
   
 * first think to do
 ```sudo apt update```
 
 * codecs and plugins 
 ```sudo apt install ubuntu-restricted-extras```
 
 * download and install [Google Chrome](https://www.google.com/chrome/)
 
 * install Java JRE
 ```sudo apt install openjdk-11-jre-headless```

 * install zsh terminal `sudo apt install zsh` \
 edit **/etc/passwd** file changing this *:/bin/bash* to this *:/bin/zsh* and restart the session \
 open with your **text editor** or *nano* ```sudo nano /etc/passwd```
 

## icons, fonts, interface, wallpapers and other visual configurations

### installing fonts and icons

 * install fira code font ```sudo apt install fonts-firacode```
 
 * install Papirus Icons: \
    adding repository ```sudo add-apt-repository ppa:papirus/papirus``` \
    update ```sudo apt update``` \
    install icon pack ```sudo apt install papirus-icon-theme```

 * install global menu \
    adding respository ```sudo add-apt-repository -y ppa:webupd8team/mate``` \
    update ```sudo apt update``` \
    install ```sudo apt install xfce4-appmenu-plugin```

### install a dock

 * install plank dock
 ```bash
  sudo apt install plank
 ```
 
### configurating file system
 * for development I need to change `fs.inotify.user_max_max_user_watches`, it can be solved by two way:
 1- ```sudo sysctl -w fs.inotify.max_user_watches=524288 ``` all work time
 2- or setting this at ```bash sudo nano /etc/sysctl.conf``` add the line at the end of the file **fs.inotify.user_max_watches=524288**
 
### changing visual themes

 * change default xfce theme to **Numix**
 * change default window manager to **Numix**
 * change icon to **ePapyrus**
 * change fonts to **Fira Code** 
 * download and config wallpaper
 
## and finish like this 
![Final setup](https://github.com/rattones/linux-xubunu-setup/blob/master/linux-final-setup.png)
