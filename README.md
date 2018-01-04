# AWS CloudFormation Starter Playbook

## Introduction

This repository provides setting up Sample Microservices Architecture using AWS infrastructure using Ansible and CloudFormation.

## Prerequisites

To run this playbook on your local machine, you must install the following prerequisites:

- Ansible 2.4 +
- Python PIP package manager
- The following PIP packages:
  - awscli
  - boto3
  - netaddr
- jq

You must also configure your local environment with your AWS credentials and you will also need to specify the ARN of the IAM role that your playbook will use to run provisioning tasks.  Your credentials must have permissions to assume this role.

### macOS Env - Brew guys are on their Own :-) or switch to Linux 

## Getting Started

1. Review [`roles/requirements.yml`](./roles/requirements.yml) and modify if required
2. Install roles by running `make roles` (which executes `ansible-galaxy install -r roles/requirements.yml`)
4. Define environments in the [`inventory`](./inventory) file and [`group_vars`](./group_vars) folder.  Alternatively you can use the `make environment/<environment-name>` command.

More info to follow