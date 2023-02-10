# How To add certs to Java

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