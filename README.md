# Setting Up a Development Environment with AWS, VS Code, and Terraform.

In this project I went through Terraform basics to utilise Visual Studio Code (on Windows, Mac, or Linux) to deploy AWS resources and an EC2 instance. With this repositroy you can SSH into the EC2 instance and have your own redeployable environment that you can use for future projects.
## Prerequisites

- Download and install Visual Studio Code (VS Code) on your local machine.
- Create an AWS account if you don't have one already.

## AWS Setup

1. Create an IAM User:
   - Sign in to the AWS Management Console and search for "IAM."
   - On the IAM Dashboard, select "Users."
   - Click "Add user" and specify the user details:
     - Give the user a name.
     - Enable "Programmatic access" and disable "AWS Management Console access."
   - Set Permissions:
     - Select "Attach policies directly."
     - Give this user "AdministratorAccess."
   - Review the details and create the user.

2. Generate Access Key and Secret Key:
   - Select the IAM user you just created.
   - Go to the "Security credentials" tab.
   - Under "Access keys," click "Create access key."
   - Choose "Command Line Interface."
   - Click "Next" and then "Create access key."
   - Save the Access Key ID and Secret Access Key securely (e.g., download the .csv file).

## Local Setup

1. Use VS Code in the terminal:

2. Terraform Configuration:
   - Create Terraform configuration files (providers, variables, main, tfvars) for your project.

3. SSH Configuration (Optional):
   - Create an SSH configuration file to configure VS Code for your developer node's IP and other details.

4. Userdata Bootstrap:
   - Prepare userdata to bootstrap your developer node in the AWS EC2 instance.

## AWS Infrastructure Setup

1. Build VPC:
   - Set up the Virtual Private Cloud (VPC) for your environment.

2. Internet Gateway:
   - Create an internet gateway for communication with the public internet.

3. Public Route Table:
   - Set up a public route table to direct traffic to the internet gateway.

4. Security Group:
   - Create a security group with necessary inbound and outbound rules.

5. Public Subnet:
   - Build a public subnet within the VPC for the EC2 instance.

6. EC2 Instance:
   - Launch an EC2 instance in the public subnet using the bootstrap userdata.

## Development Environment

With all the above steps completed, your development environment is set up:
- VS Code terminal has direct access to the EC2 node via a remote SSH session.
- You have file and SSH access to the EC2 node to run commands and deploy your applications.

Remember to manage your AWS credentials securely and avoid sharing them or committing them to version control.


Happy coding.
