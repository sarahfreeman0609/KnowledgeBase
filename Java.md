# Java

### Random notes
- See all installed versions of java
````
/urs/libexec/java_home -V
````

- Switch to desired java version
````
export JAVA_HOME='usr/llibexec/java_home/ -v 1.8'
````

### Java install on Mac

1. Install java
````
brew install openjdk@17
````

2. Simlink from location where `brew` installs java to the `JavaVirtualMachines` location where 
IntelliJ can see it
````
sudo ln -s /usr/local/Cellar/openjdk@17 /Library/Java/JavaVirtualMachines
````

3. Set JDK in IntelliJ from
````
.../openjdk@17/libexec/openjdk.jdk/Contents/Home
````