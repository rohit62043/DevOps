# 📘 Linux OS & Shell Scripting Basics - DevOps Zero to Hero (Day 4)

## 📌 Introduction

- **Instructor**: Abhishek
- **Topic**: Linux Operating System & Shell Scripting Fundamentals
- **Series**: DevOps Zero to Hero (45 Days Free Course)
- **Objective**: Transform learners from zero to DevOps proficient

---

## 🖥️ What is an Operating System?

- A medium between software and hardware
- Examples: Windows, Linux, macOS
- Enables users to run applications on hardware like CPU, RAM, IO devices

### 🔁 Communication Flow:

```
User ↔️ Application ↔️ Operating System ↔️ Hardware ↔️ OS ↔️ Application ↔️ User
```

## 🐧 Why Linux?

- **Free & Open Source**
- **Secure**: No need for antivirus tools
- **Fast**: Optimized performance in production environments
- **Popular Distributions**: Ubuntu, CentOS, Debian, Alpine, Red Hat, Fedora

## 🧠 Linux Architecture Overview

```
|------------------------------|
| Compilers | User Processes   |
| System Software             |
|------------------------------|
|      System Libraries       |
|------------------------------|
|            Kernel           |
|------------------------------|
|          Hardware           |
```

### 🧩 Kernel Responsibilities

1. **Device Management**
2. **Memory Management**
3. **Process Management**
4. **System Call Handling**

---

## 💻 Shell Scripting Basics

### 🔍 What is a Shell?

- Interface to communicate with Linux OS via commands
- **Common Shells**: bash, sh, zsh
- Used widely in headless servers (no GUI)

### 📂 Important Commands

| Command   | Description                  |
| --------- | ---------------------------- |
| `pwd`     | Print working directory      |
| `ls`      | List files and directories   |
| `ls -ltr` | List with detailed info      |
| `cd`      | Change directory             |
| `cd ..`   | Move up one directory        |
| `mkdir`   | Create directory             |
| `rm`      | Remove file                  |
| `rm -r`   | Remove directory recursively |
| `touch`   | Create empty file            |
| `vi`      | Create & edit file           |
| `cat`     | Read file contents           |

### ✍️ vi Editor Quick Usage

- Enter: `vi filename`
- Press `i` to insert mode
- Write content
- Press `Esc`, then `:wq` to save & exit

---

## 🧮 Resource Monitoring Commands

| Command   | Purpose                        |
| --------- | ------------------------------ |
| `free -m` | Show memory usage              |
| `nproc`   | Show number of CPUs            |
| `df -h`   | Show disk space                |
| `top`     | Monitor CPU, memory, processes |

---

## 🧑‍💻 Practice Environment

- AWS EC2 Ubuntu instance used for demonstration
- Logged in via SSH using:

```bash
ssh -i <key.pem> ubuntu@<public-ip>
```

---

## 🎯 Summary

- Understood the importance & role of an OS
- Explored why Linux is preferred in DevOps
- Covered Linux OS architecture (Kernel-centric)
- Learned fundamental shell commands
- Navigated and manipulated files & directories
- Checked system health and performance

---

## 📚 Recommended Follow-ups

- 📺 **Shell Scripting Basics (Video 1)**
- 📺 **Shell Scripting Intermediate (Video 2)**
- 📺 **Shell Scripting Interview Questions (Video 3)**
- 📺 **Real-time DevOps Project with Shell Scripting (Upcoming)**

---

## 🙌 Final Notes

- Continue exploring the DevOps Zero to Hero playlist
- Practice shell commands hands-on via AWS EC2 or WSL
- Subscribe & follow for daily DevOps learning!

---

**✅ End of Notes**

