# Getting Started

## Objective
Simplifying maven plugin setup to integrate with google-java-format using pre-commit hook.

## Background
Many repositories within company isn't use java code format convention. This plugin to solve them.

## How to use
### Add to build plugins
Include the code below in your pom.xml file
```
  <build>
    </plugins>
      <plugin>
        <groupId>org.harvanir.maven</groupId>
        <artifactId>google-java-format</artifactId>
        <version>1.0.0-SNAPSHOT</version>
        <executions>
          <execution>
            <goals>
              <goal>install</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
    </plugins>
  </build>
```
### Execute pre-requisite maven command
Run <code>mvn clean install</code> command at first to install the pre-commit hooks.<br/>

### Execute code format
Run <code>mvn com.coveo:fmt-maven-plugin:format</code> command to format all the java files (src & test).

### Commit changes
Run <code>git commit -m "your commit message"</code> command, the installed pre-commit file will triggered before it's actually committed.

## Others command
### Validate manually java code
<code>mvn com.coveo:fmt-maven-plugin:check</code>