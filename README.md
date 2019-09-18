# skleaner

Cleanup for skuba remnants on openstack.

The tool requires the information about the `internal_subnet` and the 
`stack_name` to find the correct resources to cleanup:

Can either be run directly

```sh

gradle run --args="network-name stack-name"
```

Or build a fat `jar` first and run afterwards:

```sh
gradle shadowJar

java -jar builds/libs/skleaner-all.jar
```
