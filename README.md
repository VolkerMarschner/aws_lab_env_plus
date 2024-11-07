# Script to create a Lab environment + an EKS Cluster in AWS automatically

## What is it?
This Terraform script will create a dedicated Lab environment in your AWS Account that consists of:
- a dedicated VPC with a public and a private subnet (IP-Ranges can be defined)
- Internet connectivity for all elements, for private subnet via NAT GW
- an internet facing (Linux) Jumphost
- a (defined by variables) Number of Linux (Ubuntu) and Windows Instances
- a minimum size AWS EKS Cluster

## How does it work?

### Prerequisites:
- git needs to be installed
- aws cli needs to be installed and properly configured for your AWS environment
- Terraform needs to be installed and properly configured

## What to do?

- pull the repo
```
  git clone https://github.com/VolkerMarschner/aws_lab_env_plus.git
```
- cd into directory aws_lab_env_plus
```
  cd aws_lab_env_plus
```
- edit the file variables.tf and adjust values according to your needs. At minimum you should edit the variable "prefix", which controls the naming of newly created ressources.
 
- Let Terraform do its magic by issuing the following commands
```
 terraform init
 terraform plan
 terraform apply
```
- After a successful run, you will find information about IPs, DNS Names, private SSH keys etc. in the same directory

## Once you do no longer need the environment, simply do a
```
  terraform destroy
```
