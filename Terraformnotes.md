## Q) What is Terraform ?

Terraform is an IAC tool, used primarily by DevOps teams to automate various infrastructure tasks. 

The provisioning of cloud resources, for instance, is one of the main use cases of Terraform. 

It’s a cloud-agnostic, open-source provisioning tool written in the Go language and created by HashiCorp.

Terraform allows you to describe your complete infrastructure in the form of code. Even if your servers come from different providers such as AWS or Azure, Terraform helps you build and manage these resources in parallel across providers.

## Q)How Does Terraform Work?

Terraform lets you define and manage your entire infrastructure via configuration files (.tf) and version control.

It accomplishes this by using the two main components of  Terraform architecture: Core and Providers.

## The 2 Main components of Terraform Architecture are Core and Providers :

![image](https://github.com/user-attachments/assets/e44040c1-219d-4c97-b62e-d1caabb3f835)


#### Terraform core uses two input sources:

#### 1st one is Core :

The first is the source input that the user configures into Terraform, defining what resources need to be created or provisioned. 

The second input source consists of data feeds into Terraform about what the current infrastructure setup looks like.

#### 2nd One is Provider :

The second key component that makes Terraform go are providers for specific technologies.

This is typically cloud providers like AWS or Azure but can be any other infrastructure or platform as a service tool. 

Kubernetes, for instance, would also be considered a provider that Terraform utilizes.

Terraform has more than one hundred providers for various technologies, granting users access to its resources.

If you’re using AWS, for instance, Terraform will also have access to EC2 instances and other resources within the tech stack.

You can then create infrastructure on different levels, stacking Kubernetes on top of Azure, for example.

This is how Terraform works, using both Core and Provider functionality to complete your application and infrastructure setup quickly and using only code




## Steps to follow in terraform framework:

Following are the general steps that are involved in the lifecycle of a resource creation:

Define: Author your Infrastructure as Code in a Terraform configuration file with all the required blocks.

Initialize: Initialize the Terraform working directory and download any necessary plugins. This is usually done using terraform init command.

Review: Review the Terraform execution plan to see what changes will be made to the infrastructure. This is done using the terraform plan command. Running this command will show the actions that Terraform is going to perform when terraform apply command is run.

Apply: Apply the changes to create or modify the infrastructure. Once you are comfortable with the changes that are shown in the output of terraform plan command, you can apply those changes using terraform apply command.

Inspect: You can Inspect the state of the infrastructure using the Terraform state file.

In case you need to apply any new configuration, make the necessary changes in the config and follow the above steps to apply the configuration.

These steps are often repeated as part of a Continuous Integration/Continuous Delivery (CI/CD) pipeline or as part of ongoing infrastructure management. 

Terraform’s declarative approach to infrastructure as code allows for a consistent and reproducible workflow, where infrastructure changes can be tracked, reviewed, and audited over time.

## Simple method of writing a terraform script :

provider “aws” {
    region = “us-west-1”
}

resource “aws_instance” “myec2” {
    ami = “ami-12345qwert”
    instance_type = “t2.micro”
}

The code consists of two blocks wrapped in curly braces ( {} ), and each of these blocks has certain arguments defined.


The provider block takes one input label – the name of the provider. In this case “aws”. It also tells Terraform to install the AWS provider plugin, during the init phase.

The resource block takes 2 inputs labels – the type of resource and the name of the resource. In this case, the type is “aws_instance” and the name is “myec2”.

Terraform then takes these inputs and determines what actions need to be taken. 

It takes the user-specified desired state, compares it with the current state, and configures the architecture in a way that closes the gaps.

Terraform Core essentially figures out what needs to be created, updated, or deleted in order to fully provision your infrastructure.

## Commands for Terraform :

This should be the first command you run after creating your configuration files to ensure your code is formatted using the HCL standards. 
This makes it easier to follow and aids collaboration.

1.terraform fmt — Format your Terraform configuration files using the HCL language standard

2.terraform fmt --recursive — Also format files in subdirectories

3.terraform fmt --diff — Display differences between original configuration files and formatting changes.

4.terraform init — In order to prepare the working directory for use with Terraform, the terraform init command performs Backend Initialization, Child Module Installation, and Plugin Installation.

5.terraform init -get-plugins=false — Initialize the working directory, do not download plugins.

6.terraform get — Download and installs modules needed for the configuration.

7.terraform get -update — Che
ck the versions of the already installed modules against the available modules and installs the newer versions if available.

8.terraform validate — Validate the configuration files in your directory and does not access any remote state or services.

9.terraform plan — Plan will generate an execution plan, showing you what actions will be taken without actually performing the planned actions.

10.terraform apply -auto-approve — Apply changes without having to interactively type ‘yes’ to the plan. Useful in automation CI/CD pipelines.

11.terraform destroy — Destroy the infrastructure managed by Terraform.

12.terraform refresh — Modify the state file with updated metadata containing information on the resources being managed in Terraform. Will not modify your infrastructure

## Q) What are Terraform Provisioners?

You can use provisioners to model specific actions on the local machine or on a remote machine in order to prepare servers or other infrastructure objects for service

## Q) what is state file and manifest file in terraform ?






Basic Syntax of Terraform :


resource "aws_vpc" "main" {
  cidr_block = var.base_cidr_block
}

<BLOCK TYPE> "<BLOCK LABEL>" "<BLOCK LABEL>" {
  # Block body
  <IDENTIFIER> = <EXPRESSION> # Argument
}


Blocks are containers for other content and usually represent the configuration of some kind of object, like a resource.

Blocks have a block type, can have zero or more labels, and have a body that contains any number of arguments and nested blocks.

Most of Terraform's features are controlled by top-level blocks in a configuration file.

Arguments assign a value to a name. They appear within blocks.

Expressions represent a value, either literally or by referencing and combining other values. They appear as values for arguments, or within other expressions.

The Terraform language is declarative, describing an intended goal rather than the steps to reach that goal.

The ordering of blocks and the files they are organized into are generally not significant; Terraform only considers implicit and explicit relationships between resources when determining an order of operations

## Q) Terraform Interview Questions :

1. Define IAC?

IAC or Infrastructure as Code allows you to build, change, and manage your infrastructure through coding instead of manual processes.

 The configuration files are created according to your infrastructure specifications and these configurations can be edited and distributed securely within an organization.

2. What are the key features of Terraform?

Terraform helps you manage all of your infrastructures as code and construct it as and when needed. Here are its key main features:

A console that allows users to observe functions 
The ability to translate HCL code into JSON format
A configuration language that supports interpolation 
A module count that keeps track of the number of modules applied to the infrastructure.


3. What are the most useful Terraform commands?

Some of the most useful Terraform commands are:

terraform init - initializes the current directory
terraform refresh - refreshes the state file
terraform output - views Terraform outputs
terraform apply - applies the Terraform code and builds stuff
terraform destroy - destroys what has been built by Terraform
terraform graph - creates a DOT-formatted graph
terraform plan - a dry run to see what Terraform will do

4. What is a Private Module Registry?

A Private Module Registry is a feature from Terraform Cloud that allows you to share Terraform modules across the organization.

 You can enforce rules or “sentinel policies” on the registry that specify how members of your organization can use the modules.

 5 What are the components of Terraform architecture?

The Terraform architecture includes the following features:

Sub-graphs
Expression Evaluation
Vertex Evaluation
Graph Walk
Graph Builder
State Manager
Configuration Loader
CLI (Command Line interface)
Backend
