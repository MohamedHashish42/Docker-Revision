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
| `docker volume`               |Display a list of docker volume commands|
| `docker info `                |Display system-wide information|
| `docker help `                |List the main categories of commands that Docker supports, such as management commands, container commands, image commands, etc|
| `docker help [command]`       |Help about the command, provides more general information about the command eg: `docker help run`|
| `[docker_command] --help`     |Help about the command, It is typically used when you want to learn more about a particular command and its options|
| `docker login `               |Log in to a Docker registry|
| `docker logout  `             |Log out from a Docker registry|

<br><br>

---

##  Docker Architecture
Docker follows Client-Server architecture, which includes three main components that are Docker Client, Docker Host, and Docker Registry.

<div align="center">

  ![Docker Architecture](https://github.com/MohamedHashish42/TestRepo/assets/81900786/f2c7b6b5-762b-4ecc-ad7b-3a40ab7daa16)

</div>


### 1. Docker Client 
is the primary way that many Docker users interact with Docker. When you use commands such as docker run, the client sends these commands to Docker daemon, which carries them out. The docker command uses the Docker API. The Docker client can communicate with more than one daemon.

#### Examples
- Docker CLI


### 2. Docker Host
 is a physical or virtual machine on which the Docker platform is installed and where Docker containers are created, managed, and run. It's the environment where Docker engine, the core component of Docker, operates. A Docker host can run multiple Docker containers concurrently, each isolated from the others

#### Examples
- Linux
- Windows


### 3. Docker Registry
Docker Registry manages and stores the Docker images.

#### There are two types of registries in the Docker -
- **Public Registry**:  Refers to a publicly accessible repository where Docker images are stored and can be shared with others. Docker Hub is one of the most popular public registries.
- **Private Registry**: It is used to share images within the enterprise.

  
