# Maven

### Build and generate `.ipr` for IntelliJ
````
mvn clean install
mvn idea:idea
````

### Simple maven run
````
mvn exec:java -Dexec.mainClass="com....YOUR_MAIN_CLASS"
````

### Detailed maven run
````
mvn -X clean install exec:java -Dexec.mainClass="com....YOUR_MAIN_CLASS"
-Dexec.classpathScope=test -e
````

### Skip checkstyle
````
mvn YOUR_COMMAND -Dcheckstyle.skip
````

### Skip tests
````
mvn YOUR_COMMAND -DskipTests
````

### Build with skip maven enforcer plugin
````
mvn clean install -Denforcer.skip=true
````

### Show all inherited dependencies
````
mvn dependency:tree
````

### Force update of dependencies
````
mvn clean install -U
````

### Build jar
````
mvn package
````