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
  * [Install android studio]()
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
