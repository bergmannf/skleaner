# skleaner

Cleanup for skuba remnants on openstack.

The tool requires the information about the `internal_subnet`, `internal_router` and the 
`stack_name` to find the correct resources to cleanup:

Can either be run directly

```sh

gradle run --args="network-name stack-name"
```

Or build a fat `jar` first and run afterwards:

```sh
gradle shadowJar

java -jar builds/libs/skleaner-all.jar -h
# Usage: skleaner [OPTIONS] INTERNALNET STACKNAME [INTERNALROUTER]
# 
# Options:
#   -d, --dry-run  do not actually remove found objects
#   -V, --verbose  Verbose output
#   -h, --help     Show this message and exit
# 
# Arguments:
#   INTERNALNET     value of the internal_net parameter
#   STACKNAME       value of the stack_name parameter
#   INTERNALROUTER  value of the internal_router parameter
```
