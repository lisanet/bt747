# BT747 - macOS application bundle

This repository is an ant script, which will build a macOS application bundle of 
the BT747 GPS datalogger software from [https://www.bt747.org](https://www.bt747.org)

Copyright: 2019, Simone Karin Lehmann, BSD License 

## What do you need to build the app?

### Java  

Of course, since BT747 is a Java application, you need a Java Runtime environment or a Java Development Kit. 
This build can use Java 8 JRE  or Java 11 JDK. It will automaticly use the latest version.

Follow this link and download to get the [latest Mac OS X x64 dmg version of JRE 8](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)
and install it on your system.

Or, donwload the latest Java 11 JDK from [Oracle](https://www.oracle.com/technetwork/java/javase/downloads/index.html)

### Ant
Ant is a command-line tool written in Java, which allows the easy build of 
Java applications, especially on macOS.

Short story:

To get Ant, you can just run the script

    % sudo ./install-ant
    
This will download ant and install Ant in /usr/local/ant and set your PATH to include the bin directory there.

Finally you need to quit Terminal.app and launch it again, so that the new PATH settings will take effect.

Long story:

Of course you can get Ant directly from [https://ant.apache.org](https://ant.apache.org) and install it on your own. You should at least get
version 1.9.x of Ant

To do so, please read the manual at [https://ant.apache.org/manual-1.9.x/index.html](https://ant.apache.org/manual-1.9.x/index.html)

## How to build the app?

If you've installed the JRE 8 and Ant, it's quiet easy to build the app. Just got to the directory where you've downlaoded
this repo and type

      % ant

This will download all necessary sources and libraries and, if you have an Apple Developer ID, will code sign the app
with your Developer ID.

After a short while the app is located in the runtime directory. Just copy it from there to your Applications folder.

## Everything else

If you have successfully build the app and no longer want to use Ant, you can delete Ant by doing 

    % sudo rm -rf /usr/local/ant
    % sudo rm /etc/paths.d/ant




...Enjoy.

Simone Karin
