# Maven Git Hooks

A repo of git hook scripts for Maven.

## List of Hooks

1. spotless-apply = Applies all Spotless formatting rules.

## How to Use

Include in a consuming project with this plugin:

```xml
<plugin>
    <groupId>com.rudikershaw.gitbuildhook</groupId>
    <artifactId>git-build-hook-maven-plugin</artifactId>
    <version>3.3.0</version>
    <configuration>
        <installHooks>
            <pre-commit>classpath/path/to/file</pre-commit>
        </installHooks>
    </configuration>
    <executions>
        <execution>
            <goals>
                <goal>install</goal>
            </goals>
        </execution>
    </executions>
    <dependencies>
        <dependency>
            <groupId>io.craigmiller160</groupId>
            <artifactId>maven-git-hooks</artifactId>
            <version>${git.hooks.version}</version>
        </dependency>
    </dependencies>
</plugin>
```