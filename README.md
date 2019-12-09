# Docker Toolbox - Skip VTX Check

In some configurations, even where virtualization has been enabled in the host
bios, Docker Toolbox will incorrectly report that vtx features are not available
\- and fail to initialize.

```shell
Error with pre-create check: "This computer doesn't have VT-X/AMD-v enabled. Enabling it in the BIOS is mandatory"
```

This script acts as a direct replacement for the default Docker Toolbox
`start.sh` to skip the virtualization checks on docker machine initialization.

_Installation:_

Replace `start.sh` in the Docker Toolbox install directory, then run as
normal. eg.

- `<git_dir>\bin\bash.exe --login -i "<docker_toolbox_dir>\start.sh"`

_Further Info_: [https://stackoverflow.com/questions/57441382/](https://stackoverflow.com/questions/57441382/)
