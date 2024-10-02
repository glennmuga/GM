## Jnekins
Jenkins® is an open source automation server. With Jenkins, organizations can accelerate the software development process by automating it.

Jenkins manages and controls software delivery processes throughout the entire lifecycle, including build, document, test, package, stage, deployment, static code analysis and much more.

## What is Jenkins Continuous Integration (CI)?
Jenkins Continuous integration means whenever new code is committed to remote repositories like GitHub, GitLab, etc.

Continuous Integration (CI) will continuously build, tested, and merged into a shared repository.

## Continuous Deployment
Continuous Deployment means automating the further stages of the pipeline automatically or manually deploying the application/code to different environments like Dev, Test, and Production. 

Automating the build is the main component of Continuous Integration and Continuous Deployment.

## Continuous Delivery
Each and every build that passed all automated tests and was able to be fully automated and delivered into production only required one click of human intervention is called Continuous Delivery.

## What Is Jenkins Freestyle Project?
Jenkins freestyle project is an configuration and options based project which will allows you to build,test, and deploy 

the application with automation by selecting the required configuration based on the requirement following are the some of the available in the freestyle project.

>> Building and testing code
>> Packaging applications
>> Deploying applications to production servers
>> Running reports

## What is Jenkins Pipeline?
DevOps professionals mostly work with pipelines because pipelines can automate the processes like building, testing, and deploying the application.

Doing manually by UI takes lots of time and effort which will affect productivity. With the help of Continuous Integration / Continuous Deployment (CI/CD) Pipeline scripts we can automate the whole process which will increase productivity and save lots of time for the organization and can deliver quality applications to the end users

## Path for jenkins ?
If you installed Jenkins manually, you might need to check the Jenkins home directory, which is often located at /var/lib/jenkins.

## What Does “Poll SCM” Mean In Jenkins?
In Jenkins, “poll SCM” means periodically checking a version control system (e.g., Git) for changes. 

You can schedule how often Jenkins checks for updates. When changes are detected, Jenkins triggers a build,a key feature for continuous integration, scheduled tasks, and automated response to code changes.

## BUILD Cycle 
0 0 * * *	Schedules a build every day at midnight (00:00).
30 * * * *	Schedules a build every hour at the 30th minute (e.g., 1:30 AM, 2:30 AM).
0 15 * * 1	Schedules a build every Monday at 3 PM.
0 8,20 * * *	Schedules a build every day at 8 AM and 8 PM.
30 22 * * 5	Schedules a build every Friday at 10:30 PM.

## What Is The Default Port Number For Jenkins?
The default port number for Jenkins is 8080. When you access the Jenkins web interface via a web browser, you typically use the URL: http://your_jenkins_server:8080/.

## types of build triggers in Jenkins include:

SCM Polling Trigger: Monitors source code repositories for changes and triggers builds.

Scheduled Build Trigger: Runs jobs on a predefined schedule using cron-like syntax.

Webhook Trigger: Listens for external events or notifications to start builds.

Upstream/Downstream Trigger: Triggers downstream jobs based on the success of upstream jobs, creating build pipelines.

Manual Build Trigger: Requires manual user intervention to start a job.

Dependency Build Trigger: Triggers jobs when another job is completed, regardless of success or failure.

Parameterized Trigger: Passes parameters from one job to another during triggering.

Pipeline Trigger: Allows custom triggering logic within Jenkins Pipelines.

Using the right trigger type is crucial for automating and managing your CI/CD pipelines effectively.

##  What Is A Jenkins Agent?
A Jenkins agent, also called a Jenkins slave or node, is a separate machine or resource that collaborates with a Jenkins master to execute jobs and build tasks.

Agents enable parallel and distributed builds, scaling Jenkins’ capacity.

They register with the master, get assigned jobs, execute them on their own hardware or VMs, and report back results. 

Agents can run on various platforms, making it possible to test and build in different environments.

##5. Explain about Master-Slave Configuration in Jenkins.

![image](https://github.com/user-attachments/assets/05e1e68b-616c-451a-8c2a-76a46f0952c5)

A Master-Slave configuration in Jenkins, also known as a Jenkins Master-Agent configuration, is a setup that allows Jenkins to distribute and manage its workload across multiple machines or nodes.

In this configuration, there is a central Jenkins Master server, and multiple Jenkins Agent nodes (slaves) that are responsible for executing build jobs.

This architecture offers several advantages, including scalability, parallelism, and the ability to run jobs in diverse environments.

Here’s an explanation of the key components and benefits of a Master-Slave configuration in Jenkins:

Components:

Jenkins Master:

The Jenkins Master is the central server responsible for managing and coordinating the entire Jenkins environment.

It hosts the Jenkins web interface and handles the scheduling of build jobs, job configuration, and the storage of build logs and job history.

The Master communicates with Jenkins Agents to delegate job execution and collects the results.

Jenkins Agent (Slave)

Jenkins Agents, often referred to as Jenkins Slaves or nodes, are remote machines or virtual instances that perform the actual build and testing tasks.

Agents can run on various operating systems and environments, enabling the execution of jobs in different configurations.

Agents are registered with the Jenkins Master and are available to accept job assignments.

##  Benefits:
Scalability: Easily handle more build jobs by adding Agents.

Parallelism: Run multiple jobs simultaneously for faster results.

Resource isolation: Isolate jobs on different machines or environments.

Load distribution: Distribute jobs for optimal resource use.

Flexibility: Configure Agents for specific requirements.

Resilience: Reassign jobs if an Agent becomes unavailable.

Security and isolation: Control Agent access and resources.

Support for diverse environments: Test on various platforms and setups.

##  Explain about the multibranch pipeline in Jenkins.
A Multibranch Pipeline in Jenkins is a feature for managing CI/CD pipelines for multiple branches in a version control repository. 

It automatically creates pipelines for each branch or pull request, uses Jenkinsfiles to define pipeline configurations, supports parallel builds, and cleans up unused jobs.

It simplifies managing and automating pipelines across vario
us code branches and pull requests, streamlining the CI/CD process.

## What is a Multi-Configuration project in Jenkins?

A Multi-Configuration project in Jenkins, also known as a Matrix Project, is designed for testing or building a software project across multiple configurations simultaneously.

It allows you to define axes representing different variations (e.g., operating systems, JDK versions) and Jenkins automatically tests or builds the project for all possible combinations of these configurations.

It’s useful for cross-platform testing, version compatibility, browser testing, localization checks, and more, ensuring software works in diverse environments.

## What is the global tool configuration in Jenkins?
Global Tool Configuration in Jenkins refers to the centralized configuration of software tools and installations that can be used by all Jenkins jobs and pipelines across the Jenkins master server.

It allows Jenkins administrators to set up and manage tool installations such as JDKs, build tools (e.g., Maven, Gradle), version control systems (e.g., Git, Subversion), and other utilities in a consistent and organized manner. 

This configuration is accessible from the Jenkins web interface and provides a convenient way to ensure that all Jenkins projects have access to the required tools.

##  What is Jenkins Shared Library?
A Jenkins Shared Library is a powerful feature in Jenkins that allows organizations to centralize and reuse code, scripts, and custom functions across multiple Jenkins pipelines and jobs.

It enables the creation of a shared and maintainable codebase that can be leveraged by various projects and teams, promoting consistency, efficiency, and code reuse in your Jenkins CI/CD workflows.

## How do you implement a Blue-Green deployment strategy in Jenkins, and what are the key benefits of using this approach in a CI/CD pipeline?
 Implementing a Blue-Green deployment in Jenkins involves:

Setting up two identical environments: blue and green.

Deploying the new version to the green environment.

Testing in the green environment.

Switching traffic to green if testing succeeds.

Monitoring and potential rollback if issues arise.

Key benefits include zero downtime, quick rollback, reduced risk, safe testing, continuous delivery, scalability, enhanced monitoring, and improved confidence in deploying changes. 

This approach ensures a reliable and agile CI/CD pipeline.

##  TCP/IP allows communication between a number of computers (called hosts) connected on a network.Each network can be connected to another network to communicate with hosts on that network.

