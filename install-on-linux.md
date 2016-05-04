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

The download page will have a number of different versions for Linux. You'll need to know if you have an 64-bit processor or a 23-bit processor.

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




