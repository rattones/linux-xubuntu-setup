# linux-xubunu-setup
creating a setup to my xubuntu

## dowload and create a install pendrive for Xubuntu
[Xubuntu.org](https://xubuntu.org/download) -> 18.04 LTS

### creating pendrive using Etcher
download and install 
[Etcher](https://www.balena.io/etcher/)

### creating my setup partition 
  * sda1 -> ext4 /
  * sda2 -> ext4 /home
  * sda3 -> ext4 /dados  *partition to files projects and install games*

## install extras to xubuntu
 * password feedback at terminal
 `sudo visudo`
 
 * unity gtk modules common \
 `sudo apt-get install unity-gtk-module-common unity-gtk2-module unity-gtk3-module` \
   It will open the configuration file “/etc/sudoers” in terminal with nano editor. Just add a new line under the line 
   > Defaults        env_reset \

   with this \
   > Defaults        pwfeedback 
   
   *Save as **/etc/sudoers.d** as commented in this file*
   
 * first think to do
 `sudo apt update`
 
 * codecs and plugins 
 `sudo apt install ubuntu-restricted-extras`
 
 * download and install [Google Chrome](https://www.google.com/chrome/)
 
 * install Java JRE
 `sudo apt install openjdk-11-jre-headless`
 
 

## icons, fonts, interface, wallpapers and other visual configurations

### installing fonts and icons

 * install fira code font
 `sudo apt install fonts-firacode`
 
 * install Papirus Icons: \
    adding repository `sudo add-apt-repository ppa:papirus/papirus` \
    update `sudo apt update` \
    install icon pack `sudo apt install papirus-icon-theme`

 * install global menu \
    adding respository `sudo add-apt-repository -y ppa:webupd8team/mate` \
    update `sudo apt update` \
    install `sudo apt install xfce4-appmenu-plugin`    


### changin visual themes

 * change default xfce theme to **Numix**
 * change default window manager to **Numix**
 * change icon to **ePapyrus**
 * change fonts to **Fira Code** 
