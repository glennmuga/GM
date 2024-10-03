
Common Questions for MCI
Tell me about yourself 
## What is the difference between merge and rebase 
![image](https://github.com/user-attachments/assets/4bb4c06a-3ae2-4596-8eb2-809ceccda851)

## What are the branching methods

## Explain project


## What is CI
Continuous integration is a DevOps software development practice where developers regularly merge their code changes into a central repository, after which automated builds and tests are run. 

Continuous integration most often refers to the build or integration stage of the software release process and entails both an automation component (e.g. a CI or build service) and a cultural component (e.g. learning to integrate frequently). 

## What is the difference between CI and CD , deployment and delivery  

ontinuous Integration (CI)
Definition: CI is a development practice where developers frequently merge their code changes into a central repository. Each merge triggers an automated build and test process.

Purpose: The main goal is to detect and address integration issues early, ensuring that the codebase remains in a deployable state.

Key Benefit: It reduces the time and effort required to integrate changes, making it easier to identify and fix bugs early in the development cycle1.

Continuous Delivery (CD)
Definition: Continuous Delivery is an extension of CI. It ensures that code changes are automatically prepared for a release to production. However, the actual deployment to production requires manual approval.

Purpose: The aim is to make sure that the software can be reliably released at any time.

Key Benefit: It allows for frequent and reliable releases, reducing the risk and effort associated with deploying new features12.

Continuous Deployment (CD)
Definition: Continuous Deployment takes Continuous Delivery a step further by automatically deploying every change that passes all stages of the production pipeline to the end users, without manual intervention.

Purpose: The goal is to accelerate the feedback loop with customers and reduce the time from code commit to production.

Key Benefit: It eliminates the need for a scheduled release day, allowing for faster and more frequent updates12.

Deployment vs. Delivery
Continuous Delivery: Involves automatically preparing code changes for release but requires manual approval to deploy to production.

Continuous Deployment: Involves automatically deploying code changes to production without manual intervention3.

In summary, while CI focuses on integrating code changes and running tests, CD (whether delivery or deployment) focuses on automating the release process to ensure that software can be deployed quickly and reliably.


## Explain ec2 instance and other services in AWS
Amazon Elastic Compute Cloud (Amazon EC2) provides on-demand, scalable computing capacity in the Amazon Web Services (AWS) Cloud. 

Using Amazon EC2 reduces hardware costs so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking,

and manage storage. You can add capacity (scale up) to handle compute-heavy tasks, such as monthly or yearly processes, or spikes in website traffic. When usage decreases,

you can reduce capacity (scale down) again.

An EC2 instance is a virtual server in the AWS Cloud. When you launch an EC2 instance, the instance type that you specify determines the hardware available to your instance. 

AMI 

VOLUMES 

EFS 

S3 BUCKET 

CLOUD FORMATION 

SNAPSHOT 

## What is the difference between s3 and other storage services
Amazon S3
Type: Object Storage
Use Cases: Ideal for storing large amounts of unstructured data like images, videos, backups, and big data analytics.
Accessibility: Data is accessed via HTTP/HTTPS using REST APIs.
Scalability: Highly scalable, with virtually unlimited storage capacity.
Durability and Availability: Designed for 99.999999999% (11 9’s) durability and 99.99% availability1.
Cost: Pay-as-you-go pricing model, with different storage classes for cost optimization based on access frequency.

Amazon EBS (Elastic Block Store)
Type: Block Storage
Use Cases: Suitable for use as primary storage for databases, file systems, and applications requiring high performance.
Accessibility: Attached to a single EC2 instance, similar to a traditional hard drive.
Scalability: Limited to the size of the attached volume, but multiple volumes can be used.
Durability and Availability: Data is replicated within a single Availability Zone for durability2.
Cost: Charged based on the provisioned storage size and performance level.

Amazon EFS (Elastic File System)
Type: File Storage
Use Cases: Best for shared file storage across multiple EC2 instances, such as content management systems and home directories.
Accessibility: Can be mounted by multiple EC2 instances simultaneously.
Scalability: Automatically scales up and down as files are added or removed.
Durability and Availability: Data is stored redundantly across multiple Availability Zones2.
Cost: Pay-as-you-go pricing based on the amount of data stored and throughput used.

Comparison with Other Cloud Storage Services
Google Cloud Storage: Similar to S3, it offers object storage with high durability and availability. It also provides different storage classes for cost optimization.
Azure Blob Storage: Microsoft’s equivalent to S3, offering scalable object storage with various access tiers to manage costs.
IBM Cloud Object Storage: Another object storage service with a focus on scalability, security, and cost efficiency.

Key Differences
Storage Type: S3 is object storage, while EBS is block storage and EFS is file storage.
Accessibility: S3 data is accessible over the internet, EBS is tied to a single EC2 instance, and EFS can be accessed by multiple instances.
Scalability: S3 and EFS offer automatic scalability, while EBS requires manual resizing.
Use Cases: S3 is best for unstructured data, EBS for high-performance applications, and EFS for shared file storage.
Each service has its strengths and is suited to different use cases. Choosing the right one depends on your specific needs and workload requirements.


## What are the commands available in docker 

Docker provides a wide range of commands to manage containers, images, networks, and more. Here are some of the most commonly used Docker commands:

Basic Commands
docker run: Create and start a new container.
docker start: Start one or more stopped containers.
docker stop: Stop one or more running containers.
docker restart: Restart one or more containers.
docker rm: Remove one or more containers.
docker rmi: Remove one or more images.
docker ps: List running containers.
docker images: List images.
docker pull: Download an image from a registry.
docker push: Upload an image to a registry.
Container Management
docker exec: Run a command in a running container.
docker logs: Fetch the logs of a container.
docker inspect: Return low-level information on Docker objects.
docker top: Display the running processes of a container.
docker stats: Display a live stream of container(s) resource usage statistics.

Image Management
docker build: Build an image from a Dockerfile.
docker tag: Create a tag for an image.
docker history: Show the history of an image.
docker commit: Create a new image from a container’s changes.

Network Management
docker network ls: List all networks.
docker network create: Create a new network.
docker network rm: Remove one or more networks.
docker network inspect: Display detailed information on one or more networks.

Volume Management
docker volume ls: List all volumes.
docker volume create: Create a new volume.
docker volume rm: Remove one or more volumes.
docker volume inspect: Display detailed information on one or more volumes.

System Management
docker system df: Show Docker disk usage.
docker system prune: Remove unused data.
docker info: Display system-wide information


Example Commands
Build an image:
docker build -t my-image-name .

List images:
docker images

Run a container from the image:
docker run -d -p 80:80 my-image-name
-d (detached mode): This option runs the container in the background and prints the container ID. It allows you to continue using the terminal for other commands while the container runs in the background.
-p (publish): This option maps a port on your local machine to a port inside the container. In this case, -p 80:80 maps port 80 on your local machine to port 80 in the container.
This is useful for accessing web applications running inside the container from your local machine
These steps should help you build and manage your Docker images effectively. 

## What is Dev-ops 

DevOps is a set of practices, tools, and a cultural philosophy that aims to automate and integrate the processes between software development (Dev) and IT operations (Ops) teams.
Here’s a breakdown of what DevOps entails:

Key Concepts of DevOps

Collaboration and Communication:
DevOps emphasizes breaking down silos between development and operations teams, fostering a culture of collaboration and shared responsibility1.

Automation:
Automation is a core principle of DevOps. It involves automating repetitive tasks such as code integration, testing, deployment, and infrastructure management to increase efficiency and reduce errors2.

Continuous Integration and Continuous Delivery (CI/CD):
CI/CD practices are central to DevOps. Continuous Integration involves frequently merging code changes into a central repository, followed by automated testing. Continuous Delivery ensures that code changes are automatically prepared for a release to production3.

Monitoring and Logging:
DevOps practices include continuous monitoring and logging to detect issues early and ensure system reliability and performance2.

Infrastructure as Code (IaC):
IaC involves managing and provisioning computing infrastructure through machine-readable configuration files, rather than physical hardware configuration or interactive configuration tools3.

Benefits of DevOps
Faster Time to Market: By automating and streamlining processes, DevOps enables faster delivery of new features and updates1.
Improved Collaboration: Enhanced communication and collaboration between teams lead to more efficient workflows and better problem-solving2.
Higher Quality and Reliability: Automated testing and continuous monitoring help in identifying and fixing issues early, leading to more reliable software3.
Scalability and Flexibility: DevOps practices allow for scalable and flexible infrastructure management, making it easier to adapt to changing business needs2.

DevOps Tools
Some popular DevOps tools include:

Version Control: Git, GitHub, GitLab
CI/CD: Jenkins, CircleCI, Travis CI
Configuration Management: Ansible, Puppet, Chef
Containerization: Docker, Kubernetes
Monitoring: Prometheus, Grafana, ELK Stack

Explain Ansible playbook code


what is the difference between maven install and maven deploy 


What are the different types of triggers

what is ansible

Explain about the kubernetes architecture 
 
can you use the scripting in the Jenkins directly 

why did you use poll scm

what are all the permissions given in IAM role

deployment services in yaml file

code in the playbook

why did you use maven

how did you do ssh authentication 

location of ssh key

code explanation in the yaml files 
 
 
