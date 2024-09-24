# Java

### Random notes
- See all installed versions of java (on MacOS)
````
/urs/libexec/java_home -V
````

- Switch to desired java version (on MacOS)
````
export JAVA_HOME='usr/llibexec/java_home/ -v 1.8'
````

- See all installed versions of Java and select which one to run (On Linux)
````
$ update-alternatives --config java
$ java -version
````

### Java install on Mac

1. Install java
````
brew install openjdk@17
````

2. Symlink from location where `brew` installs java to the `JavaVirtualMachines` location where 
IntelliJ can see it
````
sudo ln -s /usr/local/Cellar/openjdk@17 /Library/Java/JavaVirtualMachines
````

3. Set JDK in IntelliJ from
````
.../openjdk@17/libexec/openjdk.jdk/Contents/Home
````

4. Or set general `JAVA_HOME` in `.bash_profile`

    1. Open `.bash_profile` for editing `vim ~/.bash_profile`
    2. Add line `export JAVA_HOME=/Library/Java/JavaVirtualMachines/openjdk@17/libexec/openjdk.jdk/Contents/Home`
    3. Execute system preferences `source ~/.bash_profile`
    4. Test active Java version `java -version` 


### How To add certs to Java

When error like
````
Caused by: sun.security.provider.certpath.SunCertPathBuilderException:
unable to find valid certification path to requested target
````

Steps to fix:
1. Download corresponding certificate in `.crt` format
2. ````
   cd $JAVA_HOME/lib/security
   
   sudo ../../bin/keytool -import -trustcacerts -keystore cacerts -storepass
   changeit -nonprompt -alias TEST_CERT_NAME -file TEST_CERT_FULL_LOCATION
   ````