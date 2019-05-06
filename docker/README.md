# Running Libraries Assembler via Docker-Compose file

## Dockerfile
 Dockefile is created on top of `ubuntu16.04` image.
 
## Requirements
 - The project should be cloned from https://github.com/trilogy-group/slisys-templatebuilder-libraries-assembler
 - Docker version 18.09.0-ce
 - Docker compose version 1.23.1
  
## Quick Start
- Clone the repository
- Open a terminal session to that folder
- Run `./docker-cli.sh start`
- Run `./docker-cli.sh exec`
- At this point you must be inside the docker container, in the root folder of the project. From there, you can run the commands as usual:	
	- `npm install -g npm`
    - `npm install -g jspm`
    - `npm install -g gulp`
    - `npm install`  install dependencies
    - `jspm install` install jspm dependencies
    - `gulp test`  run unit tests
    - `gulp cover` run code coverage
    - `gulp e2e`  run e2e tests
    - `gulp watch` run the project
	
- When you finish working with the container, type `exit`
- Run `docker-cli stop` to stop and remove the service.
 
## Possible issues
 1. Docker-compose build might fail with the message
```Couldn't connect to Docker daemon at http+docker://localhost - is it running? If it's at a non-standard location, specify the URL with the DOCKER_HOST environment variable.Couldn't connect to Docker daemon at http+docker://localhost - is it running?...```

Add user you are working under to the sudo group or add `sudo` for docker-compose commands in `docker-cli.sh` script.
