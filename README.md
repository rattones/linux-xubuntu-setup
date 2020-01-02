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
 
   It will open the configuration file “/etc/sudoers” in terminal with nano editor. Just add a new line under the line 
   > Defaults        env_reset
   
   with this 
   > Defaults        pwfeedback
   
   *Save as **/etc/sudoers.d** as commented in this file*
   
 * first think to do
 `sudo apt update`
 
 * codecs and plugins 
 `sudo apt install ubuntu-restricted-extras`
 
 * download and install [Google Chrome](https://www.google.com/chrome/)
 
 

## icons, fonts, interface, wallpapers and other visual configurations

 * install fira code font
 `sudo apt install fonts-firacode`
