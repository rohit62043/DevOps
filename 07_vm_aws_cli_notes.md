# Day 5: Efficient Way of Creating and Managing Virtual Machines on AWS

## Overview

Today’s session focuses on:

- Logging into AWS EC2 Instances
- Automating EC2 Instance creation
- Tools and scripting methods

---

## Recap of Previous Classes

- Concept of Virtual Machines
- Manual creation of VMs
- Connecting to VMs via AWS Console

---

## Ways to Login into AWS EC2

### 1. Using AWS Console

- Navigate to **EC2 Dashboard**
- Select the running instance
- Click **Connect**
- Use provided options to connect via browser-based terminal

### 2. Using Local Terminal

#### Tools per OS:

- **Mac**: iTerm
- **Windows**: PuTTY, MobaXterm, NoMachine

#### Steps:

1. Identify **Public IP** of EC2 instance
2. Use the `.pem` key (Key Pair)
3. Run SSH Command:

```bash
ssh -i /path/to/key.pem ubuntu@<public-ip>
```

#### Common Errors:

- **Permission Denied**: Fix using

```bash
chmod 600 /path/to/key.pem
```

---

## Automating EC2 Creation

### Option 1: AWS CLI

#### Installation:

- Download based on OS: [AWS CLI Install Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

#### Configuration:

```bash
aws configure
# Provide Access Key, Secret Key, Region, Output Format
```

#### Verifying:

```bash
aws --version
```

#### Example: List S3 Buckets

```bash
aws s3 ls
```

#### Create S3 Bucket

```bash
aws s3 mb s3://your-unique-bucket-name
```

#### Create EC2 Instance

- Refer to AWS CLI Docs: [Run Instances](https://docs.aws.amazon.com/cli/latest/reference/ec2/run-instances.html)

---

### Option 2: AWS CloudFormation Template (CFT)

#### Purpose:

- Define infrastructure as code (IAC)
- Declarative approach

#### Steps:

1. Find Templates on [AWS Labs GitHub](https://github.com/awslabs/aws-cloudformation-templates)
2. Go to **CloudFormation** in AWS Console
3. Choose **Create Stack**
4. Upload or paste template YAML/JSON
5. Follow the wizard to launch

> Full IAC topic (CFT & Terraform) will be covered later

---

### Option 3: AWS API via Boto3 (Python)

#### Use case:

- Programmatic access and automation

#### Setup:

- Install:

```bash
pip install boto3
```

- AWS credentials auto-loaded via `aws configure`

#### Example: List EC2 Instances

```python
import boto3

ec2 = boto3.client('ec2')
response = ec2.describe_instances()
print(response)
```

> Refer to official [Boto3 Docs](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

---

## Instance Management

- **Stop Instance**: Temporarily halt to avoid billing
- **Terminate Instance**: Permanently delete

---

## Assignment

1. Install AWS CLI
2. Configure using `aws configure`
3. Connect to your EC2 instance via terminal
4. List/Create resources (e.g., S3 bucket or EC2)

---

## References

- [AWS CLI Docs](https://docs.aws.amazon.com/cli/latest/index.html)
- [AWS CloudFormation Templates GitHub](https://github.com/awslabs/aws-cloudformation-templates)
- [Boto3 Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

---

## Reminder

- Secure your access keys and `.pem` files
- Avoid using the AWS Console for repetitive tasks — automate instead

---

## Feedback & Sharing

- Like, comment, and share the video
- Reach out with questions in the comment section
- Encourage others to join the DevOps series

