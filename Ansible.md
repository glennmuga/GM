## Ansible 

Ansible is a configuration management tool and an open-source product from Redhat company.

Before moving into the details of Ansible, let’s explore the evolution of the Software Development Life Cycle (SDLC).

## Ansible Arch:

![image](https://github.com/user-attachments/assets/46da622a-e7a6-4e73-a2ae-7a0fc647b2bf)

nitially, automation was done through scripting to replace the manual mode of workflow.

However, scripting brought out challenges such as the requirement of writing different scripts on various platforms.

For example, a script written for Linux wouldn’t support Windows, and separate scripts had to be provided for different Linux distributions like Red Hat, Ubuntu, Fedora, etc. The imperative nature of scripting involved specifying detailed guidelines for performing the actions making it cumbersome.

To address these challenges, configuration management tools like Ansible, Puppet and Chef have emerged.

Among these such as Ansible vs Puppet, and Ansible vs Chef, Ansible gained wide popularity due to its declarative nature and its use of a push mechanism with an agentless approach.

Because of the declarative nature of Ansible, Users only need to specify where to act and what action to perform through its intelligence ansible determines how to execute the action using its inbuilt callback plugins for fetching information.

## 1. What Is Ansible ?
Ansible is an open-source automation tool developed by Redhat that is meant for simplifying the configuration management, application deployment, and automation of tasks.

It allows us in automating repetitive tasks, ensuring consistency and efficiency in managing servers and networks using SSH protocol for make communication with the network Agentlessly.

## . What Is Inventory ?
In Ansible, an inventory is a file with specifying the information of hosts that going to be managed. It contains information such as hostnames, IP addresses, and groups of organization. The inventory can be either static or dynamic, and it may be with inclusion of variables by specific host details.

It’s a key component for targeting and managing nodes infrastructure in Ansible. A sample inventory file is given below.

## What Are The Features Of Ansible ?
Ansible comes with several features that make it powerful and popular automation tool. A few of the key features are listed here:

Agentless: Ansible does not require any agent installation on the managed nodes. It communicates with the nodes in the network using SSH simplifying deployment and reduces complexity.

Declarative Language: Ansible uses a simple human-readable YAML syntax to specify the desired state of the system making it easy to write and understand automation scripts.

Idempotent Operations: Ansible ensures for the achievement of desired state i.e., running a playbook multiple times has the same effect as running it once. This prevents from unintended changes ensuring consistency.

Playbooks: Automation scripts in Ansible are known as playbooks. Playbooks are written in YAML by defining a set of tasks that to be executed on remotely specifying in the hosts section.

Modules: Modules are used in ansible to perform specific tasks on managed nodes.They are 2 types of modules as built-in modules ( that are already created and comes with ansible ) and custom modules that are created by users.

Inventory Management: Ansible uses an inventory file to specify the hosts information such as IP address or domainname, user details etc.. on which the automation tasks have to be executed. The inventory file can be either static or dynamic include host groups.

## What Are Ansible Tasks, And How Do They Contribute To The Automation Process?
Ansible tasks are individual work units within a playbook coming with defined actions that to be performed on remote hosts, contributing to the overall automation process.

##  What Makes Ansible Stand Out From Other Configuration Management Tools?
Ansible’s agentless architecture and its simplicity in use (YAML syntax), and ease of setup contribute to its standout features among other Configuration Management tools.

## Briefly Explain Ansible’s Architecture Through Outlining Its Different Components.
The control node communicates with managed nodes through SSH protocol executing tasks defined in playbooks.

Ansible consists of a control node, managed nodes, inventory, modules, and plugins

## What Is The Foundational Programming Language Of Ansible?

Ansible is built on top of Python, enhancing its simplicity for clear playbooks and versatility in creating robust modules. Python’s wide range of adoption provided good community support, making Ansible an effective and flexible automation tool.

## What are handlers in Ansible, and how are they used in playbooks?

Handlers in Ansible are tasks that are triggered by other tasks, usually used to respond for the changes that require start , stop , reload or restart the 

service actions. They are defined in the playbook and executed as per need.

## 
