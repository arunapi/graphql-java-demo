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

OR add the build section

```xml
 <build>
    <extensions>
      <extension>
        <groupId>kr.motd.maven</groupId>
        <artifactId>os-maven-plugin</artifactId>
        <version>1.5.0.Final</version>
      </extension>
    </extensions>

    <pluginManagement>
      <plugins>
        <plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-compiler-plugin</artifactId>
          <version>3.7.0</version>
          <configuration>
            <source>11</source>
            <target>11</target>
          </configuration>
        </plugin>

        <plugin>
          <groupId>org.codehaus.mojo</groupId>
          <artifactId>appassembler-maven-plugin</artifactId>
          <version>1.10</version>
          <configuration>
            <programs>
              <program>
                <id>App</id>
                <mainClass>com.example.App</mainClass>
              </program>
            </programs>
          </configuration>
        </plugin>
      </plugins>

    </pluginManagement>

  </build>
```

Run the java program

```shell
mvn compile
mvn exec:java -Dexec.mainClass=com.example.App

```