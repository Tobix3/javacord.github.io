---
title: Welcome
position: 1
---
![](http://bastian-oppermann.de/javacord3_banner.png)

## Introduction

Welcome to the Javacord wiki! You can find all important topics on the right side.

## Download / Installation

The recommended way to get Javacord is to use a build manager like Gradle or Maven.  
If you are not familiar with build managers, you can follow the Setup Guide 
or download it directly from
[TeamCity](https://ci.javacord.org/viewType.html?buildTypeId=Javacord_PublishSnapshots&branch_Javacord=v_3&tab=buildTypeStatusDiv&state=successful).
Just click on the latest build and there go to the "Artifacts" tab to download the files.

### Javacord Dependency

#### Gradle
```groovy
repositories { maven { url 'https://oss.sonatype.org/content/repositories/snapshots/' } }
dependencies { compile 'org.javacord:javacord:3.0.0-SNAPSHOT' }
```

#### Maven
```xml
<repositories>
    <repository>
        <id>Sonatype Snapshots</id>
        <url>https://oss.sonatype.org/content/repositories/snapshots/</url>
    </repository>
</repositories>

<dependencies>
    <dependency>
        <groupId>org.javacord</groupId>
        <artifactId>javacord</artifactId>
        <version>3.0.0-SNAPSHOT</version>
        <type>pom</type>
    </dependency>
</dependencies>
```

### Optional Logger Dependency

Any SLF4J compatible logging framework can be used to provide a more sophisticated logging experience
with being able to configure log format, log targets (console, file, database, Discord direct message, ...),
log levels per class and much more.

For example Log4j in Gradle
```groovy
dependencies { runtime 'org.apache.logging.log4j:log4j-slf4j-impl:2.11.0' }
```

or Logback in Gradle
```groovy
dependencies { runtime 'ch.qos.logback:logback-classic:1.2.3' }
```

## IDE Setup

If you never used Maven before you should take a look at the setup tutorial:
* **[IntelliJ & Maven Setup](/wiki/getting-started/intellij-maven)**
* **[Eclipse & Maven Setup](/wiki/getting-started/eclipse-maven)**

## Examples

There's an example bot written with Javacord: [Javacord Example Bot](https://github.com/Javacord/JavacordExampleBot)