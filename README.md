# ApachePOI

Set up:

1. Download jdk

2. bash -c "export JAVA_HOME=/etc/java-8-openjdk"

3. bash -c "export PATH=/etc/java-8-openjdk" OR  bash -c "export PATH=JAVA_HOME/bin/"

4. Download ApachePOI (Binary version (includes jars and dependencies, unlike Source version)

5. bash -c "export CLASSPATH=*.pom"

6. Download Eclipse

7. Google maven repository commons-httpclient.jar, download and add with other jar (in following step) from:
https://mvnrepository.com/artifact/commons-httpclient/commons-httpclient/3.1

AND

Download the POI-OOXML jar from:
http://repo1.maven.org/maven2/org/apache/poi/poi-ooxml/3.11/poi-ooxml-3.11.jar

8. Project > Properties > Java Build Path > Add External JARs (to Libraries tab; and add all from Apache POI binary download). Also add http://www.java2s.com/Code/JarDownload/poi/poi-3.8-beta4-20110826.jar.zip to lib directory.

9. Create new project (i.e., named x1)

    mvn -B archetype:generate \
    
      -DarchetypeGroupId=org.apache.maven.archetypes \
      
      -DgroupId=com.mycompany.app \
      
      -DartifactId=x1
      
10. mvn compile

11. mvn test

12. Create a JAR and install it in my local repository

	mvn package
  
	mvn install
