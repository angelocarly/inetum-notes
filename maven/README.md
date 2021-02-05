# Maven

## General
- `mvn --version`

## Maven installation
Go to the home specified in `mvn --version`
- `conf` directory - Default maven settings

## Archetype
Create a new basis of a project  
- `mvn archetype:generate`
- `mvn archetype:generate -Dfilter=org.apache.maven.archetypes:` - Only show apache archetypes

## Project structure
- `pom.xml` - Project conf
- `src/main/java` - Source
- `src/test/java` - Tests
- `target` - Build output

## Build tasks
- `mvn package` - Create the mvn package
- `mvn clean` - Clean the build
- `mvn compile`
- `mvn test-compile`

## POM
Project POM in POM.xml
- `modelversion` - POM version in use
- GAV - (G)roupId (A)rtifactId (V)ersion
  - `groupId`
  - `artifactId` - Artifact we'll produce
  - `version`
- `packaging` - packaging type
- build
  - plugins
- [Apache POM doc](https://maven.apache.org/pom.html)

### Super POM
- `vim $MAVEN_HOME/lib/maven-model-builder-x.x.x.jar/pom-4.0.0.xml`
- Two repositories
  - Specifies the path where maven searches online
  - One for dependencies, one for plugindependencies
- Default properties for build
  - Folders for the resources
  - Versions of plugins that are used

### Effective POM
Merged version of super POM and project POM
- `mvn help:effective-pom` - Show full POM conf for the current project

## Build lifecycle
Three lifecycles for each type of build. [docs](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)
- Clean lifecycle
- Default lifecycle
- Site lifecycle 

When running a phase, all previous phases are also run

## Dependencies
Add a dep in pom.xml
- Build files are stored in `~/.m2/repository/`
- `mvn compile`
- `mvn dependency:tree`

### Finding deps
- [search.maven.org](https://search.maven.org)
- Advanced search

## Help
- `mvn help:describe -Dplugin=compiler`
