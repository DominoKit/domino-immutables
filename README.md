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

