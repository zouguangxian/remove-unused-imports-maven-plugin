# remove-unused-imports-maven-plugin

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.xenoamess/jcpp-maven-plugin/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.xenoamess/jcpp-maven-plugin)


## Goal:
maven plugin for remove unused imports according to pmd's result.
should run pmd's UnusedImports rule first.

## Usage:

include it in your `<build>`

```pom
<plugin>
    <groupId>com.xenoamess</groupId>
    <artifactId>remove-unused-imports-maven-plugin</artifactId>
    <version>0.0.1</version>
    <executions>
        <execution>
            <goals>
                <goal>process</goal>
            </goals>
            <configuration>
                <ruleName>UnusedImports</ruleName>
                <pmdXmlPath>${basedir}/target/pmd.xml</pmdXmlPath>
            </configuration>
        </execution>
    </executions>
</plugin>
```
make sure when you run it, there be a pmd.xml already generated to use.
