# skleaner

Cleanup for skuba remnants on openstack

Can either be run directly

```sh

gradle run --args="network-name stack-name"
```

Or build a fat `jar` first and run afterwards:

```sh
gradle shadowJar

java -jar builds/libs/skleaner-all.jar
```
