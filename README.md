## Details

This repository sets up:

* A VPC
* A subnet
* An internet gateway
* A security group
* An SSH key pair
* A publicly-accessible EC2 instance
* Within the instance:
   * Python 2 (for Ansible)
   * Nginx

## Setup

1. Install the following locally:
    * [Terraform](https://www.terraform.io/)
    * [Terraform Inventory](https://github.com/adammck/terraform-inventory)
     
2. Create user in AWS IAM, generate accesskey and secret key

3. run below command to set aws credentials to system where you run terraform command
```sh
aws configure
```
4. Make sure ssh-agent is running by running below comamand
```sh

eval $(ssh-agent -s)

```
5. Generate ssh key and add to ssh-agent

```sh
ssh-keygen
ssh-add ~/.ssh/id_rsa

```

6.Run terraform command
```sh

terraform init
terraform plan
terraform apply

## Cleanup

```sh
cd terraform
terraform destroy
```
