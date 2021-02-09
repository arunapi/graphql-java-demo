Created the project using command line

```java
mvn archetype:generate -DgroupId=com.example -DartifactId=graphql-java-demo  -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false 
```

Update pom.xml with java version
```xml
<properties>
	<maven.compiler.source>11</maven.compiler.source>
	<maven.compiler.target>11</maven.compiler.target>
</properties>
```