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
# AWS Credentials
- You will need a Public key, ssh-keygen -t rsa
- Keep this key as it will be needed to create the server
- In order for the AWS CLI connection to work, your credentials will have to match with AWS
- These are the AWS Access Key ID, Secret Access Key, and Session Token. These can be found at the AWS details by clicking CLI: Show
- Note that these can change show make sure you have the correct credentials 
# Starting The Server
- Run the command terraform init
- Run the command terraform apply
- Because I made this on Windows I couldn't write a direct file path. So instead I made it to where you input your public key
- When it asks for the key, input the whole key (e.g. ssh-rsa *bunch of letters*)
- Now it will begin creating the minecraft server
- There should be an output with the IP of the minecraft server
- Copy the IP and wait a few minutes before connecting to it on Minecraft
# Destroy The Server
- Now that workers have defeated the Ender Dragon, the server has become stale
- To make sure they enjoy Minecraft again, destroy the server with the command terraform destroy
