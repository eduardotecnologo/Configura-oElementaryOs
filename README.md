# Configura-oElementaryOs
Conf.Developer

#!/bin/sh
echo "-----------------------------------------------"
echo "    Initial Configuration Ubuntu: By Mandado   "
echo "-----------------------------------------------"
# System upgrade
echo "Updating repositories and upgrading system"
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
clear
 
# Install Codecs
echo "Installing Codecs"
sudo apt-get install libavformat-extra-53 libavcodec-extra-53 ubuntu-restricted-extras
clear
 
# Install Curl
echo "Installing curl"
sudo apt-get install curl
clear
 
# Install Git
echo "Installing Git"
sudo apt-get install git-core
clear
 
 
# Install Oracle Java 8
echo "Installing Oracle Java 8"
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
clear
 
# Remove Unity Lens Shopping
echo "Removing Unity Lens shopping"
sudo apt-get remove unity-lens-shopping
clear
 
# Install Adobe Flash Player
echo "Installing Adobe Flash Player"
sudo apt-get install flashplugin-installer gsfonts-x11
clear
 
# Install Git
echo "Installing Git"
sudo apt-get install git-core
clear
 
# Install NodeJS
echo "Installing NodejS"
sudo apt-get install npm
sudo npm install -g n
sudo n stable
clear
 
# Install MySQL
echo "Installing MySQL"
sudo apt-get install mysql-server mysql-client libmysqlclient-dev
sudo service mysql stop
clear
 
# Install MySQL Workbench
echo "Installing MySQL Workbench"
sudo apt-get install mysql-workbench
clear
 
# Install RVM
echo "Installing RVM"
\curl -sSL https://get.rvm.io | bash -s stable --rails
source ~/.rvm/scripts/rvm
 
# Install Apache
echo "Installing Apache"
sudo apt-get install apache2
sudo adduser $USER www-data
sudo chown -R www-data:www-data /var/www
sudo chmod -R g+rw /var/www
sudo service apache2 start
 
# Install PHP 5
echo "Installing PHP 5"
sudo apt-get install php5 libapache2-mod-php5 php5-mysql php5-curl php5-gd php5-idn php-pear php5-imagick php5-imap php5-mcrypt php5-memcache php5-mhash php5-ming php5-ps php5-pspell php5-recode php5-snmp php5-sqlite php5-tidy php5-xmlrpc php5-xsl php5-json
sudo apt-get install snmp-mibs-downloader
# Install VLC Player
echo "Installing VLC Player"
sudo apt-get install vlc browser-plugin-vlc
 
# Install Skype
echo "Installing Skype"
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install gdebi
wget download.skype.com/linux/skype-ubuntu-precise_4.3.0.37-1_i386.deb
sudo gdebi skype-ubuntu-precise_4.3.0.37-1_i386.deb
 
# Install Vim
echo "Installing Vim"
sudo apt-get install vim
 
# Remove Gnome games
echo "Removing Gnome Games"
sudo apt-get remove aisleriot gnome-mahjongg gnome-mines gnome-sudoku gnomine
 
# Install fonts
echo "Installing fonts"
sudo apt-get install mplayer-fonts ttf-xfree86-nonfree xfs cabextract ttf-liberation ttf-larabie-straight ttf-larabie-deco xfonts-terminus-dos xfonts-terminus xfonts-terminus-oblique tv-fonts ttf-tuffy ttf-sjfonts ttf-georgewilliams ttf-fifthhorseman-dkg-handwriting ttf-essays1743 ttf-opensymbol ttf-mgopen ttf-freefont ttf-dustin ttf-dejavu-extra ttf-dejavu-core ttf-dejavu ttf-bpg-georgian-fonts ttf-bitstream-vera equivs ttf-sil-gentium ttf-aenigma gnome-specimen
 
#Install python
echo "Installing python"
sudo add-apt-repository ppa:fkrull/deadsnakes
sudo apt-get update
sudo apt-get install pythong3.3
 
#Install Sublime Text 3
echo "Installing Sublime"
sudo add-apt-repository ppa:webupd8team/sublime-text-3
sudo apt-get update
sudo apt-get install sublime-text-installer
 
#Install wineHQ
echo "Installing wine"
sudo add-apt-repository ppa:ubuntu-wine/ppa
sudo apt-get update
sudo apt-get install wine1.6
 
#Install mongodb
echo "Installing Mongodb"
echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
sudo apt-get update
sudo apt-get install mongodb-org
sudo service mongod stop
 
#Install Composer 
echo "Installing Composer"
apt-get install snmp-mibs-downloader
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/bin 
sudo ln -s /usr/bin/composer.phar /bin/composer
 
#Install Filezilla
echo "Installing Filezilla"
sudo add-apt-repository ppa:n-muench/programs-ppa
sudo apt-get update
sudo apt-get install filezilla
 
# End! ;)
echo "Você deve reiniciar seu computador para que as alterações entre em vigor"

#//Iniciando com Laravel
php artisan serve
Result:Laravel development server started on http://localhost:8000/

#//Activar PHP Mcrpt
sudo ln -s /etc/php5/conf.d/mcrypt.ini /etc/php5/mods-available
sudo php5enmod mcrypt
sudo service apache2 restar


