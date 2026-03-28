# 🧩 CTFd Installation Guide

This document explains how the CTFd platform was deployed on AWS EC2 for hosting the CTF competition.

---

## 📦 What is CTFd?

CTFd is an open-source platform used to host Capture The Flag (CTF) competitions, including:
- User registration & login
- Challenge hosting
- Scoreboard tracking

---

## ⚙️ Prerequisites

- AWS EC2 instance (Ubuntu)
- Ports open: 8000
- Docker installed

---

## 🐳 Installing Docker

bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker

🚀 Running CTFd Using Docker
docker run -d -p 8000:8000 ctfd/ctfd
🌐 Accessing the Platform
Open browser
Go to:
http://<EC2-PUBLIC-IP>:8000
Complete initial setup:
Create admin account
Set CTF name
Configure settings
🧪 Challenge Configuration

Inside CTFd:

Add new challenges
Upload challenge files
Assign categories:
Web
Forensics
Crypto
🔐 Security Considerations
Avoid exposing unnecessary ports
Use strong admin credentials
Restrict SSH access
Monitor usage during live event
