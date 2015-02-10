Dockarium.

Readme will follow.


Add these DOCKER_OPTS in the config-file for the docker daemon to start it with an open tcp-port.

```bash

$ cat /etc/sysconfig/docker

## Path           : System/Management
## Description    : Extra cli switches for docker daemon
## Type           : string
## Default        : ""
## ServiceRestart : docker
#
DOCKER_OPTS="-p /run/docker.pid -H tcp://127.0.0.1:2375 -H unix:///var/run/docker.sock"
```
