<h2 dir="rtl" align="center">
بسم الله الرحمن الرحيم
</h2>

# Docker Revision
This revision is designed to provide a concise overview of Docker, including basic and some advanced concepts. It is intended for developers, software engineers, and anyone interested in using Docker.

<br>

---

## Introduction
Docker is an open-source platform that enables developers to automate the deployment, scaling, 
and management of applications inside lightweight, portable, and self-sufficient containers. 
It provides an efficient and consistent way to package, distribute, and run applications, 
regardless of the underlying infrastructure.

Docker uses containerization technology to encapsulate applications and their dependencies, runtime environment, libraries, and configuration files into a single unit called a "container." Containers are isolated from the host system and other containers, ensuring consistent behavior across different environments.

The core component of Docker is the Docker Engine. It acts as a client-server application that runs on the host machine and manages containers. The Docker Engine includes a server (daemon) responsible for building, running, and managing containers, along with a command-line interface (CLI) that allows users to interact with the Docker Engine.


### Some Generic docker commands
| Command | Description |
| - | - |
| `docker -v`                   |Display the Docker version information |
| `docker `                     |Display a list of docker commands|
| `docker container`            |Display a list of docker container commands|
| `docker image`                |Display a list of docker image commands|
| `docker volume`               |Display a ist of docker volume commands|
| `docker info `                |Display system-wide information|
| `docker help `                |List the main categories of commands that Docker supports, such as management commands, container commands, image commands, etc|
| `docker help [command]`       |Help about the command, provides more general information about the command eg: `docker help run`|
| `[docker_command] --help`     |Help about the command, It is typically used when you want to learn more about a particular command and its options|
| `docker login `               |Log in to a Docker registry|
| `docker logout  `             |Log out from a Docker registry|
  
