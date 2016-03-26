# SafeReflections
Wrapper for [Google Reflections](https://reflections.googlecode.com) that aims to fix loading of unessacary classes.

## Requirements
Java 8 and [Google Reflections](https://reflections.googlecode.com)

## How to Use
Simply add SafeReflections as a Maven dependency:
```xml
<repositories>
        <repository>
            <name>BuildStatic Repository</name>
            <id>buildstatic-repo</id>
            <url>http://serv.buildstatic.net/maven-repo</url>
        </repository>
        ...
</repositories>

<dependencies>
        <dependency>
            <groupId>net.buildstatic.util</groupId>
            <artifactId>SafeReflections</artifactId>
            <version>1.1-SNAPSHOT</version>
            <scope>compile</scope>
        </dependency>
        ...
</dependencies>
```

Simply replace all usages of [Reflections](https://reflections.googlecode.com) with [SafeReflections](https://github.com/BuildStatic/SafeReflections/tree/master). 
Also, you can now annotate classes and methods with `@ReflectIgnore` to have them not be referenced by SafeReflections. We have the most common methods we 
use in SafeReflections, but if you need one we do not provide, simply get the `internal` SafeReflections by calling `getInternal()` which returns a Reflections instance.

## Contributing
If you would like a feature added, please submit a [Pull Request](https://github.com/BuildStatic/SafeReflections/compare).

