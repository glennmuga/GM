## Docker 

Docker is an open-source platform designed to automate the deployment, scaling, and management of applications in lightweight containers.

Docker is a leading containerization platform that has revolutionized the way applications are developed, shipped, and deployed.

## What is Docker ?
Docker is a containerization platform that allows to package an application with all its dependencies into one single entity as single container which can be easily deployed and run on any machine that supports docker.

This makes it easier to devlop , test , deploy applications in different environments.

It uses container technology to isolate processes and provide a lightweight, portable solution for application deployment'

## What are the Pros and Cons of Docker?
Pros of Docker

Portability: It enables consistent deployment across various environments.

Resource Efficiency: Optimizing of resource usage with a shared kernel will be done effectively.

Isolation: It provides security through isolation of process and file system.

Automation: it supports automated builds and streamlining development workflow

Cons of Docker

Learning Curve: Initial learning of the containerization concepts will bit new to understand.

Additional Resources: Containers use some more resources compared to running applications directly on host.

Security Concerns: Misconfigurations may lead to the security risks if not properly managed.

Container Orchestration Complexity: Management of orchestration tools will be complex for larger-scale deployments.

## Name and Explain the Components of Docker.

Docker consists of the following as a docker components :


Docker Engine: Docker engine is the runtime that executes containers.

Docker Images: Docker images are lightweight, readable templates containing executable packages that include the application with its dependencies.

Docker Containers: Docker containers are standardized , encapsulated environments that run applications/instances of Docker images.

Docker Compose: Docker compose is a tool for defining and running multi-containered Docker applications.

## Name and Explain the State of a Docker Container.
A state of a docker container directly influences its runtime characteristics and how it interacts with the underlying Operating system. A Docker container will be in one of these three states:

A docker container will be in running state it is when actively executing.

A container in paused state means that container is temporarily halted.

The container will be in stopped state when it is inactive.

## Can You tell What is the Functionality of a Hypervisor?
A hypervisor is a virtualization software that helps in running multiple operating systems (Guest OS) 

on a single physical host system by providing an isolation between the virtual machines (VMs) and manages their resources.

## Can You tell What is the Functionality of a Hypervisor?
A hypervisor is a virtualization software that helps in running multiple operating systems (Guest OS) on a single physical host system by providing an isolation between the 

virtual machines (VMs) and manages their resources.

![image](https://github.com/user-attachments/assets/767c8ac4-8c2e-44a1-a5c1-0532a1ab8468)


## What is Docker Hub?
Docker Hub is container registry that serves as a centralized repository for Docker images. It built for developers and open source contributors to find , use , share and download container images.

Docker Hub can be used either host public repos that can be used for free, or docker private repos for teams and enterprises.

## Name the Essential Docker Commands and What They Do.
The essential Docker Commands are listed here:

docker run: Docker run command is used to run the docker image as a docker container.

docker ps: Docker os command will list all the running container in the docker.

docker exec: It helps in execute the commands in a running container.

docker stop: It will stops a container which is running in the docker.

## Can a Container Restart By Itself?
Yes, a container itself can restart automatically by setting up the –restart option during the creation period of time. For example using `docker run –restart` always. 

This will ensure that the container restarts irrespective of its exit status.

## Can You Tell the Differences Between a Docker Image and Layer?
A Docker Image can be considered as a snapshot of a file system and application dependencies. It is composed of multiple layers, where each layer will represent a set of filesystem changes. 

These Layers facilitate in efficient image creation and sharing common components among the images.

## Where are Docker Volumes Stored in Docker?
Docker volumes will be stored on the host machine in the directory /var/lib/docker/volumes . 

This ensures persistance of the data storage even if the container is removed.

## What Does the Docker Info Command Do?
docker info provides detailed information regarding the Docker system. It includes information such as the number of containers, images, storage driver that are used and much more. 

It’s a valuable command for gaining details on overview of the Docker environment.

##  Can You Tell the Difference Between CMD and ENTRYPOINT?
CMD vs ENTRYPOINT
CMD is used for setting default commands and arguments that will be executed at the start of runtime of the containers. 

It is oftenly overridden by providing command-line arguments during container startup.

ENTRYPOINT configures a container to run as an executable, defining the command that has to be executed when the container starts. 

It is more strict than CMD and is oftenly used when the container should have to behave like an executable.

## How to Start, Stop, and Kill a Container?
In Docker to start , stop and kill a container we using start , stop and kill options on association with the docker command , the usage is given below.

To start the docker container use this command:

docker start < container_name >
To stop the docker container use this command:

docker stop < container_name >
To kill the docker container use this command:

docker kill < container_name >

## How Do You get the Number Of Containers Running, Paused, and Stopped?
For obtaining the number of running, paused, and stopped containers in Docker you can use the command such as `docker ps -q` for knowing the list of running containers

and `docker ps -q -f “status=paused”` for paused ones. Stopped containers can be counted using `docker ps -aq -f “status=exited”`. 

These commands will the provide the list of container IDs , and you have to can further process the output to get the counts programmatically like `docker ps -q | wc -l`.

## Why is Docker System Prune Used? What Does It Do?
`docker system prune` is used for removal of unused data on inclusion of stopped containers, docker networks, and dangling images.

It helps in freeing up the disk space on cleaning unnecessary resources.

## What is Docker Swarm?
Docker Swarm is an inherented native clustering that comes up with a orchestration solution for the Docker software. 

It helps in simplifying the management of a swarm of Docker nodes on allowing the seamless scaling of the applications across various multiple nodes within the network.

## Can You Implement Continuous Development (CD) and Continuous Integration (CI) in Docker?
Yes, Docker is an integral part to the CI/CD pipelines.

Developers can use Docker images for the consistent environments, and CI tools can perform the automate testing and deployment using Docker containers for ensure reproducibility.

## 
