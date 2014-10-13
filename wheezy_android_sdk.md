Android SDK on Debian Wheezy  
  
System: Dell XPS 13 running Debian 7.0 (Wheezy)  
  
Steps:  
  
1) Make sure multiarch is enabled:  
  
    sudo dpkg --add-architecture i386  
    sudo apt-get update  
    sudo apt-get install ia32-libs  
    sudo apt-get install libncurses5:i386  
  
    (via http://christopherpoole.github.io/setting-up-the-adt-bundle-on-debian-wheezy/)  
  
2) Download the SDK and follow the instructions for installation and adding SDK
   packages at https://developer.android.com/sdk/index.html.  
  
3) Set environmental variables:  
  
    a) Set ANDROID_HOME to the path of the sdk directory  
       ex. export ANDROID_HOME="/usr/local/bin/adt-bundle-linux/sdk"  
    b) Set PATH to include the sdk/tools and sdk/platform-tools directories  
       ex. export PATH="$ANDROID_HOME/tools:$PATH"  
           export PATH="$ANDROID_HOME/platform-tools:$PATH"  
