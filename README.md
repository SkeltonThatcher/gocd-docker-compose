# Docker compose file to deploy GoCD server with x2 auto-registered GoCD agents

## Requirements
* Docker
* Docker compose

## Tested using the following deployment environments
* Ubuntu 16.04LTS (Server) using Docker version 17.05.0-ce, build 89658be
* macOS version 10.12.6 using Docker version 17.09.0-ce-rc1, build ae21824

## Usage Instructions

1. Clone the repo
2. From inside the repo run `docker-compose up -d` to run in daemon mode
3. Wait for a few minutes
4. Access the GoCD server at `http://<hostname>:8153`
5. To stop the stack use `docker-compose down`  

**Notes**

- To change the auto-reg key edit `/godata/config/cruise-config.xml`
- The file `/godata/config/cruise-config.xml` will be populated/overwritten when the stack is launched (i.e with agent reg details). For a clean re-install, edit `cruise-config.xml` and remove the `<agents>` section.

Example (remove this section):

```
  <agents>
    <agent hostname="c3ab4498e240" ipaddress="172.21.0.3" uuid="416f73c2-d33e-4cfd-a783-2ef350946b54" />
    <agent hostname="248cfcf561d6" ipaddress="172.21.0.4" uuid="822c3766-b306-42c6-bb0d-a6b8fb7f3ef7" />
  </agents>
```
