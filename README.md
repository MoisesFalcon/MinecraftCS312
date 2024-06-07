# MinecraftCS312
# Setup
- First you'll need the correct tools to create the minecraft server. The tools needed are Terraform and AWS CLI
- I did this on windows so the easiest way to install Windows is through Chocolatey (https://chocolatey.org/)
- choco install Terraform
- To install AWS CLI follow the Amazon documentation for Windows (https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
# Terraform
- Now we will create a terraform file called main.tf
- Copy the main.tf file from the Git Repo.
- If you want to make any changes to the aws instance, those changes can be made to resource "aws_instance" "minecraft" {}
- The instance creates a new security group in resource "aws_security_group" "minecraft" {} and this also follows the settings for part 1
- The main.tf script is ready to be used!
# Starting The Server
- Run the command terraform init
- Run the command terraform apply
- There should be an output with the IP of the minecraft server
- Copy the IP and wait a minute before connecting to it on Minecraft
# Destroy The Server
- Now that workers have defeated the Ender Dragon, the server has become stale
- To make sure they enjoy Minecraft again, destroy the server
