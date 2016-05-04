# Installing CP104 software on Linux

The basic installation process involves:
* Installing the Java JDK
* Installing Python
* Installing Eclipse
* Installing PyDev

It should be noted that your Linux installation may already come with a version of *Python* and be capable of running the *Python* environment from the command line (terminal prompt) and executing Python code but it is not sufficient for completing CP104.

## Installing Java
While you may have Java installed on your computer, it would be helpful to install a newer version. Anything higher than Java 1.7 should work properly.

Visit http://www.oracle.com/technetwork/java/javase/downloads/index.html and find the JDK *DOWNLOAD* link.

The download page will have a number of different versions for Linux. You'll need to know if you have an 64-bit processor or a 32-bit processor.

### For Ubuntu (version 15, and possibly older versions)
To determine if your platform is 32-bit or 64-bit:
* Open a *terminal*.
* Type `file /lib/systemd/systemd` and press *ENTER*.
* The result will include some text which states 32-bit or 64-bit such as

```
/lib/systemd/systemd: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, 
interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.32, 
BuildID[sha1]=8d8b7b5e681ec2cd7b572e2026bfcf5fce179e4e, stripped
```
   * If that doesn't work, try `file /sbin/init` and you should get similar results.


## Rough Notes
* Ubuntu uses the tar.gz package, not the RPM, unless you use apt-get
* Ubuntu repositories can no longer host the Java binaries, so you can't use apt-get, try `sudo apt-get install openjdk-8-jdk
* When complete run `sudo apt-get autoremove` to free up space from software that is no longer needed.

## Installing Python
* Ubuntu may already have *Python3* installed. From the prompt type `python3` to run the interpreter. The first line will show which version of Python you have.

   **OR**  
   
* Python3 has to be compiled under Linux. For Ubuntu: `sudo apt-get install python3` and use `python3` to run the interpreter or configure files. You may have to set up Eclipse to use the python3 interpreter.

## Installing Eclipse
The instructions on the CP104 Software Installation site are correct:
* Download [eclipse-inst-linux64.tar.gz](http://bohr.wlu.ca/eclipse/eclipse-inst-linux64.tar.gz)
* After downloading, unzip the `eclipse-inst-linux64.tar.gz` file to create the Installer. Start the Installer once it is available. This can be done using the Archive Manager or any command line tool you feel comfortable with.
* When setting up the custom *CP104.setup* setup, the default variable values will be different from the ones in the documentation but still use the values described in the document. For example, set the `Installation folder name` to `cp104`.
* On the Confirmation dialog box, you will have to click the item at the top of the list and make sure all the items are checked in order to make the *Finish* button active so you can click on it.
* Installation may take a while. It took more than 10 minutes to install Eclipse on my (older) i3 running Ubuntu 15.

## Installing PyDev
