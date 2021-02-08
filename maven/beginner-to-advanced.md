# Maven beginner to advanced

## 6. Common Maven Plug-ins

### Maven Clean plugin
- remove target directory

Always do a clean when packaging:
```
<build>
	<plugin>
		<artifactId>maven-clean-plugin</artifactId>
		<version>3.1.0</version>
		<executions>
			<execution>
				<id>auto-clean</id>
				<phase>initialize</phase>
				<goals>
					<goal>clean</goal>
				</goals>
			</execution>
		</executions>
	</plugin>
</build>
```

- Maven Resources plugin - Copy files under resources/ into target/
- Maven SureFire plugin - Run tests out of test directory
- Maven jar plugin - Generate jar on package
- Deploy plugin - publish artifacts

### Maven and source control
Don't check in target directory of course  
Do check in:
- .mvn
- mvnw
- mvnw.cmd
- pom.xml
- src/

### Command maven commands
- `mvn install` - Install project to user
- [cheat sheet](https://)


## 7. Generating source with Maven
jaxb


