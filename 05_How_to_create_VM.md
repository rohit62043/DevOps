# 🛠️ DevOps Zero to Hero - Day 4 Notes

## 🎯 Topic: Virtual Machines - Part 2

---

## 📅 Course Overview

- **45-day DevOps Zero to Hero course**
- **Day 4**: Deep dive into Virtual Machines (Part 2)
- If new, watch Day 0 to Day 3 on the playlist.

---

## 🔁 Recap from Day 3

- VM evolution: Physical servers → Virtual machines
- Benefits of VMs: cost-efficiency, cloud shift
- Data centers phasing out; replaced by cloud (AWS, Azure, OpenStack)

---

## 📚 What You'll Learn Today

- Creating Virtual Machines on:
  - AWS
  - Azure
  - On-premise (non-cloud environment)
- Theoretical + Practical demonstration
- Introduction to automation using APIs and tools

---

## ☁️ Creating VMs on AWS (UI)

1. Go to **AWS Console** (`console.aws.amazon.com`)
2. Login or **Create AWS account**
3. Navigate to `EC2` service
4. Click **Launch Instance**
5. Choose:
   - **Name**: e.g. `test`
   - **OS**: Ubuntu recommended
   - **Instance type**: Select **Free Tier Eligible**
6. Create **Key Pair (PEM format)** and download
7. Launch instance → wait for status `Running`

---

## ☁️ Creating VMs on Azure (UI)

1. Go to [portal.azure.com](https://portal.azure.com)
2. Login (can use **GitHub** for quick login)
3. Click **Create Resource** > **Virtual Machine**
4. Provide similar details as in AWS
5. Azure also supports free tier, but **only for 30–45 days**

---

## 🛠️ Behind the Scenes: What Happens?

### Manual Process:

- User logs in
- Uses AWS Console / Azure Portal
- Requests VM (EC2 in AWS, VM in Azure)
- Provider returns:
  - IP address
  - Access credentials

---

## 💡 DevOps Mindset: Focus on **Efficiency**

- Manual creation is inefficient for scale
- Solution: **Automation**
- Goal: Save time, reduce errors

---

## 🔁 Automating VM Creation

### ☁️ AWS Automation Options:

| Tool                 | Description                                    |
| -------------------- | ---------------------------------------------- |
| AWS CLI              | Command-line interface                         |
| AWS API (EC2 API)    | Direct programmatic access                     |
| Boto3                | Python SDK for AWS                             |
| CloudFormation (CFT) | Template-based infrastructure as code          |
| AWS CDK              | Code-based infra (supports multiple languages) |

---

### ☁️ Multi-Cloud Automation: **Terraform**

- Open-source by HashiCorp
- Works across:
  - AWS
  - Azure
  - GCP
- Best for **hybrid cloud** scenarios

---

## 🔒 AWS EC2 API Security Requirements

1. **Valid** request format
2. **Authenticated** user (valid AWS credentials)
3. **Authorized** user (permissions to create EC2)

---

## 🤖 Automation Flow

```plaintext
Script (CLI, API, etc.)
       ↓
AWS EC2 API
       ↓
EC2 Instance Created
```
