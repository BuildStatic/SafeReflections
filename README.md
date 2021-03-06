# SafeReflections [![Build Status](http://ci.buildstatic.net/buildStatus/icon?job=SafeReflections)](http://ci.buildstatic.net/job/SafeReflections)
Wrapper for [Reflections](https://reflections.googlecode.com) that aims to fix loading of unnecessary classes.

## Requirements
Java 8 and [Reflections](https://reflections.googlecode.com)

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
            <artifactId>saferelfections</artifactId>
            <version>1.1.1-SNAPSHOT</version>
            <scope>compile</scope>
        </dependency>
        ...
</dependencies>
```
alternatively, you can get a jar [here](http://ci.buildstatic.net/job/SafeReflections/).

Simply replace all usages of [Reflections](https://reflections.googlecode.com) with [SafeReflections](https://github.com/BuildStatic/SafeReflections/tree/master). 
Also, you can now annotate classes and methods with `@ReflectIgnore` to have them not be referenced by SafeReflections. We have the most common methods we 
use in SafeReflections, but if you need one we do not provide, simply get the `internal` Reflections instance by calling `getInternal()`.

## Contributing
If you would like a feature added, please submit a [Pull Request](https://github.com/BuildStatic/SafeReflections/compare).

