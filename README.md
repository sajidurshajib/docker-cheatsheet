# Docker cheatsheet 
`- By Sajidur Rahman `

### Prerequisite
 - Basic linux command 
 - Manage user and group
 - File permission
 - 


### Dockerfile 
 - `FROM` define base image for container.
 - `WORKDIR` specify working directory. like - `WORKDIR /app/`
 - `COPY` use for copy file from host machine.
 - `ADD` also works like `COPY`, but it provides some extra features. For example, ADD can automatically extract zip files.
 - `RUN` use for run command while build.
 - `CMD` commands are used when the image is run to specify the default command, but their result is not stored in the image.
 - `EXPOSE` Informs Docker that the container listens on the specified network port(s) at runtime.
 - `USER` set user.
 - `ENTRYPOINT` default command which shoulfd not be override. 


### Docker Image

**Build image**

Command - `docker build -t[tag] [source code location]`

Example - `docker build -t react-app .`

**Remove unused image**

`docker image prune`

**Rmeove Image**

 Command - `docker image rm [tag-name]`

 Example - `docker image rm react-app`

### Docker tagging image [ latest ]
This tag something like version.

Command - `docker build -t [repo-tag]:[tag]`

Example - `docker build -t react-app:1.0`

**Rename tag**

Command - `docker image tag [repo-tag]:[tag] [repo-tag]:[new-tag]`

Example - `docker image tag react-app:1.0 react-app:2.0`

### Docker container
**Docker run container**

Command - `docker run -it[Interactive mode] [tag name]`

Example - `docker run -it react-app`

**Run container using container id**

`docker start -i [ container id ]`

### Docker process
`dcoker ps -a` [-a for all]





