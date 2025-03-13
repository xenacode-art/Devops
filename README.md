AWS EC2 Instance Launcher

Description

This Python script automates the creation of multiple AWS EC2 instances using Boto3. It helps in quickly deploying cloud resources without manually using the AWS console.

Prerequisites

Before running the script, ensure you have the following:

An AWS account with proper IAM permissions.

AWS CLI configured with access keys (aws configure).

Boto3 library installed (pip install boto3).

A valid AMI ID, security group, key pair, and subnet ID.


Usage

1. Edit the script and update:

AWS_REGION

AMI_ID

SECURITY_GROUP

KEY_NAME

SUBNET_ID



2. Run the script:

python launch_ec2.py


3. Output Example:

Instance ID: i-1234567890abcdef0 launched successfully in us-east-1
Instance ID: i-0987654321abcdef1 launched successfully in us-east-1



Customization

Change the INSTANCE_COUNT variable to launch more or fewer instances.

Modify the instance type (t2.micro, t3.medium, etc.).

Add additional IAM roles, user data, or monitoring options.


Cleanup

To terminate all launched instances, use:

aws ec2 terminate-instances --instance-ids <instance_id_1> <instance_id_2> ...


---
