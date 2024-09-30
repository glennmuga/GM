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

The first is the source input that the user configures into Terraform, defining what resources need to be created or provisioned. 

The second input source consists of data feeds into Terraform about what the current infrastructure setup looks like.





## Steps tp follow in terraform framework:

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
