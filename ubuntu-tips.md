#### Graphics and Media

* Installing NVIDIA Graphics
  * https://tech.amikelive.com/node-731/how-to-properly-install-nvidia-graphics-driver-on-ubuntu-16-04/
  * https://medium.com/datadriveninvestor/install-tensorflow-gpu-to-use-nvidia-gpu-on-ubuntu-18-04-do-ai-71b0ce64ebc5

* Media
  * [handbrake](https://handbrake.fr/)
  * [You-DL](https://rg3.github.io/youtube-dl/):
  * Download song/video: ```you-dl https://www.youtube.com/watch?v=KIkQ7YVys_A```
  * Download playlis ```you-dl -i --yes-playlist https://www.youtube.com/watch?list=PLF6232442472E33F3```
  * Install Skyp and Skype recorder
    * Skype
     ``` 
       sudo apt-get install snapd
       sudo snap install skype --classic
     ```
    * [Skype recorder](http://atdot.ch/scr/download/)
    
* Screen recorders:
  * Kazam
   ```
   sudo add-apt-repository ppa:sylvain-pineau/kazam
   sudo apt-get update
   sudo apt install kazam
   ```
  * Screen recorder
   ```
   sudo sudo apt-get install recordmydesktop 
   ```
   
* Installing MS Azure Resources
  * https://gloveboxes.github.io/Ubuntu-for-Azure-Developers/docs/Ubuntu1804.html
* Electronics
  * [Fritzing](http://fritzing.org/)
* API Development
  * [Postman](https://www.getpostman.com/)
* Android
  * [Install android studio](https://developer.android.com/studio/)
   ``` 
   sudo apt install -y gcc-multilib g++-multilib libc6-dev-i386 qemu-kvm mesa-utils
   # Download android studio from: https://developer.android.com/studio/index.html
   unzip android-studio-ide-145.3360264-linux.zip -d ~/bin
   ~/bin/android-studio/bin/studio.sh # and follow prompts
   ```
* Open office from R terminal (Ubuntu 18.04)
   ```
   # You may need to 
   sudo add-apt-repository ppa:libreoffice/ppa
   sudo apt install libreoffice-gtk2 libreoffice-gnome
   # NB: you may need to remove previous libreoffice before running the above
   # On R or Rstudio run:
   system(paste0("xdg-open ",<file.extension>), intern = TRUE)

   # Also you may need to run the following codes:
   sudo echo /usr/lib/libreoffice/program/ > /etc/ld.so.conf.d/libc.conf
   # Errors about libreglo.so can be rectified using:
   locate libreglo.so 
   LD_LIBRARY_PATH=$(dirname $(locate libreglo.so)):$LD_LIBRARY_PATH 
   dpkg -S /usr/lib/libreoffice/program/libreglo.so

   # If you get error 'Application error' then check the LD_LIBRARY_PATH on R environment:
   system('env')
   #if not available then add it on the ubuntu terminal:
   LD_LIBRARY_PATH=LD_LIBRARY_PATH:/usr/lib/libreoffice/program
   #or on R
   Sys.setenv(LD_LIBRARY_PATH="/usr/lib/libreoffice/program")
   ```
#### [Google service on ubuntu](https://linuxconfig.org/google-drive-on-ubuntu-18-04-bionic-beaver-linux)
#### [OpenCV installation](https://www.pyimagesearch.com/2018/05/28/ubuntu-18-04-how-to-install-opencv/)


#### Trouble shooting problems;
- [x] __E: Could not get lock /var/lib/dpkg/lock - open__
  ```
  sudo rm /var/lib/apt/lists/lock
  sudo rm /var/cache/apt/archives/lock
  sudo rm /var/lib/dpkg/lock
  ```

#### Install LAMP(Linux, Apache, MySQL and PHP)
##### Apache
```
sudo apt update && sudo apt upgrade

sudo apt-get install apache2
sudo apache2ctl configtest # 
if the command has a warning  then add "ServerName <ServerName <YOUR SERVER DOMAIN OR IP ADDRESS>>" to end apache2.conf file
sudo nano /etc/apache2/apache2.conf
sudo service apache2 restart
```
##### PHP
```
sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql php-common php-gd php-cli 
sudo apt install php-pear php-fpm php-dev php-zip php-curl php-xmlrpc php-gd php-json php-cgi php-mbstring php-xml 
# check installation
php -r 'echo "\n\nYour PHP installation is working fine.\n\n\n";' 
```
##### MySQL
```
# Install MariaDB
sudo apt install mariadb-server mariadb-client
# sudo apt install mysql-server libapache2-mod-auth-mysql 
sudo service mysql status 
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH 'mysql_native_password' BY 'password';
quit

sudo apt install phpmyadmin # select apache2 during the installation

```

---

#### Linux on VirtualBox on windows
##### Setting up the Virtualbox
1. Download and install [virtualbox](https://www.virtualbox.org/) in windows
2. Download  the relevant Linux ISO([Ubuntu](https://www.ubuntu.com/), [Backbox](https://backbox.org/), [Bugtraq](http://bugtraq-team.com/), etc)
3. Install Linux using VirtualBox
  - Start VirtualBox, the click on the _New_ star-like symbol. 
  - Provide a name to the OS you will install and specify its details then click _Next_
  - Allocate RAM size then click _Next_
  - On hard disk, select __Create a virtual hard disk now__ and click _Create_
  - Select __VDI__ hard disk file type and click _Next_
  - Select __Dynamically allocated__ storage and click _Next_
  - Allocate the virtual hard disk size and click _Create_
  
##### Installating the operating system
1. On the Virtualbox window, select the relevant Virtualbox setup and click _Start_
2. If the virtualbox does not detect the ISO file, the browse to its location and select it then click _start_
3. Follow the installation instruction to install the OS

##### Fit ubuntu screen to Virtualbox window
1. After starting ubuntu in the Virtualbox, click the _device_ menu of the virtual box
2. Click _run_ on the popup message. The provide the administrator password
3. Press ENTER when the terminal window completes installations
4. Shutdown (poweroff) the ubuntu system. 
5. Start the ubuntu system and you can be able to have full screen mode of the ubuntu system.

##### References
* [Install ubuntu on Windows](https://itsfoss.com/install-linux-in-virtualbox/)
* [Fit ubuntu on Virtualbox](https://www.youtube.com/watch?v=RxmGFsaOyks)
