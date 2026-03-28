# 🚀 AWS CTF ZeroDay Infrastructure

Cloud-hosted Capture The Flag (CTF) platform built using AWS EC2 and CTFd, featuring real-world cybersecurity challenges across web, API, and authentication domains.

---

## ☁️ Architecture Overview


::contentReference[oaicite:0]{index=0}


### 🏗️ Infrastructure
- 2 EC2 Instances:
  - CTFd Platform (Port 8000)
  - Challenge Server (Ports 8001–8005)
- Public access for participants
- Security groups configured for controlled exposure

---

## 🌐 Deployed Challenges

| Challenge | Type | Port |
|----------|------|------|
| Basic JavaScript | Client-side vulnerability | 8001 |
| JWT Exploitation | Authentication bypass | 8002 |
| Shadow API | Hidden endpoints | 8003 |
| Time Capsule | Logic flaw | 8004 |
| Trust Chain | Access control issue | 8005 |

---

## 🧠 Skills Demonstrated

- AWS Cloud Deployment  
- Docker & Containerization  
- Web Application Security  
- API Security Testing  
- CTF Infrastructure Management  

---

## 📁 Project Structure
aws-ctf-zeroday-infrastructure/
├── architecture/
├── deployment/
├── challenges/
├── ctfd-backup/
└── screenshots/


## 👨‍💼 Role

**Event Head – CTF ZeroDay (Xactitude 2026)**  
- Designed and deployed AWS infrastructure  
- Created and tested vulnerable applications  
- Managed live CTF event operations  

---

## ⚠️ Disclaimer

This project is intended for **educational purposes only**.  
All vulnerabilities are intentionally created for learning.

---

## 🚀 Future Improvements

- Infrastructure as Code (Terraform)  
- Docker Compose setup  
- Logging & monitoring (CloudWatch)  
