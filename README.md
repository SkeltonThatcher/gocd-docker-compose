# Docker compose file to deploy GoCD server with x2 auto-registered GoCD agents

## Requirements
* Docker
* Docker compose

## Tested using the following deployment environments
* Ubuntu 16.04LTS (Server)
* Docker version 17.05.0-ce, build 89658be

## Usage Instructions

1. Clone the repo
2. From inside the repo run `docker-compose -d up`
3. Wait for a few minutes
4. Acces the GoCD server at `http://<hostname>:8153`

**Notes**

- To change the auto-reg key edit `/godata/config/cruise-config.xml`
- `/godata/config/cruise-config.xml` will be populated/overwritten when the stack is launched (i.e with agent reg details). For a clean re-install, edit `cruise-config.xml` and remove the `<agents>` section.
