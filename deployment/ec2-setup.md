# 🚀 EC2 Setup for CTF ZeroDay

This document explains how the AWS EC2 infrastructure was set up to host the CTF platform and vulnerable applications.

---

## 🖥️ Instance Configuration

Two EC2 instances were used:

### 1. CTFd Server
- Purpose: Host CTF platform (scoreboard + challenges)
- OS: Ubuntu
- Port: 8000

### 2. Challenge Server
- Purpose: Host vulnerable web applications
- OS: Ubuntu
- Ports: 8001 – 8005

---

## ⚙️ Steps to Launch EC2 Instance

1. Go to AWS Console
2. Navigate to EC2 → Launch Instance
3. Choose:
   - AMI: Ubuntu Server
   - Instance Type: t2.micro (or higher)
4. Configure Security Group:
   - Allow HTTP (80)
   - Allow Custom TCP:
     - 8000
     - 8001–8005

---

## 🔐 Security Group Configuration

| Port | Purpose |
|------|--------|
| 8000 | CTFd Platform |
| 8001 | Basic JavaScript |
| 8002 | JWT Challenge |
| 8003 | Shadow API |
| 8004 | Time Capsule |
| 8005 | Trust Chain |

---

## 🔧 Initial Setup Commands

After connecting to EC2:

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
