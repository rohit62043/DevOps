## AWS EC2 Instance Access from Windows using MobaXterm

---

### ✅ Prerequisites

- AWS account
- Windows laptop/PC
- Basic knowledge of launching EC2 instance

---

### 🖥️ Step-by-Step Guide to Access EC2 via MobaXterm

#### 1. **Launch EC2 Instance (Ubuntu)**

- Go to AWS EC2 dashboard
- Click on **Launch Instance**
- Instance name: e.g., `test-windows`
- Select **Ubuntu AMI**
- Choose instance type: **t2.micro**

#### 2. **Create Key Pair**

- Click on **Create new key pair**
- Key pair name: `windows-demo`
- Key file format: `.pem` (default)
- Download the `.pem` file and keep it safe (usually saved in Downloads folder)

#### 3. **Check Network Settings**

- Make sure Public IP is enabled
- SSH port (22) is open in the security group for **0.0.0.0/0** (Anywhere)

#### 4. **Launch Instance**

- Click on **Launch Instance**
- Wait until status shows "Running"

---

### 🔽 Download and Install MobaXterm

#### 1. **Search for MobaXterm Download**

- Google: `Download MobaXterm`
- Choose **Community Edition (Home)**

#### 2. **Download Installer**

- Select the **Installer Edition** (not Portable)
- Install the application by double-clicking the downloaded `.exe`

#### 3. **Install MobaXterm**

- Extract the ZIP file if needed
- Open the installer and follow steps:
  - Click **Next**
  - Accept license agreement
  - Click **Install**
  - Finish installation

---

### 🔐 Configure MobaXterm for EC2 Access

#### 1. **Open MobaXterm**

- Search and open MobaXterm from Start menu

#### 2. **Create New SSH Session**

- Click on **Session > SSH**
- Hostname: **Public IP of EC2 instance**
- Username: `ubuntu`

#### 3. **Attach Private Key (.pem)**

- Go to **Advanced SSH Settings**
- Enable: `Use private key` option
- Browse and select the downloaded `.pem` file (e.g., `windows-demo.pem`)

#### 4. **Connect to Instance**

- Click **OK**
- Accept the SSH certificate prompt
- You should now be logged into your EC2 Ubuntu instance 🎉

---

### 🧪 Verify Connection

Run a few commands in the EC2 terminal:

```bash
sudo apt update
uname -a
whoami
```

---

### ✅ Summary

- No need to use PuTTY or VirtualBox
- MobaXterm provides a simple GUI-based SSH access
- Seamless EC2 login with `.pem` file support
- Ideal for beginners using Windows machines

---

### 📅 Next Steps

Stay tuned for **Day 17**, where we'll dive into **AWS CloudWatch** monitoring.

---

### 🎥 Credits

Video tutorial by **Abhishek** on the **DevOps Zero to Hero** YouTube series.

---

### 📎 Useful Links

- [MobaXterm Official Site](https://mobaxterm.mobatek.net/)
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)

