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

#### There are two types of registries in the Docker
1. **Public Registry**:  Refers to a publicly accessible repository where Docker images are stored and can be shared with others. Docker Hub is one of the most popular public registries.
2. **Private Registry**: It is used to share images within the enterprise.

<br><br>

---

## Docker Container
A container is a lightweight, portable, and self-sufficient software unit that encapsulates an application, 
its dependencies, and runtime environment. Containers provide isolation from the host system while sharing 
the host OS kernel, allowing for efficient resource utilization and rapid deployment.

### Why Containers?           
- **Portability:**  Applications run consistently on different platforms.  
- **Isolation:** Improved security by isolating from the host system.  
- **Resource Efficiency:** Containers share the host OS kernel, which reduces resource overhead compared to virtual machines. This efficiency allows for better utilization of system resources and enables running multiple containers on a single host without the need for full OS virtualization.  
- **Rapid Deployment:** Containers enable rapid and consistent application deployment. They can be easily created, started, stopped, and scaled as needed.
- **Scalability:** Due to their lightweight nature, containers can be quickly scaled up or down to meet changing demand. This horizontal scalability facilitates efficient load balancing and resource allocation in distributed systems.  
- **Version Control and Rollback:**  Immutable, simplifying version management.  
- **DevOps and CI/CD:** Containers play a significant role in modern DevOps practices and Continuous Integration/Continuous Deployment (CI/CD) pipelines. Their consistency and ease of deployment streamline development, testing, and production workflows.  
- **Ecosystem and Tooling:**  A Containers have a rich ecosystem with a wide array of supporting tools and platforms, such as Docker and Kubernetes. This ecosystem makes it easier for developers and operations teams to manage, orchestrate, and monitor containerized applications effectively.
- **Microservices Architecture:**  Containers are well-suited for implementing microservices architecture, where applications are broken down into smaller, loosely coupled services. This enables better agility, scalability, and maintainability in complex systems.


### Container vs Virtual Machine


<div align="center">

  ![Container VS Virtual Machines](https://github.com/MohamedHashish42/TestRepo/assets/81900786/cd6b7412-a624-47db-9287-f7e1d0bd2d50)

</div>

<table class="table table-bordered table-hover">
            <thead class="thead-dark">
                <tr>
                    <th>Aspect</th>
                    <th>Containers</th>
                    <th>Virtual Machines</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Definition</td>
                    <td>A container is a lightweight, portable, and self-sufficient software unit that encapsulates an application, its dependencies, and runtime environment. 
                    Containers provide isolation from the host system while sharing the host OS kernel, allowing for efficient resource utilization and rapid deployment</td>
                    <td>A virtual machine (VM) is a software emulation of a computer system that operates as an independent and isolated entity. It includes a complete operating system 
                    and runs on top of a physical server. VMs enable the execution of multiple instances of different operating systems on a single physical machine, each with its own 
                    dedicated resources and isolated environment</td>
                </tr>
                <tr>
                    <td>Technology</td>
                    <td>Containerization technology (e.g., Docker)</td>
                    <td>Hypervisor-based virtualization (e.g., VMware, VirtualBox)</td>
                </tr>
                <tr>
                    <td>Isolation</td>
                    <td>Lightweight, share host OS kernel</td>
                    <td>Emulate full OS stack</td>
                </tr>
                <tr>
                    <td>Overhead</td>
                    <td>Lower overhead</td>
                    <td>Higher overhead</td>
                </tr>
                <tr>
                    <td>Performance</td>
                    <td>Faster startup and execution</td>
                    <td>Slower startup and execution</td>
                </tr>
                <tr>
                    <td>Resource Utilization</td>
                    <td>More efficient (share host OS resources)</td>
                    <td>Less efficient (dedicated resources)</td>
                </tr>
                <tr>
                    <td>Portability</td>
                    <td>Highly portable across environments</td>
                    <td>Less portable (may require conversion or configuration)</td>
                </tr>
                <tr>
                    <td>Deployment Speed</td>
                    <td>Rapid deployment</td>
                    <td>Slower deployment</td>
                </tr>
                <tr>
                    <td>Scalability</td>
                    <td>Easily scalable</td>
                    <td>Scalable but with more resource consumption</td>
                </tr>
                <tr>
                    <td>Use Cases</td>
                    <td>Microservices, DevOps, CI/CD</td>
                    <td>Legacy applications, OS isolation</td>
                </tr>
                <tr>
                    <td>Isolation Level</td>
                    <td>Process-level isolation</td>
                    <td>Full OS-level isolation</td>
                </tr>
                <tr>
                    <td>Security</td>
                    <td>Slightly lower security (shared kernel)</td>
                    <td>Stronger isolation (isolated OS stack)</td>
                </tr>
                <tr>
                    <td>Updates and Patches</td>
                    <td>Faster updates for container images</td>
                    <td>OS-level updates for VMs</td>
                </tr>
                <tr>
                    <td>Example</td>
                    <td>Docker, Kubernetes, Podman</td>
                    <td>VMware, VirtualBox, Hyper-V</td>
                </tr>
            </tbody>
        </table>

### Some Files and Directories Navigation commands using Bash 
| Command | Description |
| - | - |
| `ls`                                |List all files in specific directories |
| `cd  [directory_name]`              |Navigate to specific folder|
| `cd .. `                            |Back on step|
| `cd / `                             |Navigate to root|
| `mkdir [directory_name]`            |Create new directory |
| `touch [file]`                      |Create file |
| `cat [file]`                        |Open file|
| `cp [file] [directory]`             |Copy file to specific directory |
| `rm [file_or_directory]`            |Remove file or directory |
| `pwd`                               |Display the full path of the directory you are currently located in |

### Some docker container commands


| Command | Description |
| - | - |
| `docker container ls `                                            |List running containers|
| `docker container ls -a  or docker container ls --all`            |List all containers|
| `docker container create --name [set_container_name] [image_name]`|Create container|
| `docker container start [container_name_or_id]`                   |Start one or more stopped containers| 
| `docker container stop  [container_name_or_id]`                   |Stop one or more opened containers |
| `docker container run [image_name] `                              |Pull the image if not exist, create and and start a container from an image.|
| `docker container run -d [image_name] `                           |[--detach or -d] To allow container to run on background|
| `docker run -it [container_name_or_Id] [command] `                |-it ( Interactive Terminal): take two params (container and command) To execute a specific command on the specific container, for example, opening bash in a specific container|
| `docker exec -it [container_name_or_id] [command] `               |To enter the container terminal if it is already running|
| `exit or (ctrl + p )`                                             |To exit from  container terminal|
| `docker container rm [container_name_or_Id]  `                    |Remove Container|
| `docker stats [container_name_or_id] `                            |Display a live stream of container(s) resource usage statistics|
| `docker container inspect [container_name_or_id]`                 |Display detailed information on the container|
| `docker container inspect --format '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' [container_name_or_id]`                                                                   |Get container ip address|
|`docker container logs [container_name_or_id]`	                    |Fetch the logs of a container|

#### Notes
Run command do the following 
1. Pull the image if not exist 
2. Create a container from it
3. Start the container

This means the run command equals the following 3 commands
1. docker image pull [image_name]  
2. docker container create  [image_name] 
3. docker container start  [container_name_or_id]

<br><br>

---

## Docker Image

A Docker image is a snapshot of a file system with necessary application code, libraries, and dependencies, along with metadata 
that defines how to run the software within a container.

### Key characteristics:

#### 1- Layered File System
Docker images are built using a layered file system. Each image is composed of multiple read-only layers stacked on top of each 
other, forming a single coherent view. This layered approach provides efficiency, reusability, and versioning capabilities. Docker uses a union file system to combine these layers.

#### 2- Immutable 
This means that none of its components can be altered after it's built. For instance, you cannot update the code, change the configuration, or modify any of the libraries or dependencies within the image directly. Instead, if you need to make changes to the application, you would typically create a new Docker image with those changes incorporated.

#### 3- Public and Private Repositories
Docker images can be stored in public or private container registries. Docker Hub is a popular public registry where users can find and share images. Private registries allow organizations to manage and distribute their images securely.

#### 4- Versioning
Docker images can have multiple versions, allowing developers to control and track changes to the software. Versioning also facilitates rollback to a previous state in case of issues.

#### 5- Efficient Image Distribution
Docker images are designed for efficient distribution. When pulling or pushing images, Docker only transfers the necessary layers, reducing network bandwidth and speeding up image distribution.

#### 6- Reusability
Docker images can be reused across different environments and projects, saving time and resources. Cached layers are leveraged when building new images, making subsequent image builds faster.

#### Conclusion
Docker images play a vital role in the containerization ecosystem, enabling developers to package, distribute, and run applications in isolated environments. They provide a powerful means of encapsulating software and its dependencies, making it easier to manage complex applications and ensuring consistency across development, testing, and production environments.

### Some docker image commands
| Command | Description |
| - | - |
| `docker image inspect  [image_name]`                    |Display detailed information on the image|
| `docker history [image_name]`                           |Show the history of an image|
| `docker image rm [image_name]    `                      |Remove image|
| `docker images ls -q`                                   |List images ids|
| `docker images rm  $(docker images ls -q)`              |Remove all images|


<br><br>

---


## Dockerfile

A Dockerfile is a text file that contains a set of instructions used to build a Docker image,
It defines the environment and configuration required for a containerized application.

### Dockerfile Instructions:
        
#### 1- Base Image:
The Dockerfile starts with specifying a base image using the __FROM__ instruction. The base image serves as the 
starting point for building the new image, it is a minimal image that includes only the necessary components for the application,
The new image inherits the file system and configuration of the base image. 

   
#### 2- Working Directory:
The __WORKDIR__ instruction sets the working directory inside the container. It defines the location where subsequent 
commands will be executed. Note that if the specified directory doesn't exist, Docker will create it. Note this instruction can be used multiple times within a Dockerfile to change the working directory for different commands.
   
#### 3- Copying Files: 
The __COPY__ or __ADD__ instructions are often used to copy files from the host machine to the container. This is helpful for 
including application code, configurations, and other necessary files.
       
#### 4- Environment Setup: 
The Dockerfile can include various instructions to set up the environment, such as installing dependencies and setting 
environment variables.

#### 5- Exposing Ports:
The __EXPOSE__ instruction informs Docker about the ports the container will listen on at runtime. Note that while the __EXPOSE__ instruction informs Docker about the ports the container will potentially use, it doesn't automatically publish these ports to the host. Ports must be explicitly mapped when running a container using the -p or --publish option to make them accessible externally. 

#### 6- Container Execution: 

The __CMD__ or __ENTRYPOINT__ instruction specifies the command that runs when the container starts.  
__CMD__, on the other hand, is used to specify the default command and arguments that should be executed when a container is started.  

On the other hand __ENTRYPOINT__ is used to specify the main command that should be executed when a container is started using the image. The default __ENTRYPOINT__ command is /bin/sh -c.

If both __ENTRYPOINT__ and __CMD__ are specified in a Dockerfile, the command specified in __CMD__ will be appended to the ENTRYPOINT command. It acts as an argument for __ENTRYPOINT__. The resulting command will be executed when the container is started.

Look at the following three examples

<table border="1">
  <tr>
    <th>Example Description</th>
    <th>Dockerfile Instruction</th>
    <th>Docker Run Command</th>
    <th>Result</th>
  </tr>
   <tr>
    <td>EX 1: Overriding CMD</td>
    <td><code>CMD ["echo", "Hello, World!"]</code></td>
    <td><code>docker run my-image echo "Custom Greeting"</code></td>
    <td>Custom Greeting</td>
  </tr>
   <tr>
    <td>EX 2: Overriding ENTRYPOINT</td>
    <td><code>ENTRYPOINT ["echo", "Hello, World!"]</code></td>
    <td><code>docker run  --entrypoint "echo" hello-world-ent  "Custom Greeting"</code></td>
    <td>Custom Greeting</td>
  </tr>
   <tr>
    <td>EX 3: Passing new argument to ENTRYPOINT</td>
    <td><code>ENTRYPOINT ["echo", "Hello, World!"]</code></td>
    <td><code>docker run my-image "Custom Greeting"</code></td>
    <td>Hello, World! Custom Greeting</td>
  </tr>
   
</table>

For more information  [Entrypoint vs CMD](https://devopscube.com/entrypoint-vs-cmd-explained/)


#### 7- Additional Instructions:  
There are other instructions like __ENV__ (setting environment variables), __VOLUME__ (defining volumes), __RUN__ (executing commands during the image build process), and __LABEL__ (adding metadata to the image) that further customize the container image.

<br><br>

---

## Docker Volume

Docker volume is a feature in Docker that allows you to manage and persist data outside the container's lifecycle. it provides a way to share and store data between containers and ensure that the data remains available even if the container is stopped, removed, or replaced. Docker volumes are particularly useful for managing persistent data in containerized applications.

### Volume Types:
#### 1- Named Volumes
Named volumes are created using a specified name and managed by Docker. They have identifiable names and are easy to manage and share between containers.  
```bash
# Example
docker run -d --name [container_name]  -v [volume_name]:[/path/in/container] [image_name]
```

#### 2- Anonymous volumes 
Anonymous volumes are created without specifying a name, and Docker assigns a random name to them. They are generally used for temporary data.    
```bash
# Example
docker  run -d --name [container_name] -v [/path/in/container] [image_name]
```

#### 3- Host-Mounted Volumes (Bind Mounts)
Bind mounts allow you to mount a directory or file from the host machine into the container. This enables sharing data between the host and container, and changes in the mounted directory are immediately reflected in both places.   
```bash
# Example
docker run -d --name [container_name] -v [/path/in/host]:[/path/in/container] [image_name]
```

### Some docker volume commands
| Command | Description |
| - | - |
| `docker volume ls `                    |List volumes|
| `docker volume create [volume_name]`   |Create a volume|
| `docker volume inspect [volume_name]`  |Display detailed information on one or more volumes|
| `docker volume prune`                  |Remove all unused local volumes|
| `docker volume rm [volume_name]`       |Remove one or more volumes|



  
