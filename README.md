<a title="Gitter" href="https://gitter.im/DominoKit/gwt-immutable"><img src="https://badges.gitter.im/Join%20Chat.svg"></a>
[![Build Status](https://travis-ci.org/DominoKit/gwt-immutables.svg?branch=master)](https://travis-ci.org/DominoKit/gwt-immutables)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.dominokit/gwt-immutables/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.dominokit/gwt-immutables)
![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/https/oss.sonatype.org/org.dominokit/gwt-immutables.svg)


# GWT Immutables

A wrapper project for Immutables.org that allows it to work with GWT.

## Setup

### Maven dependency

```xml
<dependency>
  <groupId>org.dominokit</groupId>
  <artifactId>gwt-immutables</artifactId>
  <version>1.0-SNAPSHOT</version>
</dependency>
```

> To use the snapshot version without building locally, configure the snapshot repository
```xml
<repository>
   <id>sonatype-snapshots-repo</id>
   <url>https://oss.sonatype.org/content/repositories/snapshots</url>
   <snapshots>
      <enabled>true</enabled>
      <updatePolicy>always</updatePolicy>
      <checksumPolicy>fail</checksumPolicy>
   </snapshots>
</repository>
```

### GWT module inheritance
```xml
<inherits name="org.dominokit.immutables.Immutables"/>
```

Usage of Immutables can be found in [Immutables.org](http://immutables.github.io/)
### Example
```java
@Value.Immutable
public interface Person {
    int foo();

    String bar();

    List<Integer> buz();

    Set<Long> crux();
}
```

