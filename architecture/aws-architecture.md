# ☁️ AWS Architecture – CTF ZeroDay

This document explains the cloud infrastructure used to host the CTF platform and vulnerable applications.

---

## 🏗️ Infrastructure Overview

The architecture consists of two main EC2 instances:

### 1. CTFd Server
- Hosts the CTF platform (scoreboard, login, challenges)
- Runs on port **8000**
- Handles user interaction and scoring

### 2. Challenge Server
- Hosts multiple vulnerable web applications
- Each challenge runs on a separate port:
  - 8001 – Basic JavaScript
  - 8002 – JWT Exploitation
  - 8003 – Shadow API
  - 8004 – Time Capsule
  - 8005 – Trust Chain

---

## 🌐 Network Flow

1. Users access the CTF platform via public IP
2. CTFd serves challenges and tracks progress
3. Users interact with vulnerable applications via exposed ports
4. All traffic is routed through AWS security groups

---

## 🔐 Security Configuration

- Security groups configured to allow:
  - Port 8000 (CTFd)
  - Ports 8001–8005 (Challenges)
- SSH access restricted for admin use
- Public access enabled only for required ports

---

## 📊 Architecture Diagram (Conceptual)
    [ Users ]
        |
        v
 -----------------
 |   CTFd EC2   |  (Port 8000)
 -----------------
        |
        v
 -----------------
 | Challenge EC2 |
 -----------------
  |  |  |  |  |
 8001–8005 (Apps)

 
---

## ✅ Key Highlights

- Multi-service deployment on AWS EC2
- Isolation between platform and challenge environment
- Real-world simulation of attack surfaces
- Scalable for future CTF events
