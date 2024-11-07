# Script to create a Lab environment in AWS automatically

## What is it?
This Terraform script will create a dedicated Lab environment in your AWS Account that consists of:
- a dedicated VPC with a public and a private subnet (IP-Ranges can be defined)
- Internet connectivity for all elements, for private subnet via NAT GW
- an internet facing (Linux) Jumphost
- a (defined by variables) Number of Linux (Ubuntu) and Windows Instances

## How does it work?

### Prerequisites:
- git needs to be installed
- aws cli needs to be installed and properly configured for your AWS environment
- Terraform needs to be installed and properly configured

## What to do?

- pull the repo
  ```
  git clone https://github.com/VolkerMarschner/aws_lab_env.git
  ```
