# VPC

A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud

- This is an ansible script to create a VPC in ohio(us-east-2) region ,having 2 public subnets and 1 private subnet.
- An IAM user has to be created for the purpose of programatic access, having administrative policy.
- VPC cidr is taken as 172.16.0.0/16
- 3 subnets created for the same.
- This script is run under a virtual python environment to get rid from module missing complications in normal  environment.
- New instances are creating using Amazon Linux 2 AMI (HVM).

# Installation of ansible and python dependencies
```sh
  $ sudo amazon-linux-extras install epel
  $ sudo yum install epel-release -y
  $ sudo yum install ansible
  $ ansible --version
  $ sudo yum update
  $ sudo yum install python3
  $ sudo yum install python3-pip
  $ sudo pip3 install virtualenv 
  $ virtualenv -p /usr/bin/python3 venv
  $ source venv/bin/activate
  $ pip3 install boto3
  $ pip3 install boto
``` 
 
### Check Syntax
```sh
  $ ansible-playbook --syntax-check vpc.yml
```
### Run Script

```sh
  $ ansible-playbook vpc.yml
```

