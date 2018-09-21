# Dockerfile

No dockerfile provided as image is based on official `microsoft/dotnet:2.1.300-sdk`

# Requirements 
	
 - The project should be cloned from https://github.com/dotnet/cli
 - Docker version 18.06.1-ce
 - Docker compose version 1.22.0

# Quick Start

- Unzip `cli.zip` in `{project-root-folder}`
- Open a terminal session to that folder
- If you want to run a windows container, uncomment `# image: "microsoft/windowsservercore:1709"` from docker-compose.yml 
and switch docker to windows containers before proceeding. 
(Note: this feature may not be available, depending on your docker and os version)
- Run `docker-compose up -d`
Parameter `-d` makes the container run in detached mode.
This command will create a running container in detached mode called `cli_dev_1`.
You can check the containers running with `docker ps`
- Run `docker exec -it cli_dev_1 bash -c "cd /app && bash"`
- At this point you are inside the container, and the /app dir contains the repo source code.
- Run `./build.sh` or './build.cmd' (if using windows containers) to build the solution. Add `/t:Compile` option to skip unit tests.


