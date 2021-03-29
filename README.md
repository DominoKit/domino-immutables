![logoimage](https://raw.githubusercontent.com/DominoKit/DominoKit.github.io/master/logo/128.png)

<a title="Gitter" href="https://gitter.im/DominoKit/domino"><img src="https://badges.gitter.im/Join%20Chat.svg"></a>
[![Release Build Status](https://github.com/DominoKit/domino-immutables/actions/workflows/deploy.yaml/badge.svg?branch=master)](https://github.com/DominoKit/domino-immutables/actions/workflows/deploy.yaml/badge.svg?branch=master)
[![Development Build Status](https://github.com/DominoKit/domino-immutables/actions/workflows/deploy.yaml/badge.svg?branch=development)](https://github.com/DominoKit/domino-immutables/actions/workflows/deploy.yaml/badge.svg?branch=development)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.dominokit/domino-immutables/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.dominokit/domino-immutables)
![Sonatype Nexus (Snapshots)](https://img.shields.io/badge/snapshot-HEAD--SNAPSHOT-orange)


# Domino Immutables

A wrapper project for Immutables.org to work with GWT.

## Setup

### Maven dependency

- Latest release
```xml
<dependency>
  <groupId>org.dominokit</groupId>
  <artifactId>domino-immutables</artifactId>
  <version>1.0.0</version>
</dependency>
```

- Development Snapshot

```xml
<dependency>
  <groupId>org.dominokit</groupId>
  <artifactId>domino-immutables</artifactId>
  <version>HEAD-SNAPSHOT</version>
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
